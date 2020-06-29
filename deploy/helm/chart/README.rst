-----------------------
Deploy using Helm Chart
-----------------------

Assuming that you have already helm properly configured (refer to helm docs), below command will install chart in the
currently active Kubernetes cluster context.

This will deploy a single pod with kube-resource-report and nginx (to serve the static HTML):

.. code-block::

    $ git clone https://github.com/hjacobs/kube-resource-report
    $ cd kube-resource-report
    $ helm install --name kube-resource-report ./unsupported/chart/kube-resource-report
    $ helm status kube-resource-report

If you want to do upgrade, try something like:

.. code-block::

    $ cd kube-resource-report
    $ git fetch --all
    $ git checkout master & git pull
    $ helm upgrade kube-resource-report ./unsupported/chart/kube-resource-report
    $ helm status kube-resource-report

Use ``helm status`` command to verify deployment and obtain instructions to access ``kube-resource-report``.
