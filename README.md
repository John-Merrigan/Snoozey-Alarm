# Snoozey-Alarm

Alarm created in Computer Topics, second semester senior year 2018.


2/6/18 
  Learned about Date Class, DateFormatter Class.
  Converted timeAlarmWillSound to a member of Date Class and used 
  DateFormatter to get only the time with "AM" or "PM" to properly display to the UI
  
SomeDay
  
Absent
  
2/15/18 
  Learned how to use a UI view to present a view inside a different view so I could have a table view in my add edit alarm VC
  Added Start Screen
  Worked on Segues 
  Connected outlets on Wake Up Vc 
  Created alarmFeaturesTableController and embedded in UI View in Add Edit Alarm VC
  Currently getting SIGBORT when I push to AddEdit, I've cleaned up some outlets and segues in Alarm View and 
  add edit alarm      View, Think it must be in the new TableView I created 
  
2/16/18
  Found the Source of the SIGBORT. "'NSInternalInconsistencyException', reason: '-[UITableViewController loadView]                          instantiated view controller with identifier "UIViewController-gZ1-DL-BKf" from storyboard "Main", but didn't get a UITableView.'" Looks liek something is a TVC when it shouldnt be. This was Add Edit Alarm page because I decided to use a seperate UI view to implenent its previous function as a table view. Source Used to fix: https://stackoverflow.com/questions/11535297/how-can-i-change-table-view-controllers-type-to-a-regular-view-controller Going to xml and editing source code fixed
  
  bug: when returning from add edit alarm vc, the tab navigation disappeared from the bottom.
  
  Read up on how to perform an Unwind Segue to preserve state of Alarm Table VC to preserve its memory. Read up on difference between unwind segue and just returning with another push segue. 

  
  *** Terminating app due to uncaught exception 'NSInternalInconsistencyException', reason: 'unable to dequeue a cell with identifier AlarmCell - must register a nib or a class for the identifier or connect a prototype cell in a storyboard'
  
    Think this has something to do with preserving state of Alarm Table VC and returning.
  
