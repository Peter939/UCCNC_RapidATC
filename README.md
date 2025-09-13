# Use a Tool Setter Probe in UCCNC with RapidATC (No IR Beam)

This macro code is for UCCNC but you can probably be adapted for other CNC control software such as Mach3, LinuxCNC and more.

How to use in M6 macro in UCCNC using the RapidATC.
Add the code in M6Ex.txt to the end of M6 in your profile.

Edit the code in function HandleToolRecognitionUnload() 

    if (!ToolRecognitionOverride)
    {
      // MessageBox.Show("Confirm tool unloaded and press OK to continue.", "Confirm Unload");
      CheckATC_DropLoad(false); // Run Tool drop check.;
    }
Edit the code in function HandleToolRecognitionLoad()

    if (!ToolRecognitionOverride)
    {
       // MessageBox.Show("Confirm tool loaded and press OK to continue.", "Confirm Load");
       CheckATC_DropLoad(true); // Run Tool load check.
    }
