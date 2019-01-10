
var url = "http://116.117.157.186:10001";


function ajax(type, url, dataType, data, contentType, Authorization,async, succsFn, errorFn) {
  $.ajax({
    type: type,
    url: url,
    dataType: dataType,
    data: data,
    contentType: contentType,
    headers: {
      "Authorization": Authorization
    },
    async:async,
    success: function (data) {
      succsFn(data)
    },
    error: function (data) {
      errorFn(data)
    }
  })
}


//写cookies，一个小时过期 
function setCookie(name, value) {
  var exp = new Date();
  exp.setTime(exp.getTime() + 60 * 60 * 1000);
  document.cookie = name + "=" + escape(value) + ";expires=" + exp.toGMTString() + ";path=/";
}


//读取cookies 
function getCookie(name) {
  var arr, reg = new RegExp("(^| )" + name + "=([^;]*)(;|$)");

  if (arr = document.cookie.match(reg)) {
    return unescape(arr[2]);
  } else {
    return null;
  }
}


