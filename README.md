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
## Clusters

## Repos
