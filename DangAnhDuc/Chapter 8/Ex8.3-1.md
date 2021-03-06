# Chapter 8 - Section 3 - Exercise 1

We have 4 clauses:
- a: curTemp < dTemp - thresholdDiff    
- b: Override  
- c: curTemp < overTemp - thresholdDiff  
- d: timeSinceLastRun > minLag  

And 2 predicates:
- p1: (a || (b && c) && (d)
- p2: b

```java
import org.junit.Test;
import static org.junit.Assert.*;
import java.io.*;
import java.util.*;
public class Test_Thermostat
{
	@Before
	public void init(){
		Thermostat ts = new Thermostat();
		ProgrammedSettings s = ProgrammedSettings();
	}

	@Test
	public void test_PC_true(){
		s.setSetting(Period.MORNING, DayType.WEEKDAY, 69);
    	ts.setPeriod(Period.MORNING);
    	ts.setDay(DayType.WEEKDAY);

    	//clause a
    	ts.setCurrentTemp(63);
    	ts.setThresholdDiff(5);

    	//clause b
    	ts.setOverride(true);

    	//clause c
	    ts.setOverTemp(70);

	    //clause d
    	ts.setMinLag(10);
    	ts.setTimeSinceLastRun(12);

    	assertTrue(ts.turnHeaterOn(s));
	}

	// Test each predicate to false to satisfy PC.
	public void test_PC_false(){
		s.setSetting(Period.MORNING, DayType.WEEKDAY, 69);
    	ts.setPeriod(Period.MORNING);
    	ts.setDay(DayType.WEEKDAY);

    	//clause a: false
    	ts.setCurrentTemp(63);
    	ts.setThresholdDiff(15);

    	//clause b: false
    	ts.setOverride(false);

    	//clause c: false
	    ts.setOverTemp(55);

	    //clause d: false
    	ts.setMinLag(20);
    	ts.setTimeSinceLastRun(15);

    	assertFalse(ts.turnHeaterOn(s));
	}
}
```
