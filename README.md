// ==UserScript==
// @name         ho luu nhien
// @namespace    http://tampermonkey.net/
// @version      0.5
// @description  TESTER JICT V2
// @author       jict
// @match        http://tranhdau.net/*
// @grant        none
// @run-at       document-end
// ==/UserScript==

(function(){
    $("body").dblclick(function(){
        if($("#doubleclick_d").is(":checked"))
            keyPress(68);
    });
    $("head").append("<style>.emberstyle a, #nick, #ip_newserver{border-radius:5px;} #fb_id:hover{text-decoration:none;}</style>");
    newIns();
    var interval_gold, interval_bomb, key = false, key2 = false, att=20, X=0, Y=0, k=0, fg=false;

    function autoSpawn()
    {
        setInterval(function(){
            if($("#overlays").is(':visible') && $("#autorespawnok").is(":checked"))
                $('.btn-play-guest')[0].click();
        },1000)
    }

    function newIns(){
              var skinInput = document.getElementById("skin");
        if (skinInput) {
            skinInput.value = "2202412260830120024298001735198212"; // thay id skin o day !
        }

    }
    $(document).on('keydown',function(e){
        // Doublesplit -> key2
        if (e.keyCode == 50)
        {
        }

        else if(e.keyCode == 80 && !$("#nick, #ip_newserver, #chat_textbox").is(":focus"))
        {
            $('.btn-play-guest')[0].click();
            $("#overlays").css("display","none");
        }


        else if(e.keyCode == 82)

        {
        }
        //=============================== mo =====================================
        else if(e.keyCode == 90  && e.ctrlKey){
			$('#close_chatfull').click(function(){$(this).fadeOut("fast");});
            setSkins(true); //Skins: false
            $('#screenshot, #account_button, .controls, #klan, #level, #stats, .tosBox').remove();
            $("#gamemode").replaceWith(
                ' </div></div>');
            $("#bilgilerModal").html('<div class="modal-dialog modal-sm"><div class="modal-content"><div class="modal-header">Emoji<button type="button" class="close" data-dismiss="modal">&times;</button></div><div class="modal-body"><h3>'+
                                     '<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;</h3></div></div></div>');

            $("#chat_textbox").attr("maxlength","70");
            $("#loginModal div.modal-content").replaceWith('<div class="modal-header">'+
                                                           '<button type="button" id="close_chatfull" class="close" data-dismiss="modal">&times;</button><h1 style="text-align:center;color:#FF0000;" class="modal-title">Hmmm..<br> Chat is full!</h1></div>');
        }
        //=============================== tat =====================================
        else if(e.keyCode == 88  && e.ctrlKey){
			$('#close_chatfull').click(function(){$(this).fadeOut("fast");});
            setSkins(false); //Skins: false
            $('#screenshot, #account_button, .controls, #klan, #level, #stats, .tosBox').remove();
            $("#gamemode").replaceWith(
                ' </div></div>');
            $("#bilgilerModal").html('<div class="modal-dialog modal-sm"><div class="modal-content"><div class="modal-header"><button type="button" class="close" data-dismiss="modal">&times;</button></div><div class="modal-body"><h3>'+
                                     '<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;</h3></div></div></div>');
            $("#chat_textbox").attr("maxlength","70");
            $("#loginModal div.modal-content").replaceWith('<div class="modal-header">'+
                                                           '<button type="button" id="close_chatfull" class="close" data-dismiss="modal">&times;</button><h1 style="text-align:center;color:#FF0000;" class="modal-title">Hmmm..<br> Chat is full!</h1></div>');


        }
            //=============================== moAcid =====================================
        else if(e.keyCode == 67  && e.ctrlKey){
			$('#close_chatfull').click(function(){$(this).fadeOut("fast");});
            setNames(true);//Acid:true
            $('#screenshot, #account_button, .controls, #klan, #level, #stats, .tosBox').remove();
            $("#gamemode").replaceWith(
                ' </div></div>');
            $("#bilgilerModal").html('<div class="modal-dialog modal-sm"><div class="modal-content"><div class="modal-header">Emoji<button type="button" class="close" data-dismiss="modal">&times;</button></div><div class="modal-body"><h3>'+
                                     '<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;</h3></div></div></div>');

            $("#chat_textbox").attr("maxlength","70");
            $("#loginModal div.modal-content").replaceWith('<div class="modal-header">'+
                                                           '<button type="button" id="close_chatfull" class="close" data-dismiss="modal">&times;</button><h1 style="text-align:center;color:#FF0000;" class="modal-title">Hmmm..<br> Chat is full!</h1></div>');
        }
                    //=============================== TatAcide =====================================
else if(e.keyCode == 86  && e.ctrlKey){
			$('#close_chatfull').click(function(){$(this).fadeOut("fast");});
             setNames(false);//Acid: false
            $('#screenshot, #account_button, .controls, #klan, #level, #stats, .tosBox').remove();
            $("#gamemode").replaceWith(
                ' </div></div>');
            $("#bilgilerModal").html('<div class="modal-dialog modal-sm"><div class="modal-content"><div class="modal-header">Emoji<button type="button" class="close" data-dismiss="modal">&times;</button></div><div class="modal-body"><h3>'+
                                     '<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;<button></button>&nbsp;</h3></div></div></div>');

            $("#chat_textbox").attr("maxlength","70");
            $("#loginModal div.modal-content").replaceWith('<div class="modal-header">'+
                                                           '<button type="button" id="close_chatfull" class="close" data-dismiss="modal">&times;</button><h1 style="text-align:center;color:#FF0000;" class="modal-title">Hmmm..<br> Chat is full!</h1></div>');
        }
// ...

// ...
                    //=============================== tat =====================================

    })
                })
