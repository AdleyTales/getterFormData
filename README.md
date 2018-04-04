# getterFormData
```
/**
 * el：容器名 不需要form做容器
 * 如果name的表单值为空，不会捕获
 * 结果示例：{name:xxx,code:yyy}
 */
function getterFormData(el) {
    var obj = {};
    Array.from($(el).find('input,select,textarea')).forEach(function (item, index) {
        if ($(item).attr('name') && $(item).val() != '') {
            obj[$(item).attr('name')] = $(item).val();
        }
    });
    return obj;
}

```
