# Dhhimel.pdf
Demo project
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My PDF Collection</title>
    <style>
        body { font-family: Arial, sans-serif; }
        .pdf-list { list-style: none; padding: 0; }
        .pdf-item { margin-bottom: 10px; }
    </style>
</head>
<body>
    <h1>My Important PDFs</h1>
    <input type="text" id="search" placeholder="Search PDFs..." onkeyup="searchPDFs()">
    <ul id="pdfList" class="pdf-list">
        <!-- Ekhane nijer PDF link boshao -->
        <li class="pdf-item"><a href="pdfs/my_important_book.pdf" target="_blank">My Important Book</a></li>
        <li class="pdf-item"><a href="pdfs/mathematics_notes.pdf" target="_blank">Mathematics Notes</a></li>
        <li class="pdf-item"><a href="pdf.com" target="_blank">Physics Guide</a></li>
        <li class="pdf-item"><a href="pdfs/sample_paper.pdf" target="_blank">Sample Paper</a></li>
        <!-- Aro link add koro -->
    </ul>

    <script>
        function searchPDFs() {
            const input = document.getElementById('search').value.toLowerCase();
            const pdfList = document.getElementById('pdfList');
            const items = pdfList.getElementsByClassName('pdf-item');

            for (let i = 0; i < items.length; i++) {
                const item = items[i].textContent.toLowerCase();
                if (item.includes(input)) {
                    items[i].style.display = '';
                } else {
                    items[i].style.display = 'none';
                }
            }
        }
    </script>
</body>
</html>
