Containers
==========

To create a new container on one of your server, you just have to add it in the Containers menu and it will be automatically deployed.

.. image:: images/container-list.png

The important fields are :

- The container name. You can only use here lowercase, digit and hyphen.

- The application which will be hosted in the container, the server where it will be deployed and the image version which will be used. When you change the application value, it will automatically update the server, the image with the info from the application and the image version with the last version available.

- You can use the no save checkbox if you don’t want to auto backup this container, because it may take too long for example. Note that some times backups may be done anyway, like during a restoration for example.

- See the Image chapter for more information about the Privileged checkbox. Use with caution.

- Check the public checkbox if you want all users of the Clouder to be able to use this container. Otherwise, a user can only access a container if he is the manager of this container (or an administrator).

.. image:: images/gettingstarted-clouder-container.png

See the `Images <images.rst>`_ and `Applications <applications.rst>`_ chapters for more informations about options, ports, volumes, and links.

When you save the new container :

- The command to create the new container will be launched on the target server,

- The ports and volumes will be configured,

- An ssh key will be generated and automatically assigned to the container so Clouder can connect to it and go inside. Note that this key is updated daily.

- The commands post creation will finish to configure the container

- The links will be deployed.

You can check all the executed command in the log.

.. image:: images/container-log.png

If something went wrong, you can use the reinstall button to purge and reinstall the container. You can also also use the restart/stop buttons to restart the container and use the reset key button if Clouder can’t access the container or you want to update the key for security reasons.

| Finally, you have to configure in the save tab the backup container where the backup will be stored. The repository will be automatically created if needed, see the `Applications <applications.rst>`_ chapter for more informations about the others fields.
| You can use the Save button to force a manual backup, use the comment field if you want to easily find this backup later. Note that all saves update the next save date field.

.. image:: images/container-save.png
