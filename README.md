# Model

Tot objecte hauria de tenir un Unic Identifier. (gid=> Global Id)

Arquitectura amb PrivaliaObject amb gid, i fer que totes les classes heredin d'aquí.
Per generar el UUID, es pilla de java.util.UUID.randomUUID()


## Constructors
constructor de classes (Inicialitzador static)
> Es single thread.
>
> S'executa el primer cop que s'accedeixi a la clase. Sigui per crear un objecte nou o per accedir a un metode static

constructor d'objecte


#Java

En Java Web, tenim variables d'applicació, son variables que conté el servidor web. 

## Compilats Java
- jar
- war
- ear
- apk

## Interficies

Té l'interficia clonnable, que permet clonar l'objecte.

Java8 permet metodes statics dins de les interficies. (i implementar-los max. 1 d'objecte i d'estatic)

### Interficies funcionals
Poder afegir implementacions a les interficies. Exemple: Runnable

Han d'incloure un metode abstracte com a mínim. 
Per implementar el metode, s'ha de ficar la paraula reservada default.


## Classpath
afegir les coses que han de ser facils per localitzar

## Anotacions
Es creen amb @interface.
Poden tenir atributs amb default values.


Es poden applicar anotacions a la mateixa anotació

## Inicialitzadors statics
No poden llençar "unmanaged exceptions", això implica que s'ha de fer un wrapping the l'excepció llençada.  (Checked vs unchecked exceptions)


## Try with resources
A partir de java 8, es poden utilitzar el try with resources, sempre i quant l'objecte tingui implementada l'interficie closable

## Try catch ours
Catch té la opcio de ficar opcional. 

## Futurable
Classes per portar les promeses aquí. 

#JUnit

Té la funcionalitat d'"expected exception" per validar que s'esta llençant una excepció

# Maven

## Run concrete tests
Testeja una clase
> mvn test -Dtest=$classNameTest 

Testejar un metode
>mvn test -Dtest=$className#$functionName

Testejar una categoria
> mvn test -Dtest.categories=slowTests

Es classifica com:
```
@Category(SlowTest.class)
@Test
public void b(){

}
```

## Archetipes
Manera de generar una estructura de la nostra infraestructura. 


## Useful things Maven:
[Phases maven](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)

mvn clean install -U

Borrar la cache:
mvn dependency:purge-local-repository clean install -U

## Scopes
test: per testing
provided: Perque utilitzi la que et proporcioni. 

## Settings
settings.xml > permet configurar el mvn. 


# Log4J
Tutorial:
https://www.adictosaltrabajo.com/tutoriales/log4j/

PropertyConfigurator.configure <= permet indicar on esta i com es diu el fitxer de configuració de log4j

# Spring

## Jerarquia de carpetas

Por estructura de proyecto, las dependencias se autoinyectan por la jerarquia de carpetas

## Log
Per fer el log, spring utilitza una façana per encapsular la majoria de frameworks de logs. Aquesta es diu slf4j

spring-boot per defecte utilitza logback, però spring-data amb hibernate utilitza log4j

# Spring-boot

[spring boot initializr](http://start.pring.io)

# Altres

## Lombock
@Data en el objecte, et proporciona getters and setters, el constructor el equals, el canEquals, hashcode y el toString

Dona una anutació segons el framework de log que necessitis.

## POJOS
Plain old Java Objects

## Reflexión
Spring utilitza "Reflexión" en català, introspecció.