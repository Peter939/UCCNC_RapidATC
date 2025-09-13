# UCCNC_RapidATC
Macros for UCCNC and RapidATC

How to use in M6 RapidATC
Macro to add to the end of M6.txt in UCCNC using RapidATC.
Add Code in M6Ex.txt to the end of M6 in your profile.


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
