---
title: "03_Java基礎文法"
emoji: "🖥"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [introduction]
published: true
---
本カリキュラムは、Javaの基礎文を学ぶ上で最低限抑えていて欲しい箇所を抽出したカリキュラムをなります。
本カリキュラムの内容を十分に理解し、基礎知識としての土台があるエンジニアを目指しましょう！

# 1. Java基礎文法

まずは、以下のサンプルをご覧下さい。
以下のコードは「Hello」という文字を単に画面に表示するだけのシンプルな処理となっております。

単語の組み合わせによって処理内容を変えることが出来る為、慣れてくるとソースを複数に分けることで処理内容を複雑に組み替えることができるようになります。

以下の様な文章のことを一般的に「コード」と呼び、 コード全体のファイルのことを「ソース」と呼びます。
また、「class Hello」の最初の { から最後の } までのことは「ブロック」と呼びます。
このような基礎的な用語も合わせて覚えておきましょう。

以降では、サンプルのコードについて解説していきます。

初めて出てくる用語はイメージがつきやすいよう()内に言い換えを記載していきます。

<サンプル>
```
class Hello{
  public static void main(String[] args){
    System.out.println("Hello");
  }
}
```

## 1-1. クラス
「クラス」は特定の目的を達成するのに必要な処理を集めたものです。
{ から } までのブロックの間に、特定の処理を行うためのプログラムを集めたメソッド(機能)や、クラスの中で使用されるデータを保管するためのフィールド(場所)を定義(設定)する。

クラスの定義は以下

```
class クラス名{
  // ...
}
```

## 1-2. メソッド
メソッドはクラスの中で特定の処理を行うために必要なプログラムをまとめたもの
メソッドは先頭に戻り値(void)のデータ型を記述したあとでメソッドの名前を記述する
括弧()の中にはメソッドが呼び出されるときに渡されてくる値を受け取るための引数を記述することができますが、今回は省略。
後の{}内でメソッドが呼び出されたときに行う処理を記述。

戻り値・・・処理の後に帰ってくる計算結果や値のこと
引数・・・処理に対して渡す値。使用して欲しいデータ(値)を処理に指定する際のそのデータ(値)のこと。

メソッドの定義は以下

```
class クラス名{
  void メソッド名(){
    // ..
  }
}
```

## 1-3. フィールド
フィールドはクラスの中でデータの値を保管するために使用するもの。
フィールドの定義は以下

フィールドに格納するデータのデータ型を記述したあとフィールド名を指定する。

```
class クラス名{
  データ型 フィールド名;
}
```

## 1-4. main メソッド

Java で作成したプログラムをコンパイル(変換)して実行した際に最初に呼び出されるメソッド。

コンパイル・・・指定された言語で書かれたプログラムを別の形式や命令に変換する作業のこと

```
public static void main(String[] args){
  // ...
}
```

上記はmainメソッドを作成する上でお決まりの定型文である為、丸暗記しましょう。
また、「System.out.println();」は文字を出力(表示)する際によく利用される定型文なのでこちらも合わせて覚えておきましょう。
使用例は以下のようになります。

<サンプル>
```
System.out.println("Hello"); //()内の文字がコンソールに表示される
```

## 1-5. コメント

プログラムを記述する際にメモ書きを残しておきたい時に利用するのがコメント。
プログラムの実行に何の影響も与えず、記載することできる。

記載方法としては以下の２つ
```
単一行コメント
// コメントを記述する

複数行コメント
/*
コメント記述する
コメント記述する
コメント記述する
*/
```
## 1-6. Javaの予約語

予約語( Keywords )とは Java であらかじめ用途が決めらた単語のこと。予約語は変数名やクラス名などの識別子として使用することができない。

掲載されている予約語の一覧は 51 個。

|            |             |           |            |        |
|------------|-------------|-----------|------------|--------|
| abstract   | assert      | boolean   | break      | byte   |
| case       | catch       | char      | class      | const  |
| continue   | default     | do        | double     | else   |
| enum       | extends     | final     | finally    | float  |
| for        | goto        | if        | implements | import |
| instanceof | int         | interface | long       | native |
| new        | package     | private   | protected  | public |
| return     | short       | static    | strictfp   | super  |
| switch     | synchrnized | this      | throw      | throws |
| transient  | try         | void      | volatile   | while  |

