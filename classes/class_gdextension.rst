:github_url: hide

.. DO NOT EDIT THIS FILE!!!
.. Generated automatically from Godot engine sources.
.. Generator: https://github.com/godotengine/godot/tree/master/doc/tools/make_rst.py.
.. XML source: https://github.com/godotengine/godot/tree/master/doc/classes/GDExtension.xml.

.. _class_GDExtension:

GDExtension
===========

**Inherits:** :ref:`Resource<class_Resource>` **<** :ref:`RefCounted<class_RefCounted>` **<** :ref:`Object<class_Object>`

A native library for GDExtension.

.. rst-class:: classref-introduction-group

Description
-----------

The **GDExtension** resource type represents a `shared library <https://en.wikipedia.org/wiki/Shared_library>`__ which can expand the functionality of the engine. The :ref:`GDExtensionManager<class_GDExtensionManager>` singleton is responsible for loading, reloading, and unloading **GDExtension** resources.

\ **Note:** GDExtension itself is not a scripting language and has no relation to :ref:`GDScript<class_GDScript>` resources.

.. rst-class:: classref-introduction-group

Tutorials
---------

- :doc:`GDExtension overview <../tutorials/scripting/gdextension/what_is_gdextension>`

- :doc:`GDExtension example in C++ <../tutorials/scripting/gdextension/gdextension_cpp_example>`

.. rst-class:: classref-reftable-group

Methods
-------

.. table::
   :widths: auto

   +------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
   | void                                                             | :ref:`close_library<class_GDExtension_method_close_library>` **(** **)**                                                                                  |
   +------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` | :ref:`get_minimum_library_initialization_level<class_GDExtension_method_get_minimum_library_initialization_level>` **(** **)** |const|                    |
   +------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
   | void                                                             | :ref:`initialize_library<class_GDExtension_method_initialize_library>` **(** :ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` level **)** |
   +------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`bool<class_bool>`                                          | :ref:`is_library_open<class_GDExtension_method_is_library_open>` **(** **)** |const|                                                                      |
   +------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+
   | :ref:`Error<enum_@GlobalScope_Error>`                            | :ref:`open_library<class_GDExtension_method_open_library>` **(** :ref:`String<class_String>` path, :ref:`String<class_String>` entry_symbol **)**         |
   +------------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------+

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Enumerations
------------

.. _enum_GDExtension_InitializationLevel:

.. rst-class:: classref-enumeration

enum **InitializationLevel**:

.. _class_GDExtension_constant_INITIALIZATION_LEVEL_CORE:

.. rst-class:: classref-enumeration-constant

:ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` **INITIALIZATION_LEVEL_CORE** = ``0``

The library is initialized at the same time as the core features of the engine.

.. _class_GDExtension_constant_INITIALIZATION_LEVEL_SERVERS:

.. rst-class:: classref-enumeration-constant

:ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` **INITIALIZATION_LEVEL_SERVERS** = ``1``

The library is initialized at the same time as the engine's servers (such as :ref:`RenderingServer<class_RenderingServer>` or :ref:`PhysicsServer3D<class_PhysicsServer3D>`).

.. _class_GDExtension_constant_INITIALIZATION_LEVEL_SCENE:

.. rst-class:: classref-enumeration-constant

:ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` **INITIALIZATION_LEVEL_SCENE** = ``2``

The library is initialized at the same time as the engine's scene-related classes.

.. _class_GDExtension_constant_INITIALIZATION_LEVEL_EDITOR:

.. rst-class:: classref-enumeration-constant

:ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` **INITIALIZATION_LEVEL_EDITOR** = ``3``

The library is initialized at the same time as the engine's editor classes. Only happens when loading the GDExtension in the editor.

.. rst-class:: classref-section-separator

----

.. rst-class:: classref-descriptions-group

Method Descriptions
-------------------

.. _class_GDExtension_method_close_library:

.. rst-class:: classref-method

void **close_library** **(** **)**

Closes the current library.

\ **Note:** You normally should not call this method directly. This is handled automatically by :ref:`GDExtensionManager.unload_extension<class_GDExtensionManager_method_unload_extension>`.

.. rst-class:: classref-item-separator

----

.. _class_GDExtension_method_get_minimum_library_initialization_level:

.. rst-class:: classref-method

:ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` **get_minimum_library_initialization_level** **(** **)** |const|

Returns the lowest level required for this extension to be properly initialized (see the :ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` enum).

.. rst-class:: classref-item-separator

----

.. _class_GDExtension_method_initialize_library:

.. rst-class:: classref-method

void **initialize_library** **(** :ref:`InitializationLevel<enum_GDExtension_InitializationLevel>` level **)**

Initializes the library bound to this GDextension at the given initialization ``level``.

\ **Note:** You normally should not call this method directly. This is handled automatically by :ref:`GDExtensionManager.load_extension<class_GDExtensionManager_method_load_extension>`.

.. rst-class:: classref-item-separator

----

.. _class_GDExtension_method_is_library_open:

.. rst-class:: classref-method

:ref:`bool<class_bool>` **is_library_open** **(** **)** |const|

Returns ``true`` if this extension's library has been opened.

.. rst-class:: classref-item-separator

----

.. _class_GDExtension_method_open_library:

.. rst-class:: classref-method

:ref:`Error<enum_@GlobalScope_Error>` **open_library** **(** :ref:`String<class_String>` path, :ref:`String<class_String>` entry_symbol **)**

Opens the library at the specified ``path``.

\ **Note:** You normally should not call this method directly. This is handled automatically by :ref:`GDExtensionManager.load_extension<class_GDExtensionManager_method_load_extension>`.

.. |virtual| replace:: :abbr:`virtual (This method should typically be overridden by the user to have any effect.)`
.. |const| replace:: :abbr:`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
.. |vararg| replace:: :abbr:`vararg (This method accepts any number of arguments after the ones described here.)`
.. |constructor| replace:: :abbr:`constructor (This method is used to construct a type.)`
.. |static| replace:: :abbr:`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
.. |operator| replace:: :abbr:`operator (This method describes a valid operator to use with this type as left-hand operand.)`
.. |bitfield| replace:: :abbr:`BitField (This value is an integer composed as a bitmask of the following flags.)`
