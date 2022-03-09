### k8sJobRunner

This is a thought experiment for someone who wants to run reports in a k8s environment. Would one need to write any custom controllers via operator pattern/CRD if they wanted to run a set of report generating jobs in a kubernetes cluster? A [job](https://kubernetes.io/docs/concepts/workloads/controllers/job/) in k8s is a native resource and in this case a job is going to run a report. For this experiment we can assume that a report is a simple command like calculating pi as shown in some of the publicly available job examples or it could run a custom golang binary that takes publicly available inputs and produces a report.

We will zoom in on the lifecycle of these reports (jobs that produce the reports) and discuss more about when and if a custom controller or an api server is needed.