();

var script = document.createElement('script');
(document.body || document.head || document.documentElement).appendChild(script);

	$("#instructions").hide();
        $("#adbg").hide();
        $("#footer").hide();
        $("#instructions").hide();
       // $("#settings-btn").hide();
        $("#canvasx").hide();
        $('.dialog-right').hide();
        $('.btn-danger').hide();
        $('.progress-bar-text').hide();
        $('.agario-exp-bar').hide();
        $('.progress-bar-star').hide();
        $("#gamemode").remove();



        $('.agario-profile-picture').replaceWith ('<img src="https://i.imgur.com/lVcAxJd.jpg" style=\" right: 100px; width: 200px; height: 210px;;\ ">')
        $("#overlays").append('<img src="https://i.imgur.com/tgVXiVu.jpeg" style="width:100%; height:1080px; display:inline-block;">');
        $('.dialog-left').css({color: 'rgba(255, 255, 255, 1)', 'background-color': 'rgba(0, 0, 0, 0.5)'})
        $('.agario-panel').css({color: 'rgba(255, 255, 255, 1)', 'background-color': 'rgba(0, 0, 0, 0.5)'})
        $('.btn-primary').css({color: 'rgba(255, 255, 255, 1)', 'background-color': 'rgba(0, 0, 0, 0.5)'})
        $('.btn-needs-server').css({color: 'rgba(255, 255, 255, 1)', 'background-color': 'rgba(0, 0, 0, 0.5)'})
        $('.btn-primary').text('Skin');
        $(".btn-play").text('Play');


window.addEventListener('keydown', keydown);
window.addEventListener('keyup', keyup);
var Feed = false;
var Speed = 50;

//Funtions
function split() {
    $("body").trigger($.Event("keydown", { keyCode: 32}));
    $("body").trigger($.Event("keyup", { keyCode: 32}));
}
function mass() {
    if (Feed) {
        window.onkeydown({keyCode: 87});
        window.onkeyup({keyCode: 87});
        setTimeout(mass, Speed);
    }
}

