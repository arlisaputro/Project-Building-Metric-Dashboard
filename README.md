**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

*TODO:* run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

**kubectl monitoring**

![namespace_monitoring](https://user-images.githubusercontent.com/47803421/231892440-60c27c7d-ad3b-4eef-a36a-9b87300a5684.PNG)

**kubectl observability**

![namespace_observability](https://user-images.githubusercontent.com/47803421/231892475-c0514a63-deb5-47b0-8928-0eb11db889a7.PNG)

**kubectl default - Manifest App**

![namespace_default_apps](https://user-images.githubusercontent.com/47803421/231892520-b503e6d8-08c5-4cd2-9cae-44673c097a2e.PNG)

## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.

![grafana_login_datasource_prometheus](https://user-images.githubusercontent.com/47803421/231892543-31086690-24d7-4242-8c61-8d68bf3db3e1.PNG)


## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.

![dashboard_prometheus_1](https://user-images.githubusercontent.com/47803421/231892950-c5a77b3d-df4a-45d8-9c1e-574a739e152e.PNG)

![dashboard_prometheus_2](https://user-images.githubusercontent.com/47803421/231892967-07341a28-0b42-490e-bd8d-557a3cebeb31.PNG)

## Describe SLO/SLI
*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.
SLIs (Service Level Indicators) are quantitative measures that are used to assess the performance of a service or system. They are metrics that help to determine whether a service is meeting its SLOs (Service Level Objectives). In the context of an SLO for monthly uptime and request response time, SLIs could include:

monthly uptime: This metric would track the percentage of time that the service is available within a given month. It would be calculated by dividing the total time the service was up by the total time in the month and multiplying by 100. This metric would be used to track the SLO for monthly uptime.

Response time: This metric would track the time taken for the service to respond to a request. It would be measured in milliseconds and would be calculated as the time taken from when the request was received to when the response was sent. This metric would be used to track the SLO for request response time.


## Creating SLI metrics.
*TODO:* It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 
here are 5 metrics to measure SLIs for the SLOs of monthly uptime and request response time:

1.Uptime Percentage: This metric measures the percentage of time that a service is available during a given month. For example, if a service is available for 99.9% of the month, that means it experienced 43.2 minutes of downtime during the month.

2.Error Rate: This metric measures the number of errors or failures that occur during a given period, usually expressed as a percentage of requests. A high error rate could indicate issues with the application code, infrastructure, or other factors.

3.Mean Time to Detect (MTTD): This metric measures the time it takes to detect an issue or error in the service. This is important because the longer it takes to detect an issue, the longer the service will be unavailable or performing poorly.

4.Mean Time to Repair (MTTR): This metric measures the time it takes to resolve or fix an issue once it has been detected. A high MTTR can lead to longer periods of downtime or poor performance.

5.Request Latency: This metric measures the time it takes for a request to be processed from start to finish. This is important because slow response times can impact the user experience and potentially lead to lost business.

## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

![dashboard-sli](https://user-images.githubusercontent.com/47803421/231898390-869ebe7a-915b-478d-9d86-b86dc5223be1.PNG)


## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here. Also provide a (screenshot) sample Python file containing a trace and span code used to perform Jaeger traces on the backend service.

![span_python](https://user-images.githubusercontent.com/47803421/231898464-e4caf912-c0ae-4925-8137-b594556b8734.PNG)

![tracing_backend](https://user-images.githubusercontent.com/47803421/231898489-7f468fc5-2aae-4ef0-9fc3-61887e2837da.PNG)


## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.



## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue also include a screenshot of the tracer span to demonstrate how we can user a tracer to locate errors easily.

**TROUBLE TICKET**

**Name**: arli saputro

**Date**: 04/14/2023 9:21:09 PM

**Subject**: Front-end service is creating many 40x and 50x errors

**Affected Area**: API requests

**Severity**: High


**Description**:
The `static/js/click.js` file is not handling clicks correctly and requests can not be processed because the
fetch url are not right.


## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name four SLIs that you would use to measure the success of this SLO.

## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create a list of 2-3 KPIs to accurately measure these metrics as well as a description of why those KPIs were chosen. We will make a dashboard for this, but first write them down here.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
