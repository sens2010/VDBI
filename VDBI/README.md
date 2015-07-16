# VDBI
A data transfer protocol which will change the resource description and data transport.   
     Just like other thing in data transfter, a resource should have themselves description. And the resource should be described by itself. In this area, RDF description maybe an excellent choice, and RDF also defined a lot of schema to describe the resource.     
     But, the user always wanna to get resouces in code-approaching, so the description should be easy encode an decode. So a data transfer protocol which just like OData and so on, should be used more frequently. On the other hand, those data protocol just defined the data format and operator, And has a little information about the description of the data. So, our group decide to develop a new data transfer protocol. The protocol will base on the RDF description style, and also give a tide expression for user to get. We call it VDBI, for the reason that it maybe first use in VDB(Virtual Database) data transfer. At first, we define it feature as follow:  
     1.Resource type, include container, file, connector, record and so on. The container can enclude the subresource, and diffrent type may defined diffrent type;  
     2.Attribute type, it include the type where we could form the characters in our type. For example, we defined name, even type in the attribute.  
     3.Service type, it just make a enclusion cover for the invoking relation to data. The service type could provide a uniform service call to user;  
     4.Data type, it defined the type of the data in each attribute, it has the common type in the other programming language, so we could transfer the data to the language we like;  
     5.User defination, the user could use the type of vdbi to state their service and resource. For example, we could use it to description the  data in our database table.  
     For the continue the program, we regist a website(http://www.vdbi.org, some reason, it still under construction) to inform the more detail. Anyone who convey the vdbi protocol could tranfer data themselves, and the proxy and buffer may be a good choice to improve the data service. We realize the almost function of vdbi, and ultilize it transfer data in VDB. Some people may be have trouble in RDF, so we give a compatible version called VDBILite.  
```flow
st=>start: 用户登陆
op=>operation: 登陆操作
cond=>condition: 登陆成功 Yes or No?
e=>end: 进入后台

st->op->cond
cond(yes)->e
cond(no)->op
```