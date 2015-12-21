# DocumentJSPlugin
Based on i5ting_ztree_toc : https://github.com/i5ting/i5ting_ztree_toc 


### 讲上述代码封装成了三个js文件, 一个css文件, 只要在文件中引入:

    <link rel = "stylesheet" href="https://dn-stk.qbox.me/css/zTreeStyle.css" type="text/css">
    
    
    <script type="text/javascript" src="https://dn-stk.qbox.me/js/jquery-1.4.4.min.js"></script>
    <script type="text/javascript" src="https://dn-stk.qbox.me/js/jquery.ztree.core-3.5.js"></script>
    <script type="text/javascript" src="https://dn-stk.qbox.me/js/ztree_toc.js"></script>
    <SCRIPT type="text/javascript" >
        <!--
        $(document).ready(function(){
            $('#tree').ztree_toc({
                is_auto_number:true
            });
        });
        //-->
    </SCRIPT>
    
    即可使得文档自动生产侧边栏.
    
    若要实现加密功能:
    
    还需引入:     
    
    <script src="https://dn-stk.qbox.me/js/MD5.js"></script>

        <script>
        loopy();
        function loopy() {
            var key = "";
            while (MD5(key) != MD5("123")) {//初始密码123 注意, 使用时直接手动计算出初始密码的md5值,不要才用现在的方式
                key = prompt("输入正确密码才能登陆!");
            }
            alert("登陆成功！");
        }
    </script>
    
    
    该加密只能稍微提高下破解门槛, 密码仍旧是以MD5值的方式存储在js文件中,可被他人看见.
