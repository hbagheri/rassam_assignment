# rassam_assignment
A Sample python/postgres project for rasam no framework
<p>First of all create a virtual enviromnent in your path</p>

<code>python3 -m venv /path/to/new/virtual/environment</code>
<p> Activate yout environment </p>
<code>source /path/to/new/virtual/environment/bin/activate </code>

<p> pip install sqlalchemy and pandas </p>
<code>pip install SQLAlchemy</code>
<code>pip install pandas</code>

<p> also apt install postgresql and pgadmin4 and config your database <p>
<p> schemas is contains 9 tables a single view a function 2 triggre function a single view cintains 3 insted action trige for insert, update and delete</p>
<p> I have used a table for main data that almost of columns have integer type but another table to define each column value to it's persian and englishcontain</p>
<p> I used this method becaues i found that almost fields value are reapeating several times so ths mtod saves space and also for example in country field if youtranslate 
	Iram to ایران this value will set to all old and new columns as same. Also a have adde translate for all other fields</p>
<p> all insertsr,update,select and deletes shoud apply in adult_data view it will translate to integer value in adult_data_data table. any new value of country names relations and ....
	will automatically adds to related table and you can add it's translate in pr_name column of the table</p>

<h2>! IMPORTANT ! </h2>
	
<p>after installing environment and requaired modules please apply the database.sql into your postgresql(I had not enogh time to create a well migration for vew, triggers and functions)
so all requaire tables, view and trigges will create and db side will e ok</p>

<h2> Usage </h2>
<p>after installing modules, postgresql,pgadmin4 and creating database and its tables,view and triggers just go to <b>Models.py</b> in root and set your db connection information in the begin af <u>dbo</u> Class</p>
<p> simply run </p>
<code> python3 adult_data.py<code>
	<p> if everythings was ok a menu will shown in cli terminal </p>
<ul>
	<li>Adult Data</li>
	<li>Edudations</li>                                                                                                                                                 
  <li>MaritalStates</li>                                                                                                                                              
  <li>Contries</li>                                                                                                                                                   
  <li>Occupations</li>                                                                                                                                                
  <li>Races</li>                                                                                                                                                      
  <li>RelationShips</li>                                                                                                                                              
  <li>Work Classes</li>                                                                                                                                               
  <li>exit</li>
	</ul>
	<h3>Adult Data</h3>
	<p>This items shows all Main actions of programs<p>
	<ul>
	<li>New</li>                                                                                                                                                        
  <li>Index</li>                                                                                                                                                      
  <li>View</li>                                                                                                                                                       
  <li>Update</li>                                                                                                                                                     
  <li>Delete</li>                                                                                                                                                     
  <li>Upload CSV</li>                                                                                                                                                 
  <li>Back</li>
	</ul>
	<h4>new</h4>
	<p>ascks fields columns one by one and you can add new record manually.Attention that you do'not needs to convert names to numbers as it will save on adult_data_data,
		The software aoutomaticaly searchs for each value and uses its related number even if the value is new, it will add to related table and new numerical value will set in main table</p>
	<h4>Index</h4>
	<p>Ascks for begin and count (default values are 1,10), and shows some columns</p>
	<h4>View</h4>
	<p>Ascs a row id(Table Primary key) to show a single record</p>
	<h4>Update</h4>
	<p>Ascs a row id(Table Primary key) then shows int's columns values one by one to change any one, if any coluns leaves it will not changes</p>
	<h4>Delete</h4>
	<p>Ascs a row id(Table Primary key) then deletes that</p>
	<h4>Upload CSV</h4>
	<p>Gets a csv file path and inserts all rows into database,adds new names and so...</p>
	<h4>Back</h4>
	<p>returns to Previous menu</p>
	<h4>All Other main menus</h4>
	<p> all other menus conains Edudations,MaritalStates,Contries,Occupations,Races,RelationShips,Work Classe has same submenus contains Index,View and Update that works exactly as
		Adult Data menus</p>
	<h4>Existin Bug</h4>
	<p> By the way ther is a bug in reading CSV all columns should hav trim befor inserting into database i may resolve it in the next commit<p> 
