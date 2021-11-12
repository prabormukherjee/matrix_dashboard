**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

Run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation
![pod](./answer-img/po.png)
![services](./answer-img/svc.png)

## Setup the Jaeger and Prometheus source
Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.
![grafana](./answer-img/grafana.png)

## Create a Basic Dashboard
Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
![prometheus_in_grafana](./answer-img/prom-src.png)

## Describe SLO/SLI
Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.
The service level is the degree (i.e. level) of performance that an application (or service) provides to the user.
* SLI -> It is known as Service Level Indicator, a specific metric used to measure the performance of a service. For example, cpu usage, memory usage, error rate, uptime
* SLO -> It is known as Service Level Objective, a target value or range of values for a service level that is measured by an SLI. For example, 99% uptime and 95% of the request return is in 50 milliseconds in next month.  
A natural structure for SLOs is thus SLI ≤ target, or lower bound ≤ SLI ≤ upper bound. 

## Creating SLI metrics.
It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 
* request latency -> how long it takes to return a response to a request
* availability/uptime -> the fraction of the time that a service is usable
* system throughput -> how many units of information a system can process in a given amount of time
* error rate -> the frequency of errors
* Traffic -> The amount of stress on a system from demand

## Create a Dashboard to measure our SLIs
Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.
![sli_dashboard](./answer-img/sli.png)

## Tracing our Flask App
We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here.
![jaeger_trace](./answer-img/jaeger-ui.png)

## Jaeger in Dashboards
Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.
![jaeger_in_grafana](./answer-img/jaeger.png)

## Report Error
Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue.

TROUBLE TICKET

Name: Trial apps not working

Date: 12-11-2021

Subject: Trial button not working from frontend

Affected Area: Frondend and trial apps

Severity: High

Description: Button with triggers the trial app, isn't working properly and resulting 500 `Internal Server Error`


## Creating SLIs and SLOs
We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name three SLIs that you would use to measure the success of this SLO.
* Uptime > 99.9%
* latency < 50ms
* error rate < 0.3%

## Building KPIs for our plan
Now that we have our SLIs and SLOs, create KPIs to accurately measure these metrics. We will make a dashboard for this, but first write them down here.
* Uptime for backend, frontend, trial app services > 99.9%
* Latency for HTTP < 50ms
* Error rate (40x, 50x) < 0.3%
* CPU and Memory usage is moderate

## Final Dashboard
Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.
* CPU usage
* Memory usage
* Average CPU saturation
* Error rate
![final_kpi](./answer-img/kpi.png)

## Beautiful Dashboard
Some dashboards that're looking good
![best_sli](./answer-img/best-sli.png)
![best_kpi](./answer-img/best-kpi.png)