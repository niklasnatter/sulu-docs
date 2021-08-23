Tag Selection
=============

Description
-----------

Shows a simple text line with an autocomplete feature for the available Tags in
the system. Tags can be managed in the settings section of Sulu. The assigned
tags will be saved as an array.

.. note::

    Tags which do not already exist will be created.

.. note::

    This content type is rarely needed because the ``Excerpt and Taxonomies``
    allows to assign tags to pages.

Parameters
----------

.. list-table::
    :header-rows: 1

    * - Parameter
      - Type
      - Description
    * - request_parameters
      - collection
      - Collection of parameters that are appended to the requests sent by the selection.
    * - resource_store_properties_to_request
      - collection
      - Collection of property names.
        The value of the respective properties are appended to the requests sent by the selection.

Example
-------

.. code-block:: xml

    <property name="tags" type="tag_selection">
        <meta>
            <title lang="en">Tags</title>
        </meta>
    </property>

Twig
----

.. code-block:: twig

    {% for tag in content.tags %}
        {{ tag }}
    {% endfor %}
