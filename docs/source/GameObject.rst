Usage
=====

.. _installation:

Installation
------------
Code

.. code-block:: csharp
   public GameObject GetObject(string path)
{
    string[] names = path.Split('/');
    GameObject currentObject = this;

    foreach (string name in names)
    {
        if (name == "..")
            currentObject = currentObject.Parent;
        else
            currentObject = currentObject.Children.FirstOrDefault(o => o.Name.Equals(name, StringComparison.OrdinalIgnoreCase));

        if (currentObject == null)
            throw new ArgumentException($"Object with the name '{name}' not found.");
    }

    return currentObject;
}
   


