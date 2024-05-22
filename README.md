*In Java, logging is an important feature that helps developers to trace out the errors. Java is the programming language that comes with the logging approach.
*To avoid such issues, logging in Java is simplified with the help of the API provided through the package, and the java.util.logging org.apache.log4j.* package.
*The process of creating a new Logger in Java is quite simple. You have to use Logger.getLogger() method. The getLogger() method identifies the name of the Logger and takes string as a parameter. So, if a Logger pre-exists then, that Logger is returned, else a new Logger is created.
*How to users logger
*example code 
```java
*   private static Logger log;
    private static FileHandler file;
    static { 
        try {
            log = Logger.getLogger("log");
            file = new FileHandler("logger.txt",true);
            file.setFormatter(new SimpleFormatter());
            log.addHandler(file);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) { // button function                                        
        try {
            String text = jTextField1.getText();
            System.out.println(Integer.parseInt(text) / 10);            
        } catch (Exception e) {
            log.warning(e.toString());
        }
    }  

    
