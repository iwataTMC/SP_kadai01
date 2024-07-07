# SP_kadai01

システムプログラミング特論  
課題1  
https://gist.github.com/koyama0612/9725738fc2f2244709c8edce72d19c87


以下、コーディング規約上の問題点についての指摘事項。

1. 行1: モジュールのimportはカンマではなく、別々の行で行う。  
   修正: 
   ```python
   import time
   import random
   ```

2. 行2: 変数名 `sum` は予約語であるため、別の名前を使用する。  
   修正例: `total` などの適切な変数名に変更する。

3. 行3: 変数名 `before` の前後にスペースがない。  
   修正: `before = time.perf_counter()`

4. 行4: forループの後のコロン `:` の前にスペースがある。  
   修正: `for i in range(1000000):`

5. 行5: インデントにスペースが使用されているが、Pythonではタブを使用するのが一般的である。  
   修正: スペースをタブに置き換える。

6. 行5: 変数名 `sum` を適切な名前に変更する。  
   修正例: `total = total + random.randint(1, 100)`

7. 行5: カンマの後にスペースがない。  
   修正: `random.randint(1, 100)`

8. 行6: `time.clock()` は非推奨の関数。代わりに `time.perf_counter()` を使用する。  
   修正: `gaptime = time.perf_counter() - before`

9. 行7: printステートメントの括弧内のカンマの後にスペースがない。  
   修正: `print("gaptime:", gaptime, flush=True)`

10. 行7: `flush` パラメータは `print()` 関数に直接渡すことができる。イコール記号の前後にスペースを追加する。  
    修正: `print("gaptime:", gaptime, flush=True)`

以下、修正後のコード。

```python
import time
import random

total = 0
before = time.perf_counter()
for i in range(1000000):
    total = total + random.randint(1, 100)
gaptime = time.perf_counter() - before
print("gaptime:", gaptime, flush=True)
```
