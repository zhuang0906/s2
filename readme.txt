ʲô�ǿ�ܣ�
��ܾ��ǰ��Ʒ����ܻ��ͨ�ù�����ǰ��װ�á���ܵ�ʹ���߾Ͳ�����дͨ�õĹ��ܡ�

��ܵ����ã�
��߿���Ч�ʣ��ܹ��ﵽ�°빦����Ч����


ʲô��MVC
M model  		ģ��
V view   		��ͼ
C controller 	������


struts2����һ����ܣ�������һ��MVC��ܡ�

Ҳ����˵��ʹ����struts2��ܣ�������mvc������ü򵥣���


=====================================================================

�struts2����
a. ����������
	<!-- https://mvnrepository.com/artifact/org.apache.struts/struts2-core -->
	<dependency>
	    <groupId>org.apache.struts</groupId>
	    <artifactId>struts2-core</artifactId>
	    <version>2.5.20</version>
	</dependency>

b. ��web.xml�У�����struts2�ġ�ǰ�˿�������
	<?xml version="1.0" encoding="UTF-8"?>
	<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://java.sun.com/xml/ns/javaee" xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd" version="2.5">
		<filter>
			<filter-name>StrutsPrepareAndExecuteFilter</filter-name>
			<filter-class>org.apache.struts2.dispatcher.filter.StrutsPrepareAndExecuteFilter</filter-class>
		</filter>
		<filter-mapping>
			<filter-name>StrutsPrepareAndExecuteFilter</filter-name>
			<url-pattern>/*</url-pattern>
		</filter-mapping>
	</web-app> 

c. ��com.woniuxy.web.action�У�����һ����������
	public class UserAction {
		public void f1() {
			System.out.println("UserAction.f1()");
		}
	}
	
d. ��src/main/resources�´���struts2�������ļ���struts.xml
	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE struts PUBLIC
		"-//Apache Software Foundation//DTD Struts Configuration 2.5//EN"
		"http://struts.apache.org/dtds/struts-2.5.dtd">
	<struts>
		<package name="default" namespace="/user" extends="struts-default">
			<action name="abc" class="com.woniuxy.web.action.UserAction" method="f1">
			</action>
		</package>
	</struts>
	
	
==================================================================================

struts2����ԭ�����װ棩 ��ͼ���ɣ�

	

