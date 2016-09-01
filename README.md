#跟浮动说再见

一、各种清除浮动，我表示受够了(╯‵□′)╯︵┻━┻。

    1.直接一个<div style="clear:both;"></div>放在浮动元素后（浪费标签）
    2.父元素.fix{overflow:hidden; zoom:1;}（会不小心裁掉内容）
    3.父元素.fix{zoom:1;}
            .fix:after{
                display:block; 
                content:'clear'; 
                clear:both; 
                line-height:0;  /*height:0;也可*/
                visibility:hidden;
            }
        （这么老长一段，清一次写一次，好麻烦（扶额）

二、浮动缺点好多，想和他分手...

    1.会脱离文档流，使周围元素环绕这个浮动元素、要清除浮动。
    2.无法方便地实现水平居中。
    3.无法实现每行垂直对齐（除非定高）。

    浮动-本来是为了解决 文字环绕图片 这个问题而存在的。我们不合适。

三、新欢：display: inline-block
    
    1.不会脱离文档流，不用清除浮动。
    2.水平居中、垂直对齐 轻松实现 ^O^ 。

    但新欢也不完美，它有间隙bug。
    解决：[http://www.zhangxinxu.com/wordpress/2012/04/inline-block-space-remove-%E5%8E%BB%E9%99%A4%E9%97%B4%E8%B7%9D/]