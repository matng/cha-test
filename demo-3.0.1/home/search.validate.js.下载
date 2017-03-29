$(function() {
    var $searchSelectList = $("#searchSelectList");
    var $serachWord = $("#serachWord");
    $serachWord.focus();
    var timer4Search = null;
    $("#searchSelect").hover(function() {
        clearTimeout(timer4Search);
        $searchSelectList.slideDown(300);
        $(this).addClass("hover");
        $(this).trigger("click");
    }, function(e) {
        timer4Search = setTimeout(function() {
            $searchSelectList.slideUp(300);
            $(e.currentTarget).removeClass("hover");
        }, 300);
    });
    $searchSelectList.find("li").click(function() {
        var config = $.parseJSON($(this).attr("data-config"));
        var wrod = $serachWord.val();
        $("#searchSelectBtn").text(config.text);
        $("#domain").attr("value", config.domain);
        $serachWord.val(wrod).attr("placeholder", config.placeholder).placeholder();
        $searchSelectList.hide();
        $searchSelectList.find("li").show();
        $(this).hide();
    });
    $("#searchForm").submit(function() {
        var serachWord = $.trim($serachWord.val());
        if (serachWord == "" || serachWord == $serachWord.attr("placeholder")) {
            alert("请输入关键字");
            return false;
        }
    });
    $("#searchBtn").mouseover(function() {
        $(this).addClass("hover");
    }).mouseout(function() {
        $(this).removeClass("hover");
    });
    $searchSelectList.find("li").mouseover(function() {
        $searchSelectList.find("li").removeClass("hover");
        $(this).addClass("hover");
    }).mouseout(function() {
        $(this).removeClass("hover");
    });
	
});