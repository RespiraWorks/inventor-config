## Threads in Inventor

When you make threads in a hole, Inventor by default just makes a stand-in object that may be rendered as threads. This is fine for modeling existing parts, but if the intention is to make a 3d-printable object that has actual threads for inserting a bolt, a pneumatic fitting or a sensor, such a model will not produce the physical threads.

### Installing threadModeler

To generate real threads in your models you need to install threadModeler. 

Assuming you have an Autodesk account with your @respira.works email, you should be able to download the following plugin: [coolOrange threadModeler](https://apps.autodesk.com/INVNTOR/en/Detail/Index?id=2540506896683021779&appLang=en&os=Win64&autostart=true).

Right-click on the downloaded '.msi' and chose "Install".

Please note that it may not have yet been ported to the newest version of Inventor. You may need to "hack" this plugin to get it working. The solution is posted in the comments section by a user Alicia Clark. Making a copy here just in case the forum post gets lost or is hard to find:

Open 
`c:\ProgramData\Autodesk\ApplicationPlugins\coolOrange_threadModeler.bundle\Contents\coolOrange.ThreadModeler.Inventor.addin`
and find a line that contains `<SupportedSoftwareVersionLessThan>`.

Change this line:
```
<SupportedSoftwareVersionLessThan>25..</SupportedSoftwareVersionLessThan>
```
to something this (might need to go higher depending on version of Inventor):
```
<SupportedSoftwareVersionLessThan>27..</SupportedSoftwareVersionLessThan>
```

Restart Inventor, and it should load!

Note: if you cannot see the `c:\ProgramData` folder, go to `Control Panel`, then `Appearance & Personalization`, then `Folder Options`. Click the `View` tab and make sure the bullet that says `Show Hidden Files & Folders` is selected. After you click `Apply` the `c:\ProgramData` folder should show up.

Additional note: It might still not appear in the navigation panel. In which case, go to `Tools->Add-Ins` and manually change the default mark `Blocked` to `Load Automatically`.

### Using threadModeler

You will find tutorials on how to use theadModeler on Youtube. The general gist is that you must model a hole using the **MAJOR** radius of the threads you intend to have. This is because threadModeler always builds threads out from the edges, rather than cutting them into the solid. If you use a smaller radius, you will have inadvertently "clogged up" the threads that will be generated. Inventor's "Hole" tool is notorious for doing whatever it wants to do. It is always safer to make your own sketch and extrude the hole to precisely the radius you need.

#### Modeling tapered threads

A special case of this is modeling tapered threads, such as NPT. You should create your own tapered hole using an initial diameter and pitch angle. You may want to look up thread definitions in the Inventor-supplied `threads.xls` or consult something like [this page](https://amesweb.info/Screws/NPT-Thread-Chart.aspx), which also links to a [calculator tool](https://amesweb.info/Screws/npt-thread-calculator.aspx) that provides more of the parameters defined in the drawing.

Note that "external threads" refers to those on the male interface, while the "hand-tight" and "wrench makeup" parameters refer to dimensions that apply to the female interface.

Check your thread fit by attempting to interface the components in assembly with cross-section view.
