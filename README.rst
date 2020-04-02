.. image:: https://mybinder.org/badge_logo.svg
    :target: https://mybinder.org/v2/gh/ltetrel/binder-tuto/master?filepath=notebooks%2Fnilearn-example.ipynb

A binder tutorial
=================

Binder allows you to execute and share notebooks to anyone using the web.
The way `Binder <https://github.com/jupyterhub/binderhub>`_ download the notebooks is through a GitHub repo, where the user should specify the environment to run them.
This make your work reproducible and shareable very easy like never before!

It ties together many technologies :

* `Docker <https://www.docker.com/>`_, a tool that emphasizes reproducibility by packaging your applications into containers to run them from any host.
* `JupyterHub <https://jupyter.org/hub>`_, which uses `kubernetes <https://kubernetes.io/>`_ to share multiple instances of notebooks among many users.
* `repo2docker <https://github.com/jupyter/repo2docker>`_, a tool that converts GitHub repositories into Jupyter-enabled Docker images.

Pre-requisites
::::::::::::::
* GitHub ease
* Basic knowledge on python packages (pip)

What will you learn ?
:::::::::::::::::::::
* Create a binder link

How to upload a work on Binder ?
::::::::::::::::::::::::::::::::

Of course, you will need a GitHub account (GitLab, Gist also supported).
After you can:

1.  Create a repository with at least one notebook (your work).
2.  Make the ``requirements.txt`` file, containing all the dependencies for your notebook(s).
3.  Build your repository into a Docker image that will host your interactive notebooks : https://mybinder.org/
4.  After few seconds, the link to share your notebook(s) from your GitHub repository are ready. Share it to anyone who has an internet browser!

Few tips
::::::::

Check `this repo <https://github.com/ltetrel/binder-tuto>`_, you can also find other examples there.

If you execute your notebook before pushing it to github, any user that open the session will have a ready to play environment (without the need to re-execute the notebook).

You can add a badge in your repository. When clicking to this badge, anyone can access the executable environment in an easy way ! Just add this snippet to your README:

.. code-block:: markdown
    [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/<user_name>/<repo_name>/master)

Adding ``?urlpath=lab`` at the end of the link will open a jupyter lab environment.
You can also point to a specific notebook with ``?filepath=notebooks%2Fnilearn-example.ipynb``!


Acknowledgements
::::::::::::::::

@emdupre, @mathieuboudreau
