#PDFMerger for PHP (PHP 5 Compatible)

Original written by http://pdfmerger.codeplex.com/team/view<br />
Forked from https://github.com/myokyawhtun/PDFMerger

## Composer Compatible

I've just forked this package to make it compatible with composer

To install add this line to your composer.json

```"clegginabox/pdf-merger": "dev-master"```

### Example Usage
```php

$pdf = new \Clegginabox\PDFMerger\PDFMerger;

$pdf->addPDF('samplepdfs/one.pdf', '1, 3, 4');
$pdf->addPDF('samplepdfs/two.pdf', '1-2');
$pdf->addPDF('samplepdfs/three.pdf', 'all');


$pdf->merge('file', 'samplepdfs/TEST2.pdf');

// REPLACE 'file' WITH 'browser', 'download', 'string', or 'file' for output options
```
## Changes

I've just forked this package to make it compatible with composer

I change  this line of code

    $fpdi->AddPage('P', array($size['w'], $size['h']));
to

    $fpdi->AddPage( $size['h'] > $size['w'] ? 'P' : 'L', array($size['w'], $size['h']));
