# phpvalidate
get the class from shopnc

## 例子
    //创建验证类
    $obj_validate = new Validate();
    $obj_validate->validateparam = array(
      array("input"=>$_POST["username"],"require"=>"true","message"=>'用户名不能为空'),
      array("input"=>$_POST["password"],"require"=>"true","message"=>'密码不能为空'),
      array("input"=>$_POST["email"], "require"=>"true","validator"=>"email","message"=>'请正确填入
      Email'),
    );
    $error = $obj_validate->validate();
    if ($error != ''){
      //输出错误信息
      showDialog($error);
    }
