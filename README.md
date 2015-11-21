# PHPUnit_Printer

An additional printer for PHPUnit that displays the test progress like this:

```
> SUITE: Tests
  > SUITE: BuildBucketTest
    > TEST: BuildBucketTest::writeAccessToBucket
      SUCCESS. (Duration: 0.89 sec)
    > TEST: BuildBucketTest::listFiles
      SUCCESS. (Duration: 0.44 sec)
    > TEST: BuildBucketTest::readAccessToBucket
      SUCCESS. (Duration: 0.84 sec)
    > TEST: BuildBucketTest::deleteFile
      SUCCESS. (Duration: 0.21 sec)
  < Duration: 2.39 sec
  > SUITE: SystemstorageBucketTest
    > TEST: SystemstorageBucketTest::writeAccessToBucket
      SUCCESS. (Duration: 0.85 sec)
    > TEST: SystemstorageBucketTest::listFiles
      SUCCESS. (Duration: 0.31 sec)
    > TEST: SystemstorageBucketTest::readAccessToBucket
      SUCCESS. (Duration: 0.78 sec)
    > TEST: SystemstorageBucketTest::deleteFile
      SUCCESS. (Duration: 0.21 sec)
  < Duration: 2.15 sec
  > SUITE: WebserverTest
    > TEST: Warning
      FAILURE: No tests found in class "WebserverTest". (Duration: 0 sec)
  < Duration: 0 sec
< Duration: 4.55 sec
```

## Configuration

```
<phpunit bootstrap="bootstrap.php"
         colors="true"
         printerClass="Aoepeople_Phpunit_Printer_VerboseResultPrinter">
   [...]
</phpunit>
```
NOTE: you might need to add `printerFile` in case you're not loading Composer's autoload file in your `bootstrap.php`