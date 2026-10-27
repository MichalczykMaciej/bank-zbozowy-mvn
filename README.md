# bank-zbozowy-mvn
[ERROR] Tests run: 6, Failures: 1, Errors: 0, Skipped: 0, Time elapsed: 0.048 s <<< FAILURE! -- in put.io.selenium.atm.AtmCardInfoTest
[ERROR] put.io.selenium.atm.AtmCardInfoTest.testTryPinCorrect -- Time elapsed: 0.009 s <<< FAILURE!
java.lang.AssertionError: PIN 1525 powinien zostać zaakceptowany expected:<true> but was:<false>
	at org.junit.Assert.fail(Assert.java:89)
	at org.junit.Assert.failNotEquals(Assert.java:835)
	at org.junit.Assert.assertEquals(Assert.java:120)
	at put.io.selenium.atm.AtmCardInfoTest.testTryPinCorrect(AtmCardInfoTest.java:33)
	at java.base/java.lang.reflect.Method.invoke(Method.java:580)


Co dokładnie zawiodło? Zawiodła faza uruchamiania testów. 
Pobieranie narzędzi powiodło się, kod poprawnie się skompilował, 
ale proces zatrzymał się na testach, 
co zapobiegło zbudowaniu wadliwego artefaktu w fazie pakowania.   
Dlaczego poprawna składniowo zmiana spowodowała błąd? 
Ponieważ CI weryfikuje nie tylko to, czy kod został poprawnie napisany pod kątem języka Java, 
ale przede wszystkim sprawdza, czy działa zgodnie z zaprogramowaną logiką biznesową. 
Zmiana PIN-u naruszyła reguły, które testy miały za zadanie chronić.
