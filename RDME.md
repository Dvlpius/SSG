# SSG[SuperSmartGUI]
An Super Smart GUI For
  1-Mobile Devices
    [SmartPhone]
    [Tablet]
  2-Desktop Devices
    [PC]
    [Laptop]
  3-IoT Devices
    [Gadget]
    [SmartHouse]
    [PublicEngineeringPluginModDevices]
    [PrivateEngineeringPluginModDevices]=>NoNeedSSG;
  4-Server Devices  ///Diabled Becuuze ServerDevices need TerminalMod and GIU not nessesary///
    [CiscoRouter]=>NoNeedSSG;
    [FireWall]=>NoNeedSSG;
  5-etc



///[MobileDev]///////////////////////
SSG for Mobile Devices
In this senario we have double mode,mode one named (Mode_0 or YoungUsr_mode),mode two named (Mode_1 or OldUsr_mode)

YoungUsr_mode: mean user has age from +10year to -40year;
YoungUsr_mode:in this mod we use Functions[TouchScreen, DigitalImage, DigitalVideo, DigitalAudio];
YoungUsr_mode: user can easily underestand Functions and use it daily;

OldUsr_mode:mean user has age from (+3Year to -10Year) && (+40year to -100year)
OldUsr_mode:in this mod we use Functions[PhysicalButton, Led, Vibration, QuickSound(Len<3sec),MechanicalSound];
OldUsr_mode:user can easily underestand Functions and use it daily;

SSG(SuperSmartGUI) in Mobile Devices has double mod and user easyly can switch betttwen YoungUsr_mode & OldUsr_mode or use both in synchorized;

///[DesktopDev]///////////////////////
SSG for Desktop Devices [PC, Laptop]
In this senario we have a GUI can undestand user behavior and User faviorites and user activity(Job,ToDo,etc) and Exec User Command's Just By a Simple Button/Action;
so all worldwide/worldlevel user has age from (+3Year to -10Year) && (+40Year to -100year) cand easily work with PC or Laptop;
LifeIsBeutiful

Example(1)
{
  ///SimpleExample
  ///System Seach From User Behavior by Date and found it,then run it, full automatic/automcion
  ///
  _DATE="Friday";
  UsrFavLst = Query("SELECT * FROM UserBehaviorHistory WHERE date=${_DATE}");
  ToDO()
  {
   foreach (UsrFav in UsrFavLst)
    {
    UsrFavTable = Fetch_Table_Content(UsrFav);
    UsrBehaviorAttribute = Fetch_Att_Content(UsrFavTable);
    Res=Query("Select ${UsrFav} FROM ${UsrFavTable} where Flaq=${UsrBehaviorAttribute}"]);
      ///Exp::Query="Select Email FROM Emailes where Flaq=No-Spam];
    STD_OUT<<Res;  
    Exec(STD_IN);
    }
  }
    
}




