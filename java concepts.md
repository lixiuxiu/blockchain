# JavaServer Faces（JSF） 

定义：JavaServer Faces (JSF) 是一种用于构建Java Web 应用程序的标准框架。它提供了一种以组件为中心的用户界面（UI）构建方法，从而简化了Java服务器端应用程序的开发。

典型的JSF应用程序包含下列部分：

- 一组JSP页面
- 一组后台bean（为在一个页面上的UI组件定义的属性和函数的JavaBean组件）
- 应用程序配置资源文件（定义页面导航规则、配置bean和其它的自定对象，如自定义组件）
- 部署描述文件（web.xml）
- 一组由应用程序开发者创建的自定义对象（有可能）
- 一些可能包含自定义组件、约束、转换器或者监听器的对象
- 为在页面中表现自定义对象的一组自定义tag



# POJO

POJO是Plain OrdinaryJava Object的缩写，但是它通指没有使用Entity Beans的普通java对象，可以把POJO作为支持业务逻辑的协助类。



# Enterprise Java Beans（EJB）

EJB是sun的JavaEE服务器端[组件模型](https://baike.baidu.com/item/%E7%BB%84%E4%BB%B6%E6%A8%A1%E5%9E%8B)，设计目标与核心应用是部署分布式应用程序。简单来说就是把已经编写好的程序（即：类）打包放在服务器上执行。



#  Java EE环境与J2SE环境   

Java EE环境与J2SE环境。因为在本章后面的学习中要经常提到这两个概念，所以读者一定要先理解它们，为以后的学习打好基础。    

— Java EE环境，包括EJB容器和Web容器。   

（1）Web容器：只运行Web应用的容器，例如Tomcat就是开源的Web容器，它可以运行JSP、Servlet等。   （2）EJB容器：运行在EJB组件的容器，提供EJB组件的状态管理、事务管理、线程管理、远程数据资源访问、连接管理和安全性管理等系统级服务。例如JBoss为EJB容器和Web容器（Web容器是集成了Tomcat）结合。   

部署在EJB容器中的JAR包都可以认为是运行在EJB容器中。但JBoss中的Web应用，比如war包中的类就不是运行在EJB容器中，而是运行在Web容器中。   

— J2SE环境   

最普通Java运行环境，例如一个HelloWorld的Java程序就是运行在J2SE的环境中，通常使用main入口方法作为程序启动的触发。   

# 两种类型的EntityManager对象   

根据EntityManager对象的管理方式，可以有以下两种类型。   

— 容器托管的（container-managed）EntityManager对象   容器托管的EntityManager对象最简单，程序员不需要考虑EntityManager连接的释放，以及事务等复杂的问题，所有这些都交 给容器去管理。容器托管的EntityManager对象必须在EJB容器中运行，而不能在Web容器和J2SE的环境中运行。本书前面讲述的 EntityManager对象都是通过注入 @PersistenceContext注释来获得的，其实，这种获得EntityManager对象的方式就是容器托管的。   

— 应用托管的（application-managed）EntityManager对象   应用托管的EntityManager对象，程序员需要手动地控制它的释放和连接、手动地控制事务等。但这种获得应用托管的 EntityManager对象的方式，不仅可以在EJB容器中应用，也可以使 JPA脱离EJB容器，而与任何的Java环境集成，比如说Web容器、J2SE环境等。所以从某种角度上来说，这种方式是JPA能够独立于EJB环境运 行的基础。 