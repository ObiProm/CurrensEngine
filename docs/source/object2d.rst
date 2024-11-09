Object2D Class
===============

The `Object2D` class represents a 2D object in the game engine, inheriting from the `GameObject` class. It provides functionality for rendering, positioning, and updating the object's state.

Namespace
---------
CurrensEngine

Public Attributes
-----------------
- **Position** (Vector2): The position of the 2D object in the game world.
- **Size** (Vector2): The size of the 2D object.
- **IsStatic** (bool): Indicates whether the object will be rendered only during initialization.

Public Methods
--------------
- **Object2D()**: Initializes a new instance of the `Object2D` class with default position and size.
- **Object2D(Vector2 pos, Vector2 size, bool isStatic)**: Initializes a new instance with specified position, size, and static state.
- **void InternalInstantiate()**: Creates the window for the 2D object using the specified initialization parameters.
- **void Invalidate()**: Invalidates the window, causing it to be redrawn.
- **virtual void CustomRender()**: Allows for custom rendering logic to be implemented in derived classes.

Internal Methods
----------------
- **void UpdatePosition()**: Updates the position of the 2D object in the window based on its current `Position` and `Size`.

Usage Example
-------------
.. code-block:: csharp

   Object2D myObject = new Object2D(new Vector2(100, 100), new Vector2(50, 50), false);
   myObject.CustomRender();

Exceptions
----------
No specific exceptions are documented for this class.

.. note::

   This project is under active development.
