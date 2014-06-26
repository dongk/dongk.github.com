
PHP中匿名函数如何使用外部变量。  

    $col = $orderArr[0];
    $order = $orderArr[1]=='asc'?1:-1;
    usort($data,function($a,$b) use ($col,$order){
        if($a[$col]>$b[$col])
            return $order;
        else
            return -1*$order;
    });
