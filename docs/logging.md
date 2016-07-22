# Logging

![](http://i.imgur.com/VdiUT.jpg)

## Logging [^1]

Logging is the process of recording application actions and state to a secondary interface.

### Logging System [^3]

![](https://lh3.googleusercontent.com/jbyMnJyc4tQwUkcz_XQAIQrca-LIXz-L3S5kfa8JhKmyiT2zYwgYf1VrS3J98yj2-jvGUsf6fQM5sg=w969-h229-no)

### Levels

<table>
  <tr>
    <th>Level</th>
    <th>When it’s used</th>
  </tr>
  <tr>
    <td>DEBUG</td>
    <td>Detailed information, typically of interest only when diagnosing problems.</td>
  </tr>
  <tr>
    <td>INFO</td>
    <td>Confirmation that things are working as expected.</td>
  </tr>
  <tr>
    <td>WARNING</td>
    <td>An indication that something unexpected happened, or indicative of some problem in the near future (e.g. ‘disk space low’). The software is still working as expected.</td>
  </tr>
  <tr>
    <td><br>ERROR<br></td>
    <td>Due to a more serious problem, the software has not been able to perform some function.</td>
  </tr>
  <tr>
    <td>CRITICAL</td>
    <td>A serious error, indicating that the program itself may be unable to continue running.</td>
  </tr>
</table>

### Best Practices [^2] [^4] [^5]

* Logging should always be considered when handling an exception but should never take the place of a real handler.
* Keep all logging code in your production code. Have an ability to enable more/less detailed logging in production, preferably per subsystem and without restarting your program.
* Make logs easy to parse by grep and by eye. Stick to several common fields at the beginning of each line. Identify time, severity, and subsystem in every line. Clearly formulate the message. Make every log message easy to map to its source code line.
* If an error happens, try to collect and log as much information as possible. It may take long but it's OK because normal processing has failed anyway. Not having to wait when the same condition happens in production with a debugger attached is priceless.


[^1]: [The Art of Logging](http://www.codeproject.com/Articles/42354/The-Art-of-Logging)
[^2]: [First Rule Of Logging](http://c2.com/cgi/wiki?FirstRuleOfLogging)
[^3]: [Taichung Python Logging](http://www.slideshare.net/ChunChiaChen1/20151024-taichungpy-python-logging)
[^4]: [Logging Best Practices](http://c2.com/cgi/wiki?LoggingBestPractices)
[^5]: [What are some patterns and anti-patterns of application logging?](http://programmers.stackexchange.com/questions/112402/what-are-some-patterns-and-anti-patterns-of-application-logging)

