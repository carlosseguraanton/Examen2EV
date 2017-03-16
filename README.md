# Examen2EV
Examen2ev

Para construir el proyecto debemos ejecutar en la consola situándonos en la carpeta del proyecto:
mvn compile

Y para ejecutarlo tendríamos que pegar en el pom.xml del proyacto el plugin:

 <plugin>
  <groupId>org.eclipse.jetty</groupId>
  <artifactId>jetty-maven-plugin</artifactId>
  <version>9.0.5.v20130815</version>
  <configuration>
    <httpConnector>
     <port>9999</port>
    </httpConnector>
    <!--
     <webAppConfig>
       <contextPath>/s4c</contextPath>
     </webAppConfig>
     <connectors>
      <connector
   implementation="org.eclipse.jetty.server.nio.SelectChannelConnector">
        <port>9096</port>
      </connector>
     </connectors>  -->
  </configuration>
</plugin>

Y después ejecutaríamos el comando mvn con el goal jetty:

mvn jetty:run

Pero dependiendo de si queremos usar el servidor web jetty.
