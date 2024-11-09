GameObject Class
================

The `GameObject` class represents an entity in a scene graph, allowing for hierarchical organization of game objects. It provides methods for managing child objects, retrieving objects by path, and interacting with the Windows API for window management.

**Namespace:** CurrensEngine

Public Attributes
-----------------
- **Name** (string): The name of the GameObject, used for searching objects.
- **OnChildAdded** (Action<GameObject>): Action invoked when a new child object is added.
- **Parent** (GameObject): The parent GameObject in the scene hierarchy.
- **Children** (List<GameObject>): A list of child GameObjects associated with this GameObject.

Public Methods
--------------
- **GameObject()**: Initializes a new instance of the `GameObject` class.
- **GameObject(string name)**: Initializes a new instance with a specified name.
- **IntPtr GetHwnd()**: Retrieves the window handle of the GameObject.
- **void AddChild(GameObject @object)**: Adds a specified GameObject as a child, updating parent-child relationships.
- **void Destroy()**: Removes this GameObject and all its children from the scene.
- **GameObject GetObject(string path)**: Retrieves a GameObject by its relative path.
- **T GetObject<T>(string path)**: Retrieves a GameObject of a specified type by its relative path.
- **GameObject GetObjectOrNull(string path)**: Attempts to retrieve a GameObject by its path, returning null if not found.
- **string GetObjectPath()**: Retrieves the path of this GameObject relative to the root of the hierarchy.
- **T GetObjectOrNull<T>(string path)**: Attempts to retrieve a GameObject of a specified type, returning null if not found or not castable.
- **void Update()**: Updates the GameObject by refreshing its associated window.
- **virtual void _OnEnterTree()**: Called when the GameObject enters the scene tree; can be overridden for custom behavior.
- **virtual void _OnReady()**: Called when the GameObject is ready; can be overridden for custom behavior.

Usage Example
-------------
.. code-block:: csharp

   GameObject myObject = new GameObject("MyObject");
   myObject.AddChild(new GameObject("ChildObject"));
   GameObject foundObject = myObject.GetObject("ChildObject");

Exceptions
----------
- **ArgumentException**: Thrown when the specified GameObject cannot be found.
- **InvalidCastException**: Thrown when the found GameObject cannot be cast to the specified type.