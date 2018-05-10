# このソフトウェアについて

Bashで１文字ずつ遅延表示するアニメーション。日本語対応。

# 使い方

```sh
. anim_wait.sh
Wait "表示したい文字列。"
```

## コード

```sh
Wait(){
    local count=0
    while [ $count -lt ${#1} ]; do
        local target="${1:$count:1}"
        echo -n "$target"
        ((count++))
        sleep 0.05
    done
}
```

# 開発環境

* [Raspberry Pi](https://ja.wikipedia.org/wiki/Raspberry_Pi) 3 Model B
    * [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) GNU/Linux 8.0 (jessie)
        * bash 4.3.30

# ライセンス

このソフトウェアはCC0ライセンスである。

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)
