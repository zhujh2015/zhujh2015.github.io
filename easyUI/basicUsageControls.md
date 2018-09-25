# markdown https://www.w3cschool.cn/lme/q92a1srq.html
## 1.1 easyui 的基础控件用法
### 1.1.1 combobox 获取
hpt_no = $("#" + id).combobox('getValue');
hpt_noName =$('#ageCrowdDw_Txt').combobox('getText');
### 1.1.2 textbox  获取
$("#userName").textbox('getValue');

### 1.1.3 textbox赋值
$("#deptTxt").textbox('setValue', '');
$("#" + id).attr("value", value);

### 1.1.4 combobox 赋值
 $("#" + id).combobox("setValue", "");
 
### 1.1.5 包含indexOf
$(obj).attr("id").indexOf(dict_id);

### 1.1.6 循环
 $("#div_ageCrowd div").each(function (index, element) {});
 
### 1.1.7 combobox 初始化
 dictList.unshift({"key": "-1", "value": "--请选择--"});  </br>
 首行插入 unshift  </br>
 末尾插入 push  </br>
    $("#" + id).combobox({
        data: dictList,</br>
        valueField: valueField == "" || valueField == undefined ? "key" : valueField,</br>
        textField: textField == "" || valueField == undefined ? "value" : textField,</br>
        panelHeight: "200", -- (列表高度)  </br>
        editable: true, -- (可编辑)  </br>
        limitToList: true, -- (列表检索)  </br>
        value: defValue,-- (设置默认值)  </br>
        onSelect: function () { -- (选择事件)  </br>
            comboboxSelectFunc(id);
        },
        onChange: function () {-- (更改事件)  </br>
            comboboxChangeFunc(id);
        }
    });  </br>
### 1.1.8 替换
     <code> $(element).attr("id").replace("scc_", "");</code> 
### 1.1.9 json 初始化
    <code> 
    var firstObj={};
    firstObj["value1"] ="-1";
    firstObj["text1"]="--请选择--";
    或者
    firstObj.value1="-1";
    firstObj.text1="--请选择--";
    dictList.push(firstObj);
    </code>
