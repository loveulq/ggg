function bounce(fn,deley){
    var timer = null,
        run = true,
        deley = deley || 500;
    return function(){
        var context = this;
        if(run){
           clearTimeout(timer); 
           timer = setTimeout(function(){
                fn.call(context);
                run = false;
            },deley);
        }else{
            run = true;
        }
    }
}
$(document).ready(function(){
    var uuu = window.location.href;
    if(uuu.indexOf("#") >= 0 ){
        var id = uuu.split("#")[1];
        var ttt = $("#" + id).offset().top;
        var ddd = "#" + id;
        $('html,body').animate({scrollTop:ttt},'slow');

        $("#nav > a").removeClass("selected");
        $('a[href=' + ddd + ']').addClass("selected");
    }
    $("#nav > a").on("click",function(e){
        $("#nav > a").removeClass("selected");
        $(this).addClass("selected");
    })
    $("#submit").on("click",function(e){
        var username = $("#username").val().trim(),
        mail = $("#mail").val().trim();
        if(!username){
            alert("姓名不能为空");
            return;
        }
        if(!mail){
            alert("邮箱不能为空");
            return;
        }
        alert("提交成功");
    })
})