function keydown(event) {
    switch(event.keyCode){
    // Feed Macro
    case 81:                                        // Q
    {
        Feed = true;
        setTimeout(mass,Speed);
    }// Center
    case 83:                                       // S
        X = window.innerWidth / 2;
        Y = window.innerHeight / 2;
        $("canvas").trigger($.Event("mousemove", {clientX: X,clientY: Y}));

    break; // Triplesplit
    case 68:         //  and Put in Your Key
        split();
        setTimeout(split, Speed);
        setTimeout(split, Speed*2);
    break; // Doublesplit
    case 65:         // A and Put in Your Key
        split();
        setTimeout(split, Speed);
    break;

    }
} // When Player Lets Go Of Q,It Stops Feeding
function keyup(event) {
    if (event.keyCode == 81) {
        Feed = false;
    }
}

//Mouse Clicks
(function() {
    $("#canvas").bind("mousedown",function(event) {
        switch(event.which){
        case 1:

        break;
        case 2:

        break;
        case 3:
            Feed = true;
            setTimeout(mass, Speed);
        break;
        }
    });

    $("#canvas").bind("mouseup",function(event) {
        if (event.which == 3) {
            Feed = false;
        }
    });
    $('#canvas').bind('contextmenu',function(e) {
        e.preventDefault();
    });
}());



(function() {
'use strict';

var New_WhiteBackgroundColor = '#000';

var old_fillRect = CanvasRenderingContext2D.prototype.fillRect;
CanvasRenderingContext2D.prototype.fillRect = function() {
    var x = arguments[0];
    var y = arguments[1];
    var w = arguments[2];
    var h = arguments[3];

    if (x==0 && y==0 && w==this.canvas.width && h==this.canvas.height) {
        if (this.fillStyle == '#f2fbff') {
            this.fillStyle = New_WhiteBackgroundColor;
        }
    }

    return old_fillRect.apply(this, arguments);
};

function calculateRemain(text) {
    if (text.endsWith('s')) {
        var match;

        match = / in:? (\d+)s$/.exec(text);
        if (match !== null) {
            return parseInt(match[1], 10);
        }

        match = /^((\d+)m)? ?(\d+)s$/.exec(text);
        if (match !== null) {
            return (parseInt(match[2], 10) || 0) * 60 + parseInt(match[3], 10); // "x || 0" is "0 if x undefined"
        }
    }

    return null;
}

var old_fillText = CanvasRenderingContext2D.prototype.fillText;
CanvasRenderingContext2D.prototype.fillText = function() {
    if (arguments[0] === 'Leaderboard') {
        arguments[0] = ' PRC TOWN';
        this.fillStyle = 'skyblue';
    }
    return old_fillText.apply(this, arguments);
};
})();







var observer = new MutationObserver(function(mutations){
  mutations.forEach(function(mutation) {
    mutation.addedNodes.forEach(function(node) {
      if (/agario\.core\.js/i.test(node.src)){
        observer.disconnect();
        node.parentNode.removeChild(node);
        var request = new XMLHttpRequest();
        request.open("get", node.src, true);
        request.send();
        request.onload = function(){
          var coretext = this.responseText;
          var newscript = document.createElement("script");
          newscript.type = "text/javascript";
          newscript.async = true;
          window._op = new mouseWheelZoom();
          newscript.textContent = replaceCore(coretext);
          document.body.appendChild(newscript);
        };
      }
    });
  });
});
observer.observe(document, {attributes:true, characterData:true, childList:true, subtree:true});

