Here is a useful compilation from various website for the search difference between volatile and synchronized.

-   If you are working with multi-threaded programming, the volatile keyword will be more useful. When multiple threads using the same variable, each thread will have its own copy of the local cache for that variable.

-   So, when it’s updating the value, it is actually updated in the local cache not in the main variable memory. The other thread which is using the same variable doesn’t know anything about the values changed by the another thread.

-   To avoid this problem, if you declare a variable as volatile, then it will not be stored in the local cache. Whenever thread are updating the values, it is updated to the main memory. So, other threads can access the updated value.

-   Synchronized method affects performance more than a volatile keyword in Java.

-   You cannot synchronize on the null object but your volatile variable in Java could be null.

-   Since volatile keyword in Java only synchronizes the value of one variable between Thread memory and "main" memory while synchronized synchronizes the value of all variable between thread memory and "main" memory and locks and releases a monitor to boot.

![Java Variables]({{ "/assets/images/java-post-img/java-volatile.png" | absolute_url }})

Difference between Volatile and synchronized Keyword is very popular java question asked in Multithreading and concurrency interviews. Here are few differences listed down :

(1) Volatile in java is a keyword which is used in variable declaration only and cannot be used with method. We will get compilation error if using volatile with method.

Syntax to use volatile with variable:

volatile Boolean flag ;

While synchronization keyword is used in method declaration or can be used to create synchronization blocks. We will get compilation error if we define variables as synchronized

How to use Synchronized method and Synchronized block

Synchronized method:<br/>
synchronized void executeMethod(){<br/>
//write code inside synchronized method<br/>
}<br/>

Synchronized block:<br/>
void executeMethod(){<br/>
synchronized (this)<br/>
{<br/>
//write code inside synchronized block<br/>
}<br/>
}<br/>

(2) Volatile variables read values from main memory and not from cached data so volatile variables are not cached whereas variables defined inside synchronized block are cached.

(3) Volatile variables are lock free which means that it does require any lock on variable or object whereas synchronized requires lock on method or block .

(4) Volatile variable can be null whereas we will get NullPointerException in case we use null object.

(5) As volatile never acquires any kind of lock ,so it will never create deadlock in program. But in case of synchronized we might end up creating deadlock if synchronization is not done properly.

(6) Synchronized keyword may cause performance issue as one thread wait for another thread to release lock on shared object whereas volatile variable is lock free and hence is not much expensive in terms of performance.

(7) Using synchronization thread can be blocked when waiting for other thread to release lock but not in the case of volatile keyword.

(8) Volatile keyword is suitable When there is an independent value to be share among multiple threads like counter and flag.
Whereas synchronization is used in the scenario where we are using multiple variables very frequently and these variables are performing some calculation.
