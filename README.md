# Bad-Words

<div style = "direction:rtl;text-align:right;">
كود بسيط بالجافا سكريبت يعمل كفلتر لكشف النصوص التي تحتوي على ألفاظ نابية.


.هذا الكود يعتمد على قائمة يدوية للكلمات النابية، والألفاظ الخادشة المحتملة باللغة العربية

يُمكن استخدام هذا الكود بسهولة في المنتديات، أو المواقع الشخصية، أو المدونات التي تتيح نظام التعليقات لكل مقال.

A simple JavaScript code that works as a filter to detect text that contains profane words. This code is based on a manual list of bad dirty words in Arabic

This code can be easily used in forums, personal sites, or blogs that allow comments for each article.

```javascript
function kalimat(KMOE, text) {
        text = normalizeText(text);
        for (let i = 0; i < KMOE.length; i++) {
            if (text.includes(KMOE[i])) {
                return true;
            }
        }
        return false;
    }
    // Function to check the user's input
    function checkWord() {
        // importanrt only const for privacy **** 
        const userWord = document.getElementById("userWord").value;
        const result = kalimat(arrayofbadkalimt, userWord);
        const resultElement = document.getElementById("result");
//-------------------------------------------------------------------------------
        if (result) {
            resultElement.innerText = "The word you entered is offensive // التعليق الذي قمت بإدخاله يحتوي ألفاظا نابية، الرجاء الالتزام بأدب النقاش ";
            resultElement.style.color = "red";
        }    


        /**you can remove the else condition because not neccsecy to tell him he enterd good word for instance */
        else {
            resultElement.innerText = "The word you entered is not offensive  ";
            resultElement.style.color = "green";
        }
    }

قبل ذلك قم بتضمين الملف داخل مشروعك كالآتي:

```javascript
    <!--استدعاء مكتبة الألفاظ النابية-->
    <script src="kalimat.js"></script>
```

ملاحظة: الغرض الوحيد من ذكر هذه الكلمات النابية في الملف هو فقط لمحاولة منع التعليقات المسيئة، لذا يُرجى المعذرة.

</div>
