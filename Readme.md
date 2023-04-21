# Simple code that can be used to asynchronously report the progress of operations

## To install for use:
- download the code
- Open your project/solution in visual studio
- In the solution explorer, right click on the solution
- Add existing project
- Select SimpleProgressWindow project you just downloaded
- Right click on your PROJECT
- Select build dependencies -> project dependencies
- Check the box next to Simple progress window
- Right click on references in YOUR project
- Add references
- Under projects, select SimpleProgressWindow

## To use:
- In your code, create a new class
- add 'using SimpleProgressWindow;' to using directives
- Make the class derive from SimpleMTBase
- Implement override of virtual function Run in the newly created class:
e.g.,
public override bool Run()
{
}
- Create an instance of this new class.
- Call the execute function of this class (contained in SimpleMTBase)
- Add function calls inside the overridden Run function in the newly created class
- Use UpdateUILabel and ProvideUIUpdate to update the progress window