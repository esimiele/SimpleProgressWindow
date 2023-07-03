# Simple code that can be used to asynchronously report the progress of operations

## v1.1 updates:
- Option to set the window to close once operations are finished (SetCloseOnFinish method)
    - first argument is bool option to close window, second is timeout before close in msec
    - call this method in the constructor of the new class (default is set to leave window up until user closes window)
- Updated UI to report the time elapsed since start of running
- Added protected method to grab the elapsed time in the class derived from simplemtbase


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

![Alt text](/Documentation/SimpleProgressWindowDemoGIF.gif?raw=true)