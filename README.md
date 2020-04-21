[itadmin@dlypmcipslave2 job-bnonline-app-sit]$ java -Xms1g -Xmx1g -Xss256k -jar -Dlogstash.address=10.10.106.51:9250 -Denv=dev -Ddev_meta=http://10.10.20.98:8080 target/online-ins-api.jar
2020-04-21 09:59:02.301 2946 [main] INFO  c.c.f.f.i.p.DefaultApplicationProvider - App ID is set to online-ins-api-service by app.id property from /META-INF/app.properties
2020-04-21 09:59:02.328 2973 [main] INFO  c.c.f.f.i.p.DefaultServerProvider - Environment is set to [dev] by JVM system property 'env'.
2020-04-21 09:59:02.567 3212 [main] WARN  c.c.f.a.i.DefaultMetaServerProvider - Could not find meta server address, because it is not available in neither (1) JVM system property 'apollo.meta', (2) OS env variable 'APOLLO_META' (3) property 'apollo.meta' from server.properties nor (4) property 'apollo.meta' from app.properties
2020-04-21 09:59:02.591 3236 [main] INFO  c.c.f.apollo.core.MetaDomainConsts - Located meta server address http://10.10.20.98:8080 for env DEV from com.ctrip.framework.apollo.core.internals.LegacyMetaServerProvider
2020-04-21 09:59:03.011 3656 [main] INFO  o.s.c.a.AnnotationConfigApplicationContext - Refreshing org.springframework.context.annotation.AnnotationConfigApplicationContext@311d617d: startup date [Tue Apr 21 09:59:03 CST 2020]; root of context hierarchy
2020-04-21 09:59:03.415 4060 [main] INFO  o.s.b.f.a.AutowiredAnnotationBeanPostProcessor - JSR-330 'javax.inject.Inject' annotation found and supported for autowiring
2020-04-21 09:59:03.504 4149 [main] INFO  o.s.c.s.PostProcessorRegistrationDelegate$BeanPostProcessorChecker - Bean 'configurationPropertiesRebinderAutoConfiguration' of type [org.springframework.cloud.autoconfigure.ConfigurationPropertiesRebinderAutoConfiguration$$EnhancerBySpringCGLIB$$8b13d9ad] is not eligible for getting processed by all BeanPostProcessors (for example: not eligible for auto-proxying)

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::        (v1.5.8.RELEASE)

2020-04-21 09:59:04.085 4730 [main] INFO  c.a.a.o.api.OnlineInsApiApplication - No active profile set, falling back to default profiles: default
Tue Apr 21 09:59:22 CST 2020 WARN: Establishing SSL connection without server's identity verification is not recommended. According to MySQL 5.5.45+, 5.6.26+ and 5.7.6+ requirements SSL connection must be established by default if explicit option isn't set. For compliance with existing applications not using SSL the verifyServerCertificate property is set to 'false'. You need either to explicitly disable SSL by setting useSSL=false, or set useSSL=true and provide truststore for server certificate verification.
2020-04-21 09:59:25.231 25876 [main] WARN  c.b.m.toolkit.TableInfoHelper - Warn: Could not find @TableId in Class: com.aeonlife.application.onlineins.api.model.vo.CmsNoticeInfoVO.
2020-04-21 09:59:25.231 25876 [main] WARN  c.b.m.mapper.AutoSqlInjector - class com.aeonlife.application.onlineins.api.model.vo.CmsNoticeInfoVO ,Not found @TableId annotation, Cannot use Mybatis-Plus 'xxById' Method.
2020-04-21 09:59:42.925 43570 [main] DEBUG c.a.a.o.a.d.s.S.selectList - ==>  Preparing: SELECT value,label,type FROM sys_dict WHERE (del_flag = ?) ORDER BY type,sort ASC 
2020-04-21 09:59:43.160 43805 [main] DEBUG c.a.a.o.a.d.s.S.selectList - ==> Parameters: 0(String)
2020-04-21 09:59:43.275 43920 [main] DEBUG c.a.a.o.a.d.s.S.selectList - <==      Total: 390
2020-04-21 09:59:54.797 55442 [main] INFO  c.a.a.o.a.s.t.impl.TrackServiceImpl - Tracking url:https://scdata.aeonlife.com.cn/sa?project=default--true--
2020-04-21 09:59:54.996 55641 [main] INFO  c.a.a.o.a.s.t.impl.TrackServiceImpl - 启动神策
2020-04-21 09:59:55.046 55691 [main] WARN  o.s.b.c.e.AnnotationConfigEmbeddedWebApplicationContext - Exception encountered during context initialization - cancelling refresh attempt: org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'shopOrderServiceImpl': Injection of resource dependencies failed; nested exception is org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'vipUserScoreServiceImpl': Unsatisfied dependency expressed through field 'noticeUtil'; nested exception is org.springframework.beans.factory.BeanCurrentlyInCreationException: Error creating bean with name 'noticeUtil': Bean with name 'noticeUtil' has been injected into other beans [vipUserGradeRecordServiceImpl,insOrderServiceImpl,insOrderNpcheckServiceImpl] in its raw version as part of a circular reference, but has eventually been wrapped. This means that said other beans do not use the final version of the bean. This is often the result of over-eager type matching - consider using 'getBeanNamesOfType' with the 'allowEagerInit' flag turned off, for example.
2020-04-21 09:59:55.053 55698 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.056 55701 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.057 55702 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.057 55702 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.058 55703 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.062 55707 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.062 55707 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.063 55708 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.069 55714 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.069 55714 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.070 55715 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.070 55715 [main] WARN  o.s.c.a.AnnotationConfigApplicationContext - Exception thrown from ApplicationListener handling ContextClosedEvent
org.springframework.beans.factory.BeanCreationNotAllowedException: Error creating bean with name 'rabbitConnectionFactory': Singleton bean creation not allowed while singletons of this factory are in destruction (Do not request a bean from a BeanFactory in a destroy method implementation!)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:216)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
	at org.springframework.beans.factory.support.AbstractBeanFactory.getBean(AbstractBeanFactory.java:202)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.retrieveApplicationListeners(AbstractApplicationEventMulticaster.java:235)
	at org.springframework.context.event.AbstractApplicationEventMulticaster.getApplicationListeners(AbstractApplicationEventMulticaster.java:192)
