Difference between DTO, VO, POJO, JavaBeans?

<b>DTO</b>   - Data transfer objects are just data containers which are used to transport data between layers and tiers.
        It mainly contains attributes. You can even use public attributes without getters and setters.
        Data transfer objects do not contain any business logic.
        DTO was mainly used to get data transported across the network efficiently, it may be even from JVM to another JVM.
        DTOs are often <i>java.io.Serializable</i> - in order to transfer data across JVM.

<b>VO</b>    - A Value Object represents itself a fix set of data and is similar to a Java enum.
        A Value Object's identity is based on their state rather than on their object identity and is immutable.
        A real world example would be Color.RED, Color.BLUE, SEX.FEMALE etc.

<b>POJO</b>  - POJO stands for “Plain Old Java Object”.
        It’s a pure data structure that has fields with getters and possibly setters, and may override some methods from Object (e.g. equals) or some other interface like Serializable, but does not have behavior of its own.

<b>Bean</b>  - The POJO class that have a public default constructor and must implement Serializable.
