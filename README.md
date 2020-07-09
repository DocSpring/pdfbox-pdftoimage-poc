Run these commands:

```
#!/bin/bash

git clone https://github.com/DocSpring/pdfbox-pdftoimage-poc.git /tmp/pdfbox-pdftoimage-poc
cd /tmp/pdfbox-pdftoimage-poc

curl https://repository.apache.org/content/groups/snapshots/org/apache/pdfbox/pdfbox-app/2.0.21-SNAPSHOT/pdfbox-app-2.0.21-20200707.181003-84.jar -o pdfbox-app-2.0.21.jar
curl https://archive.apache.org/dist/pdfbox/2.0.19/pdfbox-app-2.0.19.jar -o pdfbox-app-2.0.19.jar

java -jar pdfbox-app-2.0.19.jar PDFToImage -format png -dpi 140 -quality 0.9 -prefix "/tmp/pdfbox-pdftoimage-poc/2.0.19-page-" example.pdf
java -jar pdfbox-app-2.0.21.jar PDFToImage -imageType png -dpi 140 -quality 0.9 -outputPrefix "/tmp/pdfbox-pdftoimage-poc/2.0.21-page-" example.pdf
```
