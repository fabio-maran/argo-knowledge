# About this course
GitOps is a set of best practices that make your SCM (most common is a Git server) the source of truth for everything (and not just the application source code). With GitOps you describe your whole platform (infrastructure and applications) in a declarative format and use Git for storage, history, and auditing of your deployments.

GitOps agents constantly monitor the actual state, comparing against the desired state as defined in git and apply the desired state. Discarding custom deployment scripts and adopting a GitOps approach can help you avoid failed deployments, configuration drift, and fragile releases.

ArgoCD is a platform that enables GitOps for Kubernetes deployments. It allows you to describe your applications in a declarative format, it can eliminate configuration drift, and coupled with other Argo projects, it can change the way you work with Kubernetes.

Having covered the basics about GitOps with Argo CD in the previous course (GitOps fundamentals) we will now explore more advanced use cases and features of ArgoCD needed for both scale and practical implementation.
