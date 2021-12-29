# metadata.json

<head>
<!--_text_ for i tag-->
<!--**text** for bold-->
<link rel="stylesheet" href="https://s0net.github.io/easy.css/style.css">
<style>
#mydiv {
  position: absolute;
  z-index: 9;
  background-color: #f1f1f1;
  border: 1px solid #d3d3d3;
  text-align: center;
}

#nav_head {
  padding: 10px;
  cursor: move;
  z-index: 10;
  background-color: #2196F3;
  color: #fff;
}
</style>
</head>

<body class="goodfont">

<div id="mydiv">
  <div id="nav_head capitalcase b">in this document</div>
  <p>Move</p>
  <p>this</p>
  <p>DIV</p>
</div>

is the new way of giving data to your site for websites to read  

to start make a `metadata.json` file and and the give the following values to it

<section id="1">

## **<span class="redtext ">1)</span><span class="bluetext ">Name</span>**

<pre>{"name": "sitename"}</pre>

this is the name of your site that will be shown

</section>

<script>
    dragElement(document.getElementById("mydiv"));

function dragElement(elmnt) {
  var pos1 = 0, pos2 = 0, pos3 = 0, pos4 = 0;
  if (document.getElementById(elmnt.id + "header")) {
    document.getElementById(elmnt.id + "header").onmousedown = dragMouseDown;
  } else {
    elmnt.onmousedown = dragMouseDown;
  }

  function dragMouseDown(e) {
    e = e || window.event;
    e.preventDefault();
    pos3 = e.clientX;
    pos4 = e.clientY;
    document.onmouseup = closeDragElement;
    document.onmousemove = elementDrag;
  }

  function elementDrag(e) {
    e = e || window.event;
    e.preventDefault();
    pos1 = pos3 - e.clientX;
    pos2 = pos4 - e.clientY;
    pos3 = e.clientX;
    pos4 = e.clientY;
    elmnt.style.top = (elmnt.offsetTop - pos2) + "px";
    elmnt.style.left = (elmnt.offsetLeft - pos1) + "px";
  }

  function closeDragElement() {
    document.onmouseup = null;
    document.onmousemove = null;
  }
}
</script>

</body>
