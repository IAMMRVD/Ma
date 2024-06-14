
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Java Code Snippets</title>
<style>
    pre {
        background-color: #ffffff;
        padding: 1px;
        border-radius: 1px;
        overflow-x: auto;
    }
</style>
</head>
<body style="background-color: white; color: white;">>

<h1>NAVUSA COPY MADTHA IDVI NIVSA MADI</h1>

<button onclick="copyCode(1)">1</button>
<button onclick="copyCode(2)">2</button>
<button onclick="copyCode(3)">3</button>
<button onclick="copyCode(4)">4</button>
<button onclick="copyCode(5)">5</button>
<button onclick="copyCode(6)">6</button>
<button onclick="copyCode(7)">7</button>
<button onclick="copyCode(8)">8</button>
<button onclick="copyCode(9)">9</button>
<button onclick="copyCode(10)">10</button>
<pre id="code1">
hi

</pre>

<pre id="code2">
}
hii
</pre>

<pre id="code3">

hiii
</pre>

<pre id="code4">
hiiii
</pre>

<pre id="code5">
hiiiii

</pre>

<pre id="code6">
hiiiiii
</pre>

<pre id="code7">
hiiiiiii
</pre>
<pre id="code8">
hiiiiiiii
 </pre>
<pre id="code9">
hiiiiiiiii
<pre id="code10">
hiiiiiiiiii
</pre>
<button onclick="copyCode(1)">Copy Code 1</button>
<button onclick="copyCode(2)">Copy Code 2</button>
<button onclick="copyCode(3)">Copy Code 3</button>
<button onclick="copyCode(4)">Copy Code 4</button>
<button onclick="copyCode(5)">Copy Code 5</button>
<button onclick="copyCode(6)">Copy Code 6</button>
<button onclick="copyCode(7)">Copy Code 7</button>
<button onclick="copyCode(8)">Copy Code 8</button>
<button onclick="copyCode(9)">Copy Code 9</button>

<script>
function copyCode(id) {
    var code = document.getElementById('code' + id);
    var range = document.createRange();
    range.selectNode(code);
    window.getSelection().removeAllRanges();
    window.getSelection().addRange(range);
    document.execCommand("copy");
    window.getSelection().removeAllRanges();
    alert("Code " + id + " copied to clipboard!");
}
</script> 
<p style="color: red;">created by mr_______d</p>