const replaceCore = core => {
  core = core.replace(/;if\((\w)<1\.0\){/i, `;if(0){`);
  core = core.replace(/0;\w\[\w\+...>>3\]=(\w);\w\[\w\+...>>3\]=(\w);\w\[\w\+...>>3\]=(\w);\w\[\w\+...>>3\]=(\w);/i, `$& if(Math.abs($3-$1)>14e3 && Math.abs($4-$2)>14e3){window._op.mOX = ($1+$3)/2; window._op.mOY = ($2+$4)/2};`);


  return core;
}

var z = "";
var i = document.getElementById("helloDialog");
i.innerHTML += "<center><span class='text-muted'><span data-itr='instructions_e'> <b>" + z.fontcolor("skyblue") + "</b></span></span></center>";



load();
function load() {
    if (document.getElementById("overlays").style.display!="none") {
        document.getElementById("settings").style.display = "block";
    } else {
        setTimeout(load, 100);
    }
}
var Libra = document.getElementById('adbg');
if (Libra) { Libra.parentNode.removeChild(Libra); }

var Libra1 = document.getElementById('adbg');
if (Libra1) { Libra1.parentNode.removeChild(Libra1); }

var Libra2 = document.getElementById('adbg');
if (Libra2) { Libra2.parentNode.removeChild(Libra2); }
var Dingus = false;
var imlost = 35;



facebookIcon.appendChild(iconImage);

var instructions = document.getElementById("helloDialog");
instructions.appendChild(facebookIcon);



document.body.setAttribute('id', 'uxui');


var ux = document.getElementById("uxui");
ux.style.fontFamily = "Ubuntu";
ux.style.color = "darksalmon";



// EDIT RIENG !!

var elements = document.getElementsByClassName("dialog-left");
for (var i = 0; i < elements.length; i++) {
  elements[i].style.backgroundColor = "transparent";
}

var elements = document.getElementsByClassName("agario-panel agario-side-panel agario-profile-panel");
for (var i = 0; i < elements.length; i++) {
  elements[i].style.backgroundColor = "transparent";
}

var profileNameElements = document.getElementsByClassName("agario-profile-name");
if (profileNameElements.length > 0) {
  var profileNameElement = profileNameElements[0]; // Lấy phần tử đầu tiên trong danh sách
  profileNameElement.innerHTML = "luu nhien"; // Thay đổi nội dung
}

var profileNameElements = document.getElementsByClassName("agario-profile-id");
if (profileNameElements.length > 0) {
  var profileNameElement = profileNameElements[0]; // Lấy phần tử đầu tiên trong danh sách
  profileNameElement.innerHTML = "ID: 99999"; // Thay đổi nội dung
}

var profilePictureElements = document.getElementsByClassName("agario-profile-picture");
if (profilePictureElements.length > 0) {
  var profilePictureElement = profilePictureElements[0]; // Lấy phần tử đầu tiên trong danh sách
  profilePictureElement.src = "https://i.imgur.com/OM7hS4R.jpg"; // Đặt đường dẫn hình ảnh mới
}


var dialogLeftElements = document.getElementsByClassName("dialog-left");
if (dialogLeftElements.length > 0) {
  var dialogLeftElement = dialogLeftElements[0]; // Lấy phần tử đầu tiên trong danh sách
  var hrElements = dialogLeftElement.getElementsByTagName("hr");
  while (hrElements.length > 0) {
    var hrElement = hrElements[0]; // Lấy thẻ hr đầu tiên
    hrElement.parentNode.removeChild(hrElement); // Xóa thẻ hr
  }
}

var element = document.getElementsByClassName("mb-10")[0]; // Lấy phần tử đầu tiên có lớp là "mb-10"
element.style.marginTop = "-80px"; // Thay đổi giá trị margin right thành 20px
element.style.marginRight = "-15px"; // Thay đổi giá trị margin right thành 20px
element.style.width = "136px";
element.style.float = "Right";

var linkElements = document.querySelectorAll('a[data-toggle="modal"][data-target="#inPageModal"][onclick="openSkinsList();"]');
if (linkElements.length > 0) {
  var linkElement = linkElements[0];
  linkElement.textContent = "Skin o day ne";
}

var inputElement = document.getElementById("nick");
if (inputElement) {
  inputElement.placeholder = "Nhập tên zô i ><"; // Thay "New Placeholder" bằng giá trị placeholder mới bạn muốn đặt
}

// var pink = document.querySelector(".btn.btn-play.btn-success.btn-needs-server");
// if (pink) {
//   pink.style.background = "green"; // Thay "red" bằng màu nền mới bạn muốn áp dụng
// }



