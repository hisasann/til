# FlowからTypeScriptに移行する

## 主な書き換え

| 書き換え対象 | Flow | TypeScript |
| :---         |     :---:      |          ---: |
| 構造的型の定義 | type Foobar = {...};  | interface Foobar {...}
| null許容型 | ?string | string \| null \| undefined
| 不明な型（型安全） | mixed | unknown
| 読み取り専用のフィールド | +field: string; | readonly field: string;
| 明示的な型指定 | (foobar: any) | (foobar as any)
| 文字列リテラルの共用体型をキーとするオブジェクト | {[Foobars]: string} | {[key in Foobars]: string}
| 関数の戻り値の型 | $Call<...> | ReturnValue<...>

## 参考記事

[自作のOSSライブラリをFlowからTypeScriptに全面移行した理由と所感 - ここぽんのーと](https://cocopon.me/blog/2019/01/tweakpane-flow2ts/)
