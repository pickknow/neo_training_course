
#### 画出Base58Check的解码过程流程图

![image](https://i.postimg.cc/wBJ267PH/1.png)


#### 编码实现，梅克尔树根节点hash值计算。假设叶子节点为三笔交易，字节分为为: 0x0000, 0x1111, 0x2222

* 伪代码实现

```

var txs = new ArrayList<string> { "0x1111", "0x2222", "0x3333" };
string neoHash(string str) {
    return str;
}
string makeHash(ArrayList<string> ls) {
    var len = ls.Length;
    if (len == 1) return ls[0];
    var arrList = new ArrayList<string>();
    for (var i = 0; i < len; i = i + 2) {
        arrList.add(neoHash(ls[i] + ls[i + 1]));
    }
    return makeHash(arrList);
}
var txsHash = txs.Select(e => neoHash(e));
var rootHash = makeHash(txsHash);

```




#### 画图描述一笔UTXO的流通。Tom最开始有8个NEO，转账给Alice 5个Neo，Alice再将其中的1个NEO转给Lily，1个给了Tom。


![image](https://i.postimg.cc/SsfGMHkv/2.png)