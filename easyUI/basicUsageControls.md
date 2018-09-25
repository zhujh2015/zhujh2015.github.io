#easyui 的基础控件用法
##1.1
###1.1.1 combobox 获取
hpt_no = $("#" + id).combobox('getValue');
hpt_noName =$('#ageCrowdDw_Txt').combobox('getText');
###1.1.2 textbox  获取
$("#userName").textbox('getValue');

###1.1.3 textbox赋值
$("#deptTxt").textbox('setValue', '');
$("#" + id).attr("value", value);

###1.1.4 combobox 赋值
 $("#" + id).combobox("setValue", "");
 
###1.1.5 包含indexOf
$(obj).attr("id").indexOf(dict_id);

###1.1.6 循环
 $("#div_ageCrowd div").each(function (index, element) {});
 
###1.1.7 combobox 初始化
 dictList.unshift({"key": "-1", "value": "--请选择--"});
    $("#" + id).combobox({
        data: dictList,
        valueField: valueField == "" || valueField == undefined ? "key" : valueField,
        textField: textField == "" || valueField == undefined ? "value" : textField,
        panelHeight: "200", 列表高度
        editable: true,
        limitToList: true,
        value: defValue,
        onSelect: function () {
            comboboxSelectFunc(id);
        },
        onChange: function () {
            comboboxChangeFunc(id);
        }
    });
