## 1.1 query �Ļ����ؼ��÷�
### 1.1.1 ҳ�洫ֵ�������� 
-- ��ֵ
dict_nameid = encodeURIComponent(encodeURIComponent(dict_nameid));
</br>
-- ����ֵ
dict_nameid=phhcUtil.getUrlParameter("dict_nameid");
dict_nameid=decodeURIComponent(decodeURIComponent(dict_nameid));
</br>

### 1.1.2 ����url ҳ�洫ֵ��ʽ�Ĳ��� 
 getUrlParameter:function(name){
	    	var reg = new RegExp("(^|&)"+ name +"=([^&]*)(&|$)");
	        var r = window.location.search.substr(1).match(reg);
	        if(r!=null){
	       	 return  unescape(r[2]); 
	        } 
	        return null;
	    }
### 1.1.3 span ��ǩ����ֵ
  $("#span_title").text(titleName + ":");