---
copyright:
  years: 1994, 2017
lastupdated: "2017-11-28"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Plesk 9 への SSL 証明書のインストール

Plesk 9 に SSL 証明書を追加するには、以下の手順を実行します。

1. Plesk にログインし、証明書をインストールするドメインに移動します。
2. ターゲット・ドメインの構成に入ります。
3. **「SSL 証明書」**をクリックします。
4. **「SSL 証明書の追加」**をクリックします。

   **注:** 既に SSL 証明書がある場合は、このステップを飛ばして、ステップ 8 に進んでください。
5.  証明書に名前を付けます。どのような名前でも構いませんが、タイム・スタンプを含む記述名を使用すると便利です。

   この場合は、*YYYYMMDDRR* 形式を使用しています。ここで、*RR* は改訂番号 (この場合は、同じ日付の改訂がないので 00) です。
6. SSL 要求に必要な調整を行います。この情報は SSL 証明書に組み込まれるため、ドメインの登録情報と同様でなければなりません。

  E メール・アドレスは、ドメイン登録機関によって情報が提供されたドメイン内の E メール・アドレスの 1 つに一致していなければなりません。

  **重要:** 虚偽の情報は SSL 認証局によって拒否される可能性があります。
7. 証明書の構成に移動して戻ります。
8. CSR と秘密鍵を確認して、秘密鍵を安全な場所に保管します。  

  **注:** サーバーで証明書の再入力を必要とする何かが発生した場合のために、少なくとも証明書と秘密鍵を持っている必要があります。
9. CSR を取得し、選択した認証局に送信します。{{site.data.keyword.cloud_notm}} インフラストラクチャーは SSL 証明書を提供しません。
10. 認証局から証明書を受け取った後、それを証明書のテキスト域に貼り付けることができます。

   **注:**
   * 認証局が要求する場合、認証局独自の証明書を CA 証明書のテキスト域に貼り付けることが必要になります (通常、CA バンドルと呼ばれます)。
   * 証明書を使用するには、一致する秘密鍵と証明書を持っている必要があります。
11. ドメインの構成から *<span style="text-decoration: underline">Web ホスティング設定</span>*に戻ります。
12. 対応する証明書を選択し、**「OK」**をクリックします。

これで、新しい証明書がドメインに使用されるようになりました。証明書を更新した場合は、新しい証明書を使用する前に、ブラウザーを完全にクローズすることが必要な場合があります。
