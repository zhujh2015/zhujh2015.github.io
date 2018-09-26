## 1.1 query 的基础控件用法
### 1.1.1 页面传值中文乱码 
-- 传值
dict_nameid = encodeURIComponent(encodeURIComponent(dict_nameid));
</br>
-- 接收值
dict_nameid=phhcUtil.getUrlParameter("dict_nameid");
dict_nameid=decodeURIComponent(decodeURIComponent(dict_nameid));
</br>

### 1.1.2 解析url 页面传值方式的参数 
 getUrlParameter:function(name){
	    	var reg = new RegExp("(^|&)"+ name +"=([^&]*)(&|$)");
	        var r = window.location.search.substr(1).match(reg);
	        if(r!=null){
	       	 return  unescape(r[2]); 
	        } 
	        return null;
	    }
### 1.1.3 span 标签内容值
  $("#span_title").text(titleName + ":");