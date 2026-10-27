# bank-zbozowy-mvn
[ERROR] Tests run: 6, Failures: 1, Errors: 0, Skipped: 0, Time elapsed: 0.048 s <<< FAILURE! -- in put.io.selenium.atm.AtmCardInfoTest
[ERROR] put.io.selenium.atm.AtmCardInfoTest.testTryPinCorrect -- Time elapsed: 0.009 s <<< FAILURE!
java.lang.AssertionError: PIN 1525 powinien zostać zaakceptowany expected:<true> but was:<false>
	at org.junit.Assert.fail(Assert.java:89)
	at org.junit.Assert.failNotEquals(Assert.java:835)
	at org.junit.Assert.assertEquals(Assert.java:120)
	at put.io.selenium.atm.AtmCardInfoTest.testTryPinCorrect(AtmCardInfoTest.java:33)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)

