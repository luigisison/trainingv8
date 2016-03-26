#Technical Training Outline

##Day 1
* Install Odoo
* Reference: [Command Line Interface - odoo.py] (https://www.odoo.com/documentation/9.0/reference/cmdline.html)
* ORM architecture
* ORM API
* MVC - Configuration options
* Odoo Folders

##Day 2
* Reference: [Building a Module] (https://www.odoo.com/documentation/9.0/howtos/backend.html)
* Modules
* Object - Base, Computed and Relational Fields
* Reference: [Views] (https://www.odoo.com/documentation/9.0/reference/views.html)
* Action
* Menu

##Day 3
Environment - ORM API
Decorators
ORM Methods - Create, Write
Relational Fields - One2many, Many2one,
Inheritance - Model, View
Domain
onchange
Compute fields

##Day 4
Reference: [Workflows] (https://www.odoo.com/documentation/9.0/reference/workflows.html)
  Activities, Transitions
Buttons - Status buttons
Change attributes depending on 
impt: Reporting
 Qweb - https://www.odoo.com/documentation/9.0/reference/qweb.html
 Qweb Reports - https://www.odoo.com/documentation/9.0/reference/reports.html
impt: Wizards
Chatter - Thread messaging

##Day 5
Security - Levels - User Login, Groups, Record Rule, Access Control List (ACL)
Website - js folder, main layout
Translation - Gengo module (gengo.com), Transifex (https://www.transifex.com/)
Import/Export
Web Services
XML-RPC (Web Service API) - https://www.odoo.com/documentation/9.0/api_integration.html
ref: OERPLib - https://pythonhosted.org/OERPLib/; Jigar's site - , ERPpeek https://github.com/tinyerp/erppeek

Server Actions ir.actions.server
Documentation in Actions https://www.odoo.com/documentation/9.0/reference/actions.html
Menu - Automated Actions
Install: Base import module

Scheduled Actions - a type of Cron
Example: Run server action 324
  Object = ir.actions.server, Method=run, Arguments [324], mimimum Interval Unit = 1 hour
  
Company Properties - Specify value of a field for a company

View Types: Kanban, Calendar, Graph, Pivot, Search
Reference: https://www.odoo.com/documentation/9.0/reference/views.html
Define view in ir.iu.view
Add view in ir.actions.act_window.view_mode

Add in module_views.xml
compound search: filter_domain="['|', ('name, 'ilike', self), ('notes','ilike', self)]

<separator/> #filters within the same separator define an OR operation
<filter string="New Sessions" domain=[('state' ,"=","new")]
<filter string="Open Sessions" domain=[('state' ,"=","open")]
<separator/> #new separator defines an AND operation
<filter string="Rejected Sessions" domain=[('state' ,"=","refect")]

Upcomihg Sessions under Filter dropdown
<filter string="Upcoming Sessions" domain="start_date >+ datetime.datetime.now().strftime('%Y-%m-%d') + ' 00.00:00')]/>

Course under Group By dropdown
```xml
<group expand="0" string="Group By"/>
   <filter name'"course" domain="[]" string="Course" context={'group_by' : 'course_id'}/>```
   
Default filter
Add <filter name=
in ir.actions.act_window, add 








