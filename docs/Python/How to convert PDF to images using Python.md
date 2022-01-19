# How to convert PDF to images using Python
Follow these steps in order to convert PDF files to images using [[Python]]:
1. Run `pip install pdf2image`.
2. Run script below:

```python
from pdf2image import convert_from_path


pdf_path = r'C:\Users\Almog-PC\Downloads\Technion Student - Almog Tzabari.pdf'
pages = convert_from_path(pdf_path, 500)
for page in pages:
	page.save('out.jpg', 'JPEG')
```
