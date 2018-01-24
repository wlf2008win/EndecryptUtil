# EndecryptUtil

## 简介
Java、Android加密解密工具类，不依赖于其他库。

[查看 EndecryptUtil.java 源码](https://github.com/whvcse/EndecryptUtil/blob/master/src/com/wangfan/endecrypt/utils/EndecryptUtils.java)

## 导入
#### grade
```java
dependencies {
    compile 'com.othershe:BaseAdapter:1.2.0'
}
```
#### maven
```java
dependencies {
    compile 'com.othershe:BaseAdapter:1.2.0'
}
```
#### jar包
[EndecryptUtil.jar]()

## 用法
#### 1.字符串转base64编码
```java
String str = "Hello Word!";
String rs = EndecryptUtils.encrytBase64(str);
```
#### 2.base64编码转字符串
```java
String str = "SGVsbG8gV29yZCE=";
String rs = EndecryptUtils.decryptBase64(str);
```


#### 3.字符串转16进制
```java
String str = "Hello Word!";
String rs = EndecryptUtils.encrytHex(str);
```
#### 4.16进制转字符串
```java
String str = "48656c6c6f20576f726421";
String rs = EndecryptUtils.decryptHex(str);
```


#### 5.AES加密
```java
String str = "Hello Word!";
Key key = EndecryptUtils.generateKey("wangfan");
String rs = EndecryptUtils.encrytAes(str, key);
```
#### 6.AES解密
```java
String str = "2c700dadcc66726f1665a4d604f6e6a4f8a498bc0173ed5f49f063b8f1a74f7e";
Key key = EndecryptUtils.generateKey("wangfan");
String rs = EndecryptUtils.decryptAes(str, key);
```


#### 7.Md5加密
```java
String str = "Hello Word!";
String rs = EndecryptUtils.encrytMd5(str);
```
#### 8.Md5加盐加密
```java
String str = "Hello Word!";
String salt = "wangfan";  //盐
int hashIterations = 3;  //散列次数,把密文再进行3次Md5加密
String rs = EndecryptUtils.encrytMd5(str, salt, hashIterations);
```
 
