# Declarative ArgoCD's objects

## Application Set

## Applications and Projects
* Different alternatives to declare ArgoCD's
    * applications
    * projects
* How to create them?
    * Navigate to directory in which application exists
    * `kubectl apply -f NameOfTheFile`
* How to check that it has been created properly?
    * `kubectl get application -n argocd`
        * argocd
            * Namespace for ArgoCD created
        * Why if you get all (`kubectl get all -n argocd`) it doesn't appear?
    * `argocd app list`
    * via Web UI
* How to deploy / refresh new changes?
    * `kubectl apply -f NameOfTheFile`
* If the application or project live in a private repo
    * no change at all in it's definition is required
    * register the credentials as Kubernetes' secret is necessary


## Clusters

## Repos
* Private repos
    * Create Kubernetes' secret resource
    * Create personal access token to the private repo (:warning: Don't push it :warning:)
    * `kubectl apply -f NameOfTheFile`
    * `kubectl get secret -n argocd`
        * Check that secret has been created
    * Go ArgoCD Web UI, Settings, Repositories and check that a new one has been added
