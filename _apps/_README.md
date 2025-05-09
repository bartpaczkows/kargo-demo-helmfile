# _apps

This directory contains environment-specific files, each with a list of ArgoCD application deployment definitions.

*One definition is one ArgoCD application that deploys to one cluster-namespace.*

ArgoCD watches these files. Any addition/modification or deletion of the application definition there
is reflected in ArgoCD after file modification within 3 minutes automatically.


The name of the branch should be equal to the name of this file.
For example, to deploy on `fr2-pre-a01` one would modify `preprod.yaml` in `preprod` branch.
For your convenience, a set of default ArgoCD application deployment definitions
are provided in these files. To get the application created in ArgoCD:
* uncomment the whole definition (remove prepending #)
* push to the remote branch
* wait for 3 minutes and observe the application created in ArgoCD UI

If your target cluster is not present in the file, feel free to add it there following the same pattern.

Check the complete doc here: https://kyridev.atlassian.net/wiki/spaces/DEV/pages/13417676856/ArgoCD+Application+deployment+definitions+spec