2020-04-21 09:59:55.147 55792 [main] ERROR o.s.boot.SpringApplication - Application startup failed
org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'shopOrderServiceImpl': Injection of resource dependencies failed; nested exception is org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'vipUserScoreServiceImpl': Unsatisfied dependency expressed through field 'noticeUtil'; nested exception is org.springframework.beans.factory.BeanCurrentlyInCreationException: Error creating bean with name 'noticeUtil': Bean with name 'noticeUtil' has been injected into other beans [vipUserGradeRecordServiceImpl,insOrderServiceImpl,insOrderNpcheckServiceImpl] in its raw version as part of a circular reference, but has eventually been wrapped. This means that said other beans do not use the final version of the bean. This is often the result of over-eager type matching - consider using 'getBeanNamesOfType' with the 'allowEagerInit' flag turned off, for example.
	at org.springframework.context.annotation.CommonAnnotationBeanPostProcessor.postProcessPropertyValues(CommonAnnotationBeanPostProcessor.java:321)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1264)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:553)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:483)
	at org.springframework.beans.factory.support.AbstractBeanFactory$1.getObject(AbstractBeanFactory.java:306)
Caused by: org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'vipUserScoreServiceImpl': Unsatisfied dependency expressed through field 'noticeUtil'; nested exception is org.springframework.beans.factory.BeanCurrentlyInCreationException: Error creating bean with name 'noticeUtil': Bean with name 'noticeUtil' has been injected into other beans [vipUserGradeRecordServiceImpl,insOrderServiceImpl,insOrderNpcheckServiceImpl] in its raw version as part of a circular reference, but has eventually been wrapped. This means that said other beans do not use the final version of the bean. This is often the result of over-eager type matching - consider using 'getBeanNamesOfType' with the 'allowEagerInit' flag turned off, for example.
	at org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor$AutowiredFieldElement.inject(AutowiredAnnotationBeanPostProcessor.java:588)
	at org.springframework.beans.factory.annotation.InjectionMetadata.inject(InjectionMetadata.java:88)
	at org.springframework.beans.factory.annotation.AutowiredAnnotationBeanPostProcessor.postProcessPropertyValues(AutowiredAnnotationBeanPostProcessor.java:366)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.populateBean(AbstractAutowireCapableBeanFactory.java:1264)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:553)
Caused by: org.springframework.beans.factory.BeanCurrentlyInCreationException: Error creating bean with name 'noticeUtil': Bean with name 'noticeUtil' has been injected into other beans [vipUserGradeRecordServiceImpl,insOrderServiceImpl,insOrderNpcheckServiceImpl] in its raw version as part of a circular reference, but has eventually been wrapped. This means that said other beans do not use the final version of the bean. This is often the result of over-eager type matching - consider using 'getBeanNamesOfType' with the 'allowEagerInit' flag turned off, for example.
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.doCreateBean(AbstractAutowireCapableBeanFactory.java:585)
	at org.springframework.beans.factory.support.AbstractAutowireCapableBeanFactory.createBean(AbstractAutowireCapableBeanFactory.java:483)
	at org.springframework.beans.factory.support.AbstractBeanFactory$1.getObject(AbstractBeanFactory.java:306)
	at org.springframework.beans.factory.support.DefaultSingletonBeanRegistry.getSingleton(DefaultSingletonBeanRegistry.java:230)
	at org.springframework.beans.factory.support.AbstractBeanFactory.doGetBean(AbstractBeanFactory.java:302)
