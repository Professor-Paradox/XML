# Introduction
* XML stands for eXtensible Markup Language.

**Extensible:**      
EXtensible means the developer,user can use this language as they see fit,for different purposes.     
XML doesn't have predefined tags,Just few rules and Guidelines.    

**Markup:**    
Enclosing the data between two tags,opening and close tag.      
Ex:`<name>data</name>`     

**Language:**     
XML was desinged to be an independent language for multiple software and hardware platforms.    
* Was created to store and transport data over the web.    
* XML is similar to HTML,Human and Machine readable.      
* It designed to be  self-discriptive.
* XML doesn't do anything,just stores data inside tags.
* XML documents can be used as text based databases.
* We send the data in xml format and then process our programming logic on it.
* We can use the xml document to create objects from our data,or create xml document from objects in our programming language like java,python.  
* XML specification was given by [**W3C**](https://www.w3schools.com/).    

## WebServices
* Webservices are created to provide better communication between multiple languages,platforms over the internet.      
* WebService is a collection of open protocols and standards used for exchanging data between application or systems,We request data with a xml file,and response is sent in a xml file.       
* Recently JSONJ(javascript object notation) is gaining in popularity,but xml is still being used widely.  
* Webservices help in development of other webservices or webapplications
Ex: payment gateway by banks, api for development applications.      
Types of webservices are      
1. **SOAP** webservices        
   SOAP:Simple Objects Access Protocol       
   SOAP was popular for api standard,and xml for data    
   XML is a full fledged language and has many features JSON doesn't have,it is a document markup.And supports metadata.   
2. **RESTFull** webservices    
   REST:REpresentational State Transfer            
   An api is called RESTFull if it follows all guidelines of REST.           
   REST was now new standard for apis,and json for data with it.             
   JSON is purely for structured data interchange,done by taking data directly from objects and other data types.                

## Webapplications
Webapplications are the software used by the end user.  
Webaplications use webservices to operate.    
Example:gmail,outlook,youtube    
A browser is used to access webapplications.    

## XML vs HTML
* XML main purpose was to store data
* HTML was designed to store and display data,it has a layout.
* XML tags are user defined,we can name them what ever we want
* HTML tags are predefined and custom tags are not allowed.
* XML only have a barebones document structure,with guidelines,user have to define their own structure.
* HTML has a well defined structure for elements and data.
* XML document can be updated with new data, without breaking the structure.
* HTML documents tend to be tricky while updating the data. 
* XML stores data in plain text,easy readable.
* HTML has meaningful tags,not as easy as XML
* XML documents form a tree structure that starts at **root** and ends at **leaves**.
* HTML documents form a tree structure starting at **html** root tag.
* Both XML and HTML have data and attributes inside a tag/element.     

## XML Structure
XML have 3 parts
1. Elements
   An element can contain child elements,attributes,text data.       
   Elements in xml [are](#elements-in-dtd)
2. Attributes
   An attribute can be the data inside an element,but it is preferred to keep metadata as attributes     
   Attributes in xml [are](#attributes-in-dtd)
3. Entity reference
   Special symbols.

### XML Prolog    
We prolog to define the document type and Xml version.      
* XML has only one version, 1.0.    
`<?xml version="1.0" encoding="UTF-8"?>`

### Rules
* All xml elements must have a closing tag.
* All xml tags are case-sensitive.
* Elements must be properly nested,other wise data maynot be stored correctly.   
Ex:`<b><i>test</i></b> is valid,`   
   `<b><i>test</b></i> is not valid.`      
* Attributes are present inside the tags if needed.
Ex:`<note date="1990-01-01"><text>test text</text></note>`
* XML document doesn't remove extra whitespace,so every space,tab is stored as data.
* where as Html removes extra white space and treats it as a single space.

### Entity reference:
XML has special meaning to certain characters/symbols,but if we need to use those in our document,we use Entity Reference.    
Entity references are pre-defined alias's for symbols,They are.        
1. < is referenced as  *\&lt;*
2. *>* is referenced as *\&gt;*
3. *&* is referenced as *\&amp;*
4. *'* is referenced as *\&apos;*
5. *"* is referenced as *\&quot;*

### Comments
We use the same syntax for comments in html and xml.      
Syntax:        
`<!-- comments -->`        

### Elements vs Attributes
* Attributes cannot have a tree structure,while elements can.
* Attributes are not expandable,elements are.
* We can have all elements as attributes but it will create non-maintainable structure.
* Use Attributes only to differ between elements
* Good practice is use elements for data,attributes for metadata. 


### Naming conventions
* Give element tags descriptive names
* Except **xml** no element names are reserved.
* element name shouldn't have spaces.
* Avoid, '-','.',':' since some programming languages may subtract,refer an object,search a namespace.
* follow the naming conventions of the programming language,database in use with xml.For better readabily.  
  
| Style      | Example       |
| ---------- | ------------- |
| lowercase  | \<firstname>  |
| uppercase  | \<FIRSTNAME>  |
| underscore | \<first_name> |
| pascalcase | \<FirstName>  |
| camelcase  | \<firstName>  |

### DTD vs XSD
**DTD**     
* DTD document is used to define the structure of xml documents.  
* XML DTD use's SGML(Standard Generalized Mardkup Language)Syntax.
* Some people don't mind it,some people hate it,because it is different from xml syntax.    
* Good to know DTD,Better learn XSD,with new features.

**XSD**        
* Where as XSD uses the XML syntax.  
* XSD supports Namespaces.
* XSD defines order of child elements.
* XSD can be modified using DOM
* XSD is extensible,DTD is not.
* XSD has individual/Custom DataTypes,instead of PCDATA for all characters in DTD.

### Document Type Definition(DTD)   
Document type definition is used to define the structure of xml document.     
With an extension **.dtd**.   
* DTD contains declaration of Elements,Attributes,Entity references.      
  
**Usage**         
1. Internal dtd:
   here we write dtd code inside xml.       
   > `Syntax: <!doctype rootelement [DTD rules]>`    

   > `EXample:<!doctype employee [`      
   > `<!ELEMENT employee (empno,name,salary)>]>`      
   > `<employee><code></employee>`     

   Not reusable.  
2. External dtd:This is of Two types
* Private DTD        
   **Syntax**:`<!DOCTYPE rootelement SYSTEM "dtdfilename.dtd">`     

   A DTD file that is used for a particular application,project it is a private dtd.  
          
* Public DTD         
A DTD file that is not particular for an application,project that can be used any where is a public dtd.          
   **Syntax**:`<!DOCTYPE rootelement PUBLIC "ifisoregister//vendorname//version//language" "DTDfilename.dtd">`       

Here *ifisoregister* is used to specify if this file is registered with *iso standard* if yes "+" is used,if no "-" is      used.       
   *vendorname* is the company name.     
   *version* is the version of document      
   *language* is the language inwhich document is created.       

It is not mandatory to specify anything about the company/version/language/registration.Just used for differentiation.But we have to provide empty quotes to specify,empty data of company.               

#### Elements in DTD
DTD is a document that defines structure for other xml documents.    
We declare the elements structure using element dtd.     
Syntax for element declaration:     
`<!ELEMENT element-name (content-model)>`  

ELEMENTs can have five types of Content-model.     
1. *Text-Only Elements*       
   * Here we use **#PCDATA** to accept text elements.characters and numbers are considered text elements.           
      *PCDATA*:Parsable Character DATA            
> Syntax:`<!ELEMENT employee (#PCDATA)>`       

2. *Child-only Elements*
   * Here we declare the child elements with their respective [cardinality](#cardinality-operator).   
   * all defined child elements need to be present in xml document.
   * pipe(|) operator is used to specify OR relation,i.e, one of the elements should be present,but not both elements.
   * Ex: (empname|salary),the xml document can have either empname or salary not both. 
> Syntax:`<!ELEMENT employee (empname,salary,id)>`

3. *Mixed Elements*  
   * mixed elements are used when we want to have text-only,child-only elements in content-model.
   * When using mixed elements we must follow these rules,
     * Must start with **#PCDATA**,
     * must use OR(|) operator,
     * Must use *\** as cardinality operator.
   * We can have text or child element inside the employee element.we use this occasionally.
>Syntax:`<!ELEMENT employee (#PCDATA|empname|empsalary)*>`

4. *Empty Elements*
   * Empty elements are used to provide metadata,not data.
   * Empty elements shouldn't contain spaces,characters.If it does,then an invalid error is raised.
   * It's preferred to use self closing element tags.instead of opening and closing tag,that can result in errors.
   * Ex: `not this <employee></employee>,prefer <employee />`
>Syntax:`<!ELEMENT employee EMPTY>`

5. *Any Elements*
   * We use ANY to have text,child,mixed,empty elements in our structure.
   * if we want to have child elements inside this ANY element,then they must be declared separately,if not the parser can't find what to do with those elements,when we create. 
   * Ex: `<!ELEMENT empname (#PCDATA)>` to use empname as child of employee.  
>Syntax: `<!ELEMENT employee ANY>`

* If we don't follow the DTD structure,a validation error is raised, then the data won't be transfered successfully.  

#### Attributes in DTD
* Attributes are used to store metadata.They are key-value pairs. 
* Attributes order is not important,they are present inside a opening tag.          
* We can store all attributes as elements,and all elements as attributes.          
* But that breaks our structure and creates unmaintainable document structure .              
* So it is preferred to use Attributes for metadata,elements for actual data.     
* Attributes must be inside single or double quotes.       
* We can use single quote inside double quotes or vice versa.       
Ex: `<name data="test 'data'">`

We can have attributes for all 5 types of elements.
>Syntax:`<!ATTLIST element-name attributename attributedatatype attributespecifier other-information>`   
1. *element-name* is the element that has these attributes.
2. *attributename* is the name of attribute
3. *attributedatatype* is the type of data the attribute can take
   * **CDATA** Character DATA is used to take text input,used only for attributes.  
   * **PCDATA** Parsable Character DATA is used for elements only.   
   * **ENUMERATED** values are used to select from pre-defined options,We can't have new values. 
     * EX:`<!ATTLIST payment payment-method (CASH|CARD|ONLINE) #IMPLIED>`,here we can only use these values,no new values are accepted.Values inside the "()" are enumerated values.  
     * Syntax:`<!ATTLIST payment payment-method (value1|value2|value3) #IMPLIED>`
   * **ID** is used for unique identification,can only use one ID per element.   
     * Can't start with numeric values,doesn't allow special symbols as part of ID.
     * Can start with "_" or alphabets.
     * Ex: `<payment paymentid="V123" />`
     * Syntax:`<!ATTLIST payment paymentid ID #REQUIRED>`---> here ID is unique for each element.   
   * **IDREF** is used to avoid repetition of values,here we take another ID,to use their data.
     * Ex:`payment paymentdid="v123" /> <person pid="v123" />`
     * Syntax:`<!ATTLIST payment paymentid IDREF #REQUIRED>` the value for IDREF is another ID.
   * **IDREFS** are used to have collection of ID's for a single element. A single attribute can have multiple ID values. different ID's are seperated by spaces.   
     * Ex:`<payment paymentids="v123 v456">`
     * Syntax:`<!ATTLIST payment paymentids IDREFS #REQUIRED>`
   * **NMTOKEN** is similar to CDATA,with a few restrictions.  It only allows
     * A-Z,a-z,0-9
     * special characters like (-,_,.) are allowed,rest of the symbols are not allowed.
     * EX:`<payment paymentid="stuff" \>`
     * Syntax:`<!ATTLIST payment paymentid NMTOKEN #REQUIRED>`
   * **NMTOKENS** are same as NMTOKEN but accepts list of values.
     * EX:`<payment paymentsid="stuff stuff"/>`
     * Syntax:`<!ATTLIST payment paymentsid NMTOKEN #REQUIRED>`
   * **NOTATION** is used to create a shortcut for a long text. 
     * EX:`<!NOTATION JPG SYSTEM "IMAGE/JPG">`----->creating a shortcut
     * EX: `<!ATTLIST photo phototype NOTATION (JPG|GIF) #REQUIRED>`---->linking shortcut
     * EX: `<photo phototype="GIF">`---->using shortcut
     * Syntax:`<!NOTATION shortcutname SYSTEM "LONG Value">`
   * **ENTITY** is used to create shortcut for text,just like notation,but can use an entity anywhere.
     * We use custom entities,same as inbuild entity references. 
     * Ex:`<!ENTITY name "somerandomnamethatneedstobeused1000times">`
     * Ex:`<test>&name;</test>`
     * Syntax:`<!ENTITY entity-name "entity data">`
   * **ENTITIES** we can use multiple entities for a single entity.
4. *attributespecifier* is the DTD specifier that gives some conditions 
   * There are some specifiers present in DTD,we can use according to our need.   
   * **#REQUIRED** is a *mandatory* attribute,or an error is raised.      
   * **#IMPLIED** is an *optional* attribute
   * **#FIXED**  is a  *fixed* attribute
     * here the data for the fixed attribute is given.
     * Ex :`<!ATTLIST employee empsalary CDATA #FIXED "1000">`--->this provides the fixed value to entire employee.  
     * We can't override the fixed value in the xml document.We have to use this in our xml document with the same value.    
   * **#default** if we don't give our attributespecifer a value then it is *default*.We have to specify the value of our default attribute. 
     * Ex: `<!ATTLIST employee empCompany CDATA "ibm">`-->this is default for employee
     * We can override the default value by using the attribute name.
   * The **other-information** in syntax is the default values,fixed values.
>Syntax:`<!ATTLIST employee empno CDATA #REQUIRED "some information for fixed/defaul values">`

#### Cardinality operator
In the content-model we can have multiple repetitions of elements,with Cardinality operator.      
There are three cardinality operators.       
1. *\**  :indicates 0 or more 
2. *+*   :indicates 1 or more 
3. *?*   :indicates 0 or 1    
Ex:         
`<!ELEMENT books (book)>      --->can have only one book element`       
`<!ELEMENT books (book*)>     --->can have zero or more book elements`      
`<!ELEMENT books (book+)>     --->can have one or more book elements`        
`<!ELEMENT books (book?)>     --->can have zero or one book element`     

Cardinality operators are used to specify the repetition of elements,child elements. 




### XML Schema Definition(XSD)
Can provide data and structure of a document.  
XML schema definition,with extension XSD 

#### Schema
Schema is the first element of a xsd.




#### Namespaces
Since all the elements are user defined,their will be conflicts when merging different xml documents with same element names.     
To avoid this we use a prefix.This prefix is called a namespace.           
Namespaces avoid ambiguity problems,when ever we use elements,we use fully qualified names.          
We use **xmlns** attribute to define a namespace.     

Syntax:     
xmlns:prefix="uri"      

**Uniform Resource Indentifier** is used to indentify unique internet resource.        
Most used URI is URL **Uniform resource locator** which indentifies internet domain address.    
**Uniform Resource Name** URN is not popular as URL.   

Here the uri is not used for searching data,it is used for unique namespace.        
Generally we use the website domain as the namespace URI.      
Ex:  `<test xmlns:h="uri">`      
With this we can use H to refer to our uri.     
   

We can define the *xmlns* in the prolog of the document,to create a namespace for the entire document.      

In android we use xmlns to differentiate elements from user defined elements.They will be specific to that document.    
Ex:`<xml xmlns:android="google.com"><android:test >`     
in above example the 'android' is used to uniquly indentify test element,their can be another test element but it is different from android:test.     
In above example the android:test is replaced with google.com:test,we use xmlns to shortly identify the URI.         



## XML Usage
XML is just a document with data and structure that is transfered between multiple systems. Their has to be a way to use the data in the logic.Their are multiple way's.They are
### XMLHttpRequest Object
The XMLHttpRequest object can be used to request data from a web server.without reloading the page.
* Update a web page without reloading the page
* Request data from a server - after the page has loaded
* Receive data from a server  - after the page has loaded
* Send data to a server - in the background

This is not a xml element,it used by programming languages like javascript,or backend languages, to send and receive xml data.   

### xml parser
xml parser is used to access and modify the xml document.   
This is done by converting the xml document into xml dom object.  
This is a object for programming use.
XML is just data in plain text,all these methods,objects are how to use the data.   

## XML DOM
DOM is a standard for accessing and modifying documents.
Used to dynamically access,modify,data and structure of the document.   
Markup Languages operate in terms of trees.
So to access that tree in code we use a object of that tree,and access the field,element we want with that object.   
So when we create a object for the html,xml document we can access the data inside with that object.
Syntax:
parser = new Domparser();
xmldoc.getelementbytagname('title')[0].childnode[0].nodevalue;
Here we are taking a dom object of xml document and searching for a node and chagning it's value.

AGain this concept is for programming languages.
We don't use this in xml.  
