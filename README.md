# Lab-8_202001070

# Student Name - Samay Deepak Ashar
# Student ID - 202001070


### 3. Test the Boa class:

#### Code:

~~~
package JUnit_Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(!jen.isHealthy());
	    assertTrue(ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		// Test when cage length is less than boa length
	    assertTrue(jen.fitsInCage(4));
	    assertFalse(ken.fitsInCage(5));
	}
}
~~~

#### Explanation:

We first import the necessary JUnit classes and the Boa class we want to test.
We then create two Boa objects in the setUp() method. One is a healthy Boa and the other is an unhealthy one.
In the testIsHealthy() method, we test the isHealthy() method of both Boa objects. We expect the healthy Boa to be healthy and the unhealthy Boa to be unhealthy.
In the testFitsInCage() method, we test the fitsInCage() method of both Boa objects. We expect the healthy Boa to fit in a cage of length 4 and the unhealthy Boa not to fit in a cage of length 5.
We use the assertTrue() and assertFalse() methods to make assertions about the expected results of the methods being tested.

### 4. Modifying the set-up method

#### Code:

~~~
public class BoaTest {

    private Boa jen;
    private Boa ken;

    @Before
    public void setUp() throws Exception {
        jen = new Boa("Jennifer", 2, "grapes");
        ken = new Boa("Kenneth", 3, "granola bars");
    }

    // test methods go here
}
~~~

#### Explanation
This creates two Boa objects named jen and ken with different values for their name, length, and favorite food properties. The jen object has a name of "Jennifer", a length of 2 feet, and a favorite food of "grapes". The ken object has a name of "Kenneth", a length of 3 feet, and a favorite food of "granola bars". The private fields jen and ken are added to the BoaTest class so that they can be accessed in the test methods.


### 5. Test Subs:

Part 1: Both the lengths are less than the cage length

#### Code:

~~~
package JUnit_Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(!jen.isHealthy());
	    assertTrue(ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		// Test when cage length is less than boa length
	    assertFalse(jen.fitsInCage(1));
	    assertFalse(ken.fitsInCage(2));
	}
}
~~~

![lab8_1](https://user-images.githubusercontent.com/123536462/233048809-08c4a047-81e6-4177-bfd3-84baec6f47ce.PNG)

Part 2: Both the lengths are equal to cage length

#### Code:

~~~
package JUnit_Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(!jen.isHealthy());
	    assertTrue(ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		// Test when cage length is less than boa length
	    assertFalse(jen.fitsInCage(2));
	    assertFalse(ken.fitsInCage(3));
	}
}
~~~

![lab8_2](https://user-images.githubusercontent.com/123536462/233049221-2aeaf214-0cc1-4022-be78-16d8f5c68eee.PNG)

Part 3: Both the lengths are greater than the cage length

#### Code: 

~~~
package JUnit_Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(!jen.isHealthy());
	    assertTrue(ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		// Test when cage length is less than boa length
	    assertFalse(jen.fitsInCage(4));
	    assertFalse(ken.fitsInCage(5));
	}
}
~~~

![lab8_3](https://user-images.githubusercontent.com/123536462/233049572-e23cb1dd-70b4-42fe-96df-888f12db2552.PNG)


### 6.

#### Code: 

~~~
package JUnit_Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(!jen.isHealthy());
	    assertTrue(ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		// Test when cage length is less than boa length
	    assertFalse(jen.fitsInCage(4));
	    assertFalse(ken.fitsInCage(5));
	}
}
~~~

![lab8_3](https://user-images.githubusercontent.com/123536462/233049572-e23cb1dd-70b4-42fe-96df-888f12db2552.PNG)

Here we will have to change the assertsFalse to assertsTrue for the test case to pass.

#### Code: 

~~~
package JUnit_Testing;

import static org.junit.Assert.*;

import org.junit.Before;
import org.junit.Test;

public class BoaTest {
	private Boa jen;
	private Boa ken;

	@Before
	public void setUp() throws Exception {
		jen = new Boa("Jennifer", 2, "grapes");
		ken = new Boa ("Kenneth", 3, "granola bars");
	}

	@Test
	public void testIsHealthy() {
		assertTrue(!jen.isHealthy());
	    assertTrue(ken.isHealthy());
	}

	@Test
	public void testFitsInCage() {
		// Test when cage length is less than boa length
	    assertTrue(jen.fitsInCage(4));
	    assertTrue(ken.fitsInCage(5));
	}
}
~~~

![lab8_4](https://user-images.githubusercontent.com/123536462/233049945-f33247cd-13ee-453d-9edc-49645b22ef1a.PNG)

### 7.

~~~
private Boa ken;
private Boa jen;

@Before
public void setUp() throws Exception {
    jen = new Boa("Jennifer", 6, "granola bars");
    ken = new Boa("Kenneth", 8, "mice");
}

@Test
public void testIsHealthy() {
    assertTrue(jen.isHealthy());
    assertFalse(ken.isHealthy());
}

@Test
public void testFitsInCage() {
    assertTrue(jen.fitsInCage(7));
    assertFalse(ken.fitsInCage(6));
}

@Test
public void testLengthInInches() {
    assertEquals(jen.lengthInInches(), 72);
    assertEquals(ken.lengthInInches(), 96);
}
~~~

#### Explanation
After adding the lengthInInches() method to the Boa class, I can write a test case to verify its implementation in the BoaTest class. The test case should compare the expected result with the actual result from invoking the method on both the jen and ken objects. The expected length in inches for a Boa with a length of n feet is n * 12 inches.
