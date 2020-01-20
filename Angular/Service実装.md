# まとめ

## サービス追加

```
ng g service service/[serviceDir名]/[service名]
```

## POST
IF、headers、Bodyを作成してPostに飛ばす

### IF定義
```javascript:TypeScript
interface IConsulter {
  id: string;
  name: string;
  mailAddress: string;
}
```

### headers作成
```javascript:TypeScript
    //json の場合のサンプル
    const headers: HttpHeaders = new HttpHeaders({
      'Content-Type': 'application/json',
      'accept': 'application/json'
    });
```
### Body作成
```javascript:TypeScript
    //2つ以上の要素は , 区切り
    const body = {
      token: <<body内容>>
    };
```

### POST作成
```javascript:TypeScript
    //Consulter情報取得のサンプル
    return this.http.post<IConsulter>(AppConfig.apiEndpoint + '/consulters/profile', body, { headers: headers }).map(response => {
      console.log(response);
      return new Consulter(response.id, response.name, response.mailAddress);
    });
```

## Observerパターン
### .map()

### .subscribe()
```
subscribe(
  (x) => console.log(x),                    // onNext
  (error: Error) => console.error(error),   // onError
  () => console.log('Completed!!')          // onComplete
)
```
第一引数の`onNext`は新しい値が流れてきたときに、第二引数の`onError`はストリームの途中でエラーが発生したときに、第三引数の`onComplete`は全ての値が流れきってストリームが終了した時にそれぞれ呼び出されます。

# 参考資料
[ObserverパターンとHelloWorldからはじめるRxJava](https://qiita.com/chooblarin/items/1cb6a58f6e52b8792c52)
