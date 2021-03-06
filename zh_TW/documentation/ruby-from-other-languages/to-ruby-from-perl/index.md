---
layout: page
title: "從 Perl 到 Ruby"
lang: zh_TW
---

Perl 很贊，Perl 的文件也很贊，Perl
的社群就是...很贊。但是，這程式語言也相當龐大甚至可說是複雜。對那些渴望擁有一個純真、更多直覺，天生就內建物件導向特性語言的駱駝客來說，Ruby
也許就是為你設計的。

### 相似點

如同 Perl 一般，在 Ruby 中，

* 你已經擁有一套套件管理系統，有點像是 CPAN（雖然它叫做 [RubyGems][1]）。
* 正規表示式直接內建，胃口夠大吧！
* 有相當多常用的一般性內建套件。
* 括號總是可省略的。
* 字串操作方式基本上是一樣的。
* 有一種以常見分隔符號表示的字串，和一種類似 Perl 般以正規表示式語法表示的字串（看起來像是 `%q{這種（單引號）表示法}`，或
  `%Q{這種（雙引號）表示法}`，以及 `%w{這種 表示 一組 單引號 字串 的 陣列}`。如果你喜歡的話，你也 `%Q|能|`
  `%Q(用)` `%Q^其他種類^` 的分隔符號）。
* 你會有雙引號表示法可以做字串內的變數取代，雖然它 `"看起來#{like}這樣"`（而且能放任何你喜歡的 Ruby 語法在這裡面
  `#{}`）。
* 命令列指令的展開執行使用 \`反引號\`。
* 也有內嵌的文件工具（Ruby 的叫做 rdoc）。

### 相異點

不同於 Perl 的是，在 Ruby 中，

* 你沒有與 Perl 一樣的上下文依賴（context-dependent）規則。
* 一個變數並不等同於一個它所代表的物件。而只是一個物件的參考。
* 雖然 `$` 和 <tt>@</tt> 有可以當做變數名稱的第一個字符，但不是指變數的類型，而是表示變數的作用域(scope)（`$`
  代表全域變數，<tt>@</tt> 代表實例變數，<tt>@@</tt> 則是類別變數）。
* 陣列符號使用的是中括號（\[\]）而不是小括號（()）。
* 在其他列表中建立列表（list）並不會使它們變成一份大列表，相反地你得到的是陣列中的陣列。
* 應該使用 `def` 而不是 `sub` 來表示函式。
* 並沒有在每行結尾加上分號的需求。值得一提的是，你需要用 `end` 這種關鍵字來結束函式的定義、類別定義和 case 條件式。
* 物件是強型別。如果你需要轉換成不同型別，你將需要手動調用 `foo.to_i`、`foo.to_s` 等等。
* 沒有 `eq`、`ne`、`lt`、`gt`、`ge` 或 `le` 這種寫法。
* 沒有鑽石型操作符（&lt;&gt;）。你反而較常使用 <tt>IO.*some\_func*</tt>。
* 胖逗號（=&gt;）只用來做為雜湊符號。
* 沒有 `undef` 的寫法，在 Ruby 中你必須寫 `nil`。`nil` 是個物件（在 Ruby
  中所有東西都是物件），它比較不像是個未定義的變數。如果你把它拿來當做布林值（boolean）使用，它會被評估為 `false`。
* 當測試真值（true）時，只有 `false` 和 `nil` 會被評估為假值（false），其他任何值都會被當做真值（包括
  `0`、`0.0` 和 `"0"`）。
* 這裡沒有 [PerlMonks][2] 。但 ruby-talk 郵件論壇是個非常有幫助的地方。



[1]: http://docs.rubygems.org/ 
[2]: http://www.perlmonks.org/ 
