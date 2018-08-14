# Bumo CTP1.0 Token ��׼

## ���

CTP1.0(Contract Token Protocol) ָ���� BUMO ��Լ���� token �ı�׼Э�顣��Э���ṩ��ת�� token �Ļ������ܣ������� token ��Ȩ��������ʹ�á�

## Ŀ��

��׼�ӿڿ����� Bumo �ϵ��κ� token ������Ӧ�ó���ʹ�ã�����Ǯ���ͽ�������


## ����

Bumo ���ܺ�Լ�� javascript ʵ��,����������ں��� init��main �� query ��init �������ں�Լ����ʱ��ʼ����main ������Ҫ��������д�룬query �����������ݲ�ѯ��


## ���ܺ�Լ����

| ����        | ����                    |  
| :--------- | ------------------------ |
|name        | Token ����                |
|symbol      | Token ����                |
|decimals    | Token С��λ��             |
|totalSupply | Token ����                |


## ����

### contractInfo

���� Token �Ļ�����Ϣ����ں��� query��

E.g.

- ����json�ṹ:
```json
{
    "method":"contractInfo",
    "params":""
}
```
- ������function contractInfo()
- ����ֵ��
```json
{
    "result":{
        "symbol":"XXX",
        "decimals":5,
        "totalSupply":"10000000000000000000",
        "name":"XXXCOIN",
    }
} 
```

### name

���� token �����ơ���ں��� query��

E.g.

- ����json�ṹ:
```json
{
    "method":"name",
    "params":""
}
```
- ������function name()
- ����ֵ��
```json
{
    "result":{
        "name":"XXXCOIN"
    }
} 
```

### symbol

���� token �ķ��š���ں��� query��

E.g.

- ����json�ṹ:
```json
{
    "method":"symbol",
    "params":""
}
```
- ������function symbol()
- ����ֵ��
```json
{
    "result":{
        "symbol":"XXX"
    }
} 
```

### decimals

���� token ʹ�õ�С�����λ�� ���� 5,��ʾ���� token ����Ϊ100000����ں���q uery��

E.g.

- ����json�ṹ:
```json
{
    "method":"decimals",
    "params":""
}
```
- ������function decimals()
- ����ֵ��
```json
{
    "result":{
        "decimals":5
    }
} 
```

### totalSupply

���� token ���ܹ�Ӧ������ں��� query��

E.g.

- ���� json �ṹ:
```json
{
    "method":"totalSupply",
    "params":""
}
```
- ������function totalSupply()
- ����ֵ��
```json
{
    "result":{
        "totalSupply":"10000000000000000000"
    }
} 
```

### balanceOf

���� owner �˻����˻�����ں��� query��

- ����json�ṹ:
```json
{
    "method":"balanceOf",
    "params":{
        "address":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj"
    }
}
```
������address �˻���ַ

- ������function balanceOf(owner)
- ����ֵ��
```json
{
    "result":{
        "balanceOf":"100000000000000",
    }
} 
```

### transfer

ת�� value ��token�������ĵ�ַ to�����ұ��봥�� log �¼��� ��� from �ʻ����û���㹻��token��֧�����ú���Ӧ�ñ�throw, from Ϊ���ͽ��׵��˻���ַ����ں��� main��

- ���� json �ṹ:
```json
{
    "method":"transfer",
    "params":{
        "to":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj",
        "value":"1000000"
    }
}
```
������toĿ���˻���ַ��
������valueת���������ַ������ͣ�

- ������function transfer(to, value)
- ����ֵ��true�������쳣

### transferFrom

�ӵ�ַfrom��������Ϊ value ��token����ַ to�����봥�� log �¼��� �� transferFrom ֮ǰ��form �����Ѿ����ù� approve �� to ��Ȩ�˶�ȡ���� from �ʻ����û���㹻��token��֧������ from ��Ȩ�� to �Ķ�Ȳ��㣬�ú���Ӧ�ñ� throw����ں��� main��

����json�ṹ:
```json
{
    "method":"transferFrom",
    "params":{
        "from":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj",
        "to":"buQYH2VeL87svMuj2TdhgmoH9wSmcqrfBner",
        "value":"1000000"
    }
}
```
������from Դ�˻���ַ��
������to Ŀ���˻���ַ��
������value ת���������ַ������ͣ�

- ������function transferFrom(from,to,value)
- ����ֵ��true�������쳣


### approve

��Ȩ�˻� spender ���Դӽ��׷������˻�ת������Ϊ value ��token����ں��� main��

����json�ṹ:
```json
{
    "method":"approve",
    "params":{
        "spender":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj",
        "value":"1000000"
    }
}
```
������spender �˻���ַ��
������value ����Ȩ��ת���������ַ������ͣ�

- ������function approve(spender, value)
- ����ֵ��true �������쳣

### assign

��Լ token ӵ������ to ��������Ϊ value �� token����ں��� main��

����json�ṹ:
```json
{
    "method":"assign",
    "params":{
        "to":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj",
        "value":"1000000"
    }
}
```
������to �����˻���ַ��
������value �����������ַ������ͣ�

- ������function assign(to, value)
- ����ֵ��true �������쳣

### changeOwner

����Լ token ӵ��Ȩת�Ƹ� address��ֻ�к�Լ token ӵ���߲���ִ�д�Ȩ�ޣ���ں��� main��

���� json �ṹ:
```json
{
    "method":"changeOwner",
    "params":{
        "address":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj"
    }
}
```
������address �˻���ַ��

- ������function changeOwner(address)
- ����ֵ��true�������쳣

### allowance

���� spender ��Ȼ������� owner ��ȡ�Ľ���ں��� query��

����json�ṹ:
```json
{
    "method":"allowance",
    "params":{
        "owner":"buQnTmK9iBFHyG2oLce7vcejPQ1g5xLVycsj",
        "spender":"buQYH2VeL87svMuj2TdhgmoH9wSmcqrfBner"
    }
}
```
������owner �˻���ַ��
������spender �˻���ַ��

- ������function allowance(owner, spender)
- ����ֵ��
```json
{
    "result":{
        "allowance":"1000000",
    }
} 
```


## ��ں���

### ��ں��� init

```js
function init(input_str){
}

```

### ��ں��� main

```js
function main(input_str){
    let input = JSON.parse(input_str);

    if(input.method === 'transfer'){
        transfer(input.params.to, input.params.value);
    }
    else if(input.method === 'transferFrom'){
        transferFrom(input.params.from, input.params.to, input.params.value);
    }
    else if(input.method === 'approve'){
        approve(input.params.spender, input.params.value);
    }
    else if(input.method === 'assign'){
        assign(input.params.to, input.params.value);
    }
    else if(input.method === 'changeOwner'){
        changeOwner(input.params.address);
    }
    else{
        throw '<undidentified operation type>';
    }
}
```

### ��ں���query

```js
function query(input_str){
    loadGlobalAttribute();

    let result = {};
    let input  = JSON.parse(input_str);
    if(input.method === 'name'){
        result.name = name();
    }
    else if(input.method === 'symbol'){
        result.symbol = symbol();
    }
    else if(input.method === 'decimals'){
        result.decimals = decimals();
    }
    else if(input.method === 'totalSupply'){
        result.totalSupply = totalSupply();
    }
    else if(input.method === 'contractInfo'){
        result.contractInfo = contractInfo();
    }
    else if(input.method === 'balanceOf'){
        result.balance = balanceOf(input.params.address);
    }
    else if(input.method === 'allowance'){
        result.allowance = allowance(input.params.owner, input.params.spender);
    }
    else{
       	throw '<unidentified operation type>';
    }

    log(result);
    return JSON.stringify(result);
}
```