使用例は以下

```
import XXXX
import XXXX
import XXXX

class Xxxx abstract Yyyy{
  public static void main(String[] args){
    int a;
  }
};
```


## 2-1. 変数

変数とは、データを格納する場所。
変数は値を保管する箱のようなものであり、数値や文字列などを保管することができます。
また変数に保管した値を取り出して参照することができる。
利用するには最初に変数という箱を用意する必要。
変数を用意することを「変数の宣言」と呼ぶ。
データによって値の型が違う為、それぞれに合った値の型を一緒に指定する。

変数の定義の仕方は以下
```
値の型　変数名;
```
値の型とは、値にはそれぞれ対応する型が存在し、型に応じた値しか格納することが出来ません。
文字列を格納する際の型であれば、「String(型)」、数字であれば「int(型)」が主に使用されます。
「String」、「int」は非常によく使われる型ですので、覚えておきましょう。

*  変数名(識別子)のルール
```
・変数名には Unicode に含まれる文字が使用できる。
・一文字目に数字は使用できない。
・大文字と小文字は区別される。
・予約語( Keywords )は使用できない。
・文字数の制限はない
・変数名にはアルファベットや数字などの他に全角文字も使用できる。
・日本語の変数名も使用できる。
・記号についてはアンダーバー(_)と $ のみ使用可能。
・最初の文字には数字( 0 ～ 9 )は使用できない。
・予約語( Keywords )とまったく同じ文字列は使用できない。
・メソッド名はすべて小文字。
・複数の文字列をつなげる場合は最初の文字を大文字にしてそのままつなげる。
```

* 変数のイメージ

```
int num;　←int型のnumという変数

char c;　←char型のcという変数
```
変数が用意できたら、値を格納することができる。

```
num = 500;　←変数numに500を格納
c = 'あ';　←変数cに「あ」を格納
```
変数は一つにつき1データのみ格納可能。
新しい値を新たに保管するとそれまで保管していた値が上書きされる為、参照できなくなる。

```
num = 500;
num = 180;　←500と180が置き換わる(180のみ参照可能)
```
変数に格納した値は以下のように利用したりして処理を動かすことができる。

```
System.out.println(num);　
※System.out.printlnはコンソール(cmdなどの黒画面)に値を表示するメソッド
```
この処理を日本語で訳すと、、、

```
出力する(変数numの中身を);
```

というようなイメージとなる
変数numに最後に保管されていた値は180になるので、出力結果は180が表示される

## 2-2. 基本データ型の種類

Java で用意されている基本データ型

| データ型    | 値(値の範囲)                                                      |
|---------|--------------------------------------------------------------|
| boolean | true or false                                                |
| char    | 16ビットUnicode文字 \u0000～\uFFFF                                 |
| byte    | 8ビット整数 -128～127                                              |
| short   | 16ビット整数 -32,768～32,767                                       |
| int     | 32ビット整数 -2,147,483,648～2,147,483,647                         |
| long    | 64ビット整数 -9,223,372,036,854,775,808～9,223,372,036,854,775,807 |
| float   | 32ビット単精度浮動小数点数(およそ10の38乗、10の-45乗)                            |
| double  | 64ビット単精度浮動小数点数(およそ10の308乗、10の-324乗)                          |

整数を扱うデータ型はいくつかあるが、扱える数値の範囲が異なります。
大きな値を扱えるデータ型はその分メモリも多く使用する為、扱う値に応じた適切なデータ型を使用することが大事です。

long 型の変数に数値を代入する場合は末尾に「L」を記述する。

long num;
num = 39433204432234523L;

float 型の変数に数値を代入する場合は末尾に「F」を記述する。

float num;
num = 7.8F;

1 つの文字に対して 1 つの文字コードが割り当てられています。 Unicode では 'a' や 'あ' の文字コードは次の通り。

'a' の文字コードは 0x0061
'あ' の文字コードは 0x3042

そのため、以下の文は同じ処理となります。

char c1 = 'a';
char c2 = 0x0061;