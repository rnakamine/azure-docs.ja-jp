---
title: 商業マーケットプレースで Dynamics 365 for Operations オファーを作成する
description: Microsoft パートナー センターの商業マーケットプレース ポータルを使用して、Azure Marketplace、AppSource、クラウド ソリューション プロバイダー (CSP) プログラムでリスト登録または販売を行うために新しい Dynamics 365 for Operations オファーを作成する方法。
ms.service: marketplace
ms.subservice: partnercenter-marketplace-publisher
ms.topic: conceptual
author: navits09
ms.author: navits
ms.date: 06/17/2020
ms.openlocfilehash: 79bf5f0d6b7e3fa4735d94c7b26c1736ab25113e
ms.sourcegitcommit: d39f2cd3e0b917b351046112ef1b8dc240a47a4f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/25/2020
ms.locfileid: "88817002"
---
# <a name="create-a-dynamics-365-for-operations-offer"></a>Dynamics 365 for Operations オファーの作成

このトピックでは、新しい Dynamics 365 for Operations オファーの作成方法について説明します。 [Microsoft Dynamics 365 for Finance and Operations](https://dynamics.microsoft.com/finance-and-operations) は、高度な財務、経営、製造、サプライ チェーン管理がサポートされるエンタープライズ リソース プランニング (ERP) サービスです。 Dynamics 365 for Operations のすべてのオファーは、弊社の認定プロセスを通過する必要があります。

開始する前に、まだ[パートナー センターで商業マーケットプレース アカウントを作成](create-account.md)していなければ、作成してください。 ご利用のアカウントを確実に商業マーケットプレース プログラムに登録します。

>[!NOTE]
> オファーが公開されると、オファーに対する編集は、パブリケーションのためにオファーを再送信した後、パートナー センターとオンライン ストアでのみ更新されます。

## <a name="create-a-new-offer"></a>新しいオファーを作成する

1. [パートナー センター](https://partner.microsoft.com/dashboard/home)にサインインします。
2. 左側のナビゲーション メニューで、 **[商業マーケットプレース]**  >  **[概要]** の順に選択します。
3. [概要] ページで、 **[+ 新しいプラン]**  >  **[Dynamics 365 for Operations]** の順に選択します。

    ![左側のナビゲーション メニューの画像。](./media/new-offer-dynamics-365-operations.png)

> [!NOTE]
> オファーを公開した後にパートナー センターで編集した内容がオンライン ストアに表示されるのは、オファーを再公開した後のみです。 変更後は必ず再公開してください。

## <a name="new-offer"></a>新しいプラン

**[オファー ID]** を入力します。 これは、アカウントのオファーごとに一意の識別子です。

- この ID は、マーケットプレース オファーの Web アドレスと Azure Resource Manager テンプレート (該当する場合) で顧客に表示されます。
- 使用できるのは小文字と数字だけです。 ハイフンとアンダースコアを含めることができますが、スペースは使用できず、文字数は 50 文字に制限されています。 たとえば、ここに「**test-offer-1**」と入力すると、オファーの Web アドレスは `https://azuremarketplace.microsoft.com/marketplace/../test-offer-1` になります。
- **[作成]** を選択した後で、オファー ID を変更することはできません。

**[オファーのエイリアス]** を入力します。 これは、パートナー センター内でオファーに使用される名前です。

- この名前はマーケットプレースでは使用されず、顧客に表示されるオファー名やその他の値とは異なります。

**[作成]** を選択してオファーを生成し、続行します。

## <a name="offer-setup"></a>オファーのセットアップ

### <a name="how-do-you-want-potential-customers-to-interact-with-this-listing-offer"></a>潜在顧客がこの登録オファーとやり取りする方法について選択してください。

このオファーに使用するオプションを選択します。

#### <a name="get-it-now-free"></a>Get it now (今すぐ入手する) (無料)

顧客に対して、プランを無料で使用できるものとしてリスト登録します。そのために、アプリにアクセスできる有効な (*http* または *https* で始まる) URL を指定します。  たとえば、`https://contoso.com/my-app` のように指定します。

#### <a name="free-trial-listing"></a>Free trial (無料試用版) (一覧)

顧客が試用版を入手できる有効な (`http` または `https` で始まる) URL を示すことにより、無料試用版へのリンクを使用して顧客にオファーを一覧表示します。 たとえば、「 `https://contoso.com/trial/my-app` 」のように入力します。 オファー登録情報の無料試用版がご利用のサービスによって作成、管理、および構成され、Microsoft によって管理されるサブスクリプションはありません。

> [!NOTE]
> 試用版リンクからアプリケーションが受信するトークンは、そのアプリのアカウント作成を自動化するためのユーザー情報を Azure Active Directory (Azure AD) を介して取得するためだけに使用できます。 このトークンを使用した認証には、Microsoft アカウントはサポートされません。

#### <a name="contact-me"></a>[Contact me (お問い合わせ)]

顧客関係管理 (CRM) システムに接続して、顧客の連絡先情報を収集します。 顧客は、自分の情報を共有する許可を求められます。 これらの顧客の詳細は、オファーの名前と ID のほか、顧客がオファーを見つけたマーケットプレース ソースと一緒に、お客様が構成した CRM システムに送信されます。 CRM の構成の詳細については、「[潜在顧客](#customer-leads)」を参照してください。

### <a name="test-drive"></a>体験版

体験版は、購入前に試用するオプションを提供することで潜在顧客へのオファーを披露し、その結果、コンバージョンが増加し、見込みの高いリードが生成される優れた方法です。 詳細については、まず「[体験版とは](../what-is-test-drive.md)」をご覧ください。

一定期間、体験版を有効にするには、 **[体験版を有効にする]** チェック ボックスをオンにします。 オファーから体験版を削除するには、このチェック ボックスをオフにします。

### <a name="customer-leads"></a>潜在顧客

[!INCLUDE [Connect lead management](./includes/connect-lead-management.md)]

詳しくは、[リード管理の概要](./commercial-marketplace-get-customer-leads.md)に関する記事をご覧ください。

続行する前に、 **[下書きの保存]** を選択します。

## <a name="properties"></a>Properties

このページでは、マーケットプレース上でのオファーのグループ分けに使用するカテゴリと業界、アプリのバージョン、オファーがサポートされる法的契約を定義できます。

### <a name="category"></a>カテゴリ

オファーを適切なマーケットプレース検索領域に配置するために、カテゴリとサブカテゴリを選択します。 オファーでこれらのカテゴリがどのようにサポートされるかを、必ずオファーの説明に記述してください。 選択:

- 少なくとも 1 つ、最大で 2 つのカテゴリ。プライマリ カテゴリとセカンダリ カテゴリを含みます (省略可能)。
- プライマリ カテゴリ、セカンダリ カテゴリ、またはその両方についてそれぞれ最大 2 つのサブカテゴリ。 オファーに適用できるサブカテゴリがない場合は、 **[該当なし]** を選択します。

「[オファーの掲載のベスト プラクティス](../gtm-offer-listing-best-practices.md)」でカテゴリとサブカテゴリの完全な一覧を参照してください。

### <a name="industry"></a>業界

[!INCLUDE [Industry Taxonomy](./includes/industry-taxonomy.md)]

### <a name="app-version"></a>アプリのバージョン

オファーのバージョン番号を入力します。 顧客にはオファーの詳細ページにこのバージョンが表示されます。

### <a name="terms-and-conditions"></a>使用条件

**[使用条件]** フィールドに、独自の法的な使用条件を入力します。 使用条件を見つけることができる URL を指定することもできます。 顧客は、オファーを試す前にこれらの条件を承諾する必要があります。

続行する前に、 **[下書きの保存]** を選択します。

## <a name="offer-listing"></a>オファーのリスト登録

このページに、オファーが登録される言語が表示されます。 現時点では、使用可能なオプションは **[英語 (米国)]** のみです。

言語/市場ごとにマーケットプレースの詳細 (オファーの名前、説明、画像など) を定義する必要があります。 この情報を提供する言語/市場名を選択します。

> [!NOTE]
> オファー登録情報のコンテンツ (説明、ドキュメント、スクリーンショット、使用条件など) は、オファーの説明が「このアプリケーションは、[英語以外の言語] でのみ利用可能です。」という文言で始まっていれば英語である必要はありません。 また、オファー登録情報のコンテンツで使用されている言語以外の言語でコンテンツを提供するための*役に立つリンクの URL* を提供することもできます。

Microsoft AppSource でのオファー情報の表示例を次に示します。

:::image type="content" source="media/example-azure-marketplace-d365-operations.png" alt-text="Microsoft AppSource でこのオファーがどのように表示されるかを示しています。":::

#### <a name="call-out-descriptions"></a>コールアウトの説明

1. ロゴ
2. 製品
3. Categories
4. 業界
5. サポートのアドレス (リンク)
6. 使用条件
7. プライバシー ポリシー
8. プラン名
9. スクリーンショット/ビデオ
10. 説明

### <a name="name"></a>名前

ここで入力する名前は、オファー登録情報のタイトルとして顧客に表示されます。 このフィールドには、オファーの作成時に **[オファーの別名]** に入力したテキストが事前に設定されていますが、この値は変更できます。 この名前は商標の場合もあります (商標または著作権マークを含めることもできます)。 名前は 50 文字以下にする必要があります。絵文字を含めることはできません。

### <a name="short-description"></a>簡単な説明

オファーの簡単な説明を最大 100 文字で入力します。 この説明は、マーケットプレースの検索結果で使用される場合があります。

### <a name="description"></a>説明

[!INCLUDE [Long description-1](./includes/long-description-1.md)]

[!INCLUDE [Long description-2](./includes/long-description-2.md)]

[!INCLUDE [Rich text editor](./includes/rich-text-editor.md)]

### <a name="search-keywords"></a>キーワード検索

オファーを顧客がマーケットプレースで検索できるように、必要に応じて最大 3 つの検索キーワードを入力することができます。 最良の結果を得るには、これらのキーワードを説明にも使用するようにします。

### <a name="products-your-app-works-with"></a>アプリが対応する製品

アプリが特定の製品で動作することを顧客に知らせる場合は、ここに製品名を 3 つまで入力します。

### <a name="support-urls"></a>サポート URL

このセクションには、顧客がオファーの詳細を理解するのに役立つリンクを入力できます。

#### <a name="help-link"></a>ヘルプ リンク

顧客がオファーの詳細について確認できる URL を入力します。

#### <a name="privacy-policy-url"></a>[プライバシー ポリシーの URL]

自分の組織のプライバシー ポリシーへの URL を入力します。 プライバシーに関する法律および規制にアプリが準拠していることを保証し、有効なプライバシー ポリシーを提供する責任があります。

### <a name="contacts"></a>連絡先

このセクションでは、**サポートの連絡先**と**エンジニアリングの連絡先**の名前、メール、電話番号を入力します。 この情報は顧客には表示されませんが、Microsoft で利用できるようになり、CSP パートナーに提供される場合もあります。

**[サポートの連絡先]** セクションに、CSP パートナーがオファーのサポートを確認できる**サポート URL** を指定します。

### <a name="supporting-documents"></a>サポート ドキュメント

ここには、関連するマーケティング ドキュメント (ホワイト ペーパー、パンフレット、チェックリスト、プレゼンテーションなど) を 1 つ以上 (3 つまで) 入力します。 これらのドキュメントは、PDF 形式である必要があります。

### <a name="marketplace-images"></a>マーケットプレースの画像

このセクションでは、顧客にオファーを表示するときに使用されるロゴや画像を指定できます。 画像はすべて .png 形式である必要があります。

[!INCLUDE [logotips](../includes/graphics-suggestions.md)]

>[!Note]
>ファイルのアップロードで問題が発生した場合は、パートナー センターで使用されている https://upload.xboxlive.com サービスがローカル ネットワークでブロックされていないことを確認してください。

#### <a name="store-logos"></a>ストア ロゴ

**大**サイズのロゴに PNG ファイルを指定します。 パートナー センターでは、これを使用して、**小**サイズのロゴを作成します。 これは、必要に応じて、後で別の画像に置き換えることができます。

- **大** (216 x 216 から 350 x 350 px、必須)
- **小** (48 x 48 px、省略可能)

これらのロゴは、リスト登録のさまざまな場所で使用されます。

[!INCLUDE [logos-appsource-only](../includes/logos-appsource-only.md)]

[!INCLUDE [Logo tips](../includes/graphics-suggestions.md)]

#### <a name="screenshots"></a>Screenshots (スクリーンショット)

オファーがどのように動作するかを示すスクリーンショットを追加します。 少なくとも 1 つのスクリーンショットが必要です。最大 5 つまで追加できます。 スクリーンショットはすべて、1280 x 720 ピクセルにする必要があります。

#### <a name="videos"></a>ビデオ

必要に応じて、オファーをデモンストレーションするビデオを最大 4 つ追加することもできます。 これらのビデオは、YouTube または Vimeo でホストされている必要があります。 それぞれのビデオについて、ビデオの名前、URL、ビデオのサムネイル画像 (1280 x 720 ピクセル) を入力します

#### <a name="additional-marketplace-listing-resources"></a>マーケットプレースのリスト登録に関するその他のリソース

[マーケットプレース オファーのリスト登録に関するベスト プラクティス](../gtm-offer-listing-best-practices.md)

続行する前に、 **[下書きの保存]** を選択します。

## <a name="availability"></a>可用性

このページには、オファーを利用できる場所と方法に関するオプションが表示されます。

### <a name="markets"></a>市場

このセクションでは、オファーを利用できる市場を指定します。 これを行うには、 **[市場の編集]** を選択します。 **[市場の選択]** ポップアップ ウィンドウが表示されます。

既定では、どの市場も選択されていません。 オファーを発行するには、少なくとも 1 つの市場を選択してください。 **[すべて選択]** をクリックして利用可能なすべての市場でオファーを利用できるようにするか、追加する特定の市場を選択します。 完了したら、 **[保存]** を選択します。

ここで選択した内容は、新規購入にのみ適用されます。ユーザーが既に特定の市場でアプリを入手しているときに、後でその市場が削除された場合、その市場で既にオファーを入手したユーザーは引き続きそれを使用できますが、その市場で新しいユーザーがオファーを入手することはできません。

> [!IMPORTANT]
> ここやパートナー センターにこれらの要件が記載されていない場合でも、あらゆる地域の法的要件を満たす必要があります。

すべての市場を選択した場合でも、国や地域によっては、地域の法律や規制、その他の要因により、特定のオファーが一覧表示されない場合があることに注意してください。

### <a name="preview-audience"></a>プレビュー対象ユーザー

オファーをより広範なマーケットプレース オファーに公開する前に、まず、限定された**プレビュー対象ユーザー**に対してオファーを利用できるようにする必要があります。 ここでは、**非表示キー** (小文字と数字のみを使用する任意の文字列) を入力します。 プレビュー対象ユーザーのメンバーは、この非表示キーをトークンとして使用して、マーケットプレースでオファーのプレビューを表示できます。

オファーを利用可能にしてプレビューの制限を解除する準備ができたら、**非表示キー**を削除して再度発行する必要があります。

続行する前に、 **[下書きの保存]** を選択します。

## <a name="technical-configuration"></a>技術的な構成

このページでは、オファーに接続するために使用される技術的な詳細を定義します。 この接続によって、最終顧客がオファーを取得することを選択した場合、Microsoft は最終顧客向けにオファーをプロビジョニングできます。

### <a name="solution-identifier"></a>ソリューション識別子

ソリューションのソリューション識別子 (GUID) を入力します。

ソリューション識別子を検索するには:

1. Microsoft Dynamics Lifecycle Services (LCS) で、 **[ソリューション管理]** を選択します。
2. ソリューションを選択し、 **[パッケージの概要]** で**ソリューション識別子**を探します。 識別子が空白の場合、 **[編集]** を選択してパッケージを再発行してから、もう一度やり直してください。

### <a name="release-version"></a>リリース バージョン

このソリューションが動作する Dynamics 365 for Finance and Operations のバージョンを選択します。

続行する前に、 **[下書きの保存]** を選択します。

## <a name="test-drive-technical-configuration"></a>体験版の技術的な構成

このページでは、購入前に顧客がオファーを試すことができるデモ (体験版) を設定します。 詳細については、「[体験版とは](../what-is-test-drive.md)」をご覧ください。

体験版を有効にするには、[[オファーのセットアップ]](#test-drive) タブで **[体験版を有効にする]** チェック ボックスをオンにします。オファーから体験版を削除するには、このチェック ボックスをオフにします。

体験版の設定が完了したら、 **[下書きの保存]** を選択してから続行します。

## <a name="supplemental-content"></a>補足コンテンツ

このページでは、オファーの検証に役立つ、オファーに関する追加情報を提供できます。 この情報は顧客に表示されることも、マーケットプレースに公開されることもありません。

### <a name="validation-assets"></a>検証アセット

このセクションでは、[カスタマイズ分析レポート (CAR)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/dev-tools/customization-analysis-report) をアップロードします。 このレポートは、事前に定義された一連のベスト プラクティス ルールに基づいて、カスタマイズおよび拡張モデルを分析することによって生成されます。

このファイルは .xls または .xlsx 形式である必要があります。 複数のレポートがある場合は、すべてのレポートを含む .zip ファイルをアップロードできます。

### <a name="does-solution-include-localizations"></a>Does solution include Localization?\(ソリューションにローカライズを含めますか?\)

ソリューションでローカルの標準とポリシーの使用を有効にする場合は、 **[はい]** を選択します (国/地域ごとに必要な異なる給与支払い規則に対応している場合など)。 それ以外の場合は、 **[いいえ]** を選択します。

### <a name="does-solution-enable-translations"></a>Does solution enable translation?\(ソリューションで翻訳を有効にしますか?\)

ソリューション内のテキストを他の言語に翻訳できる場合は、 **[はい]** を選択します。 それ以外の場合は、 **[いいえ]** を選択します。

続行する前に、 **[下書きの保存]** を選択します。

## <a name="publish"></a>発行

### <a name="submit-offer-to-preview"></a>プレビューへのオファーの送信

オファーの必須セクションをすべて入力したら、ポータルの右上隅にある **[レビューと公開]** を選択します。

このオファーを公開するのが初めての場合、以下のことが可能です。

- オファーの各セクションの完了状態を確認する。
    - **[未開始]** – セクションは着手されておらず、完了する必要があります。
    - **[未完了]** - 修正が必要なエラーがセクションにあり、追加の情報を入力する必要があります。 セクションに戻って更新してください。
    - **[完了]** – セクションが完了しています。必須のデータはすべて入力済みであり、エラーはありません。 オファーを送信するには、オファーのセクションがすべて完了状態でなければなりません。
- **[認定の注意書き]** セクションで、アプリの理解に役立つ補足事項に加えて、テストの指示を認定チームに提供し、アプリが確実に正しくテストされるようにします。 テスト手順と最初の発行の完了の詳細については、「[AppSource Dynamics 365 Finance and Operations の機能検証](https://docs.microsoft.com/azure/marketplace/dynamics-365-finance-operations-functional-validation)」を参照してください。
- **[送信]** を選択して、公開するためにオファーを送信する。 お客様が確認して承認できるようにオファーのプレビュー バージョンが利用可能になったら、それを知らせるメールが Microsoft から届きます。 パートナー センターに戻り、オファーに対して **[一般公開する]** を選択して、オファーを一般に公開します。

## <a name="next-step"></a>次のステップ

- [商業マーケットプレースで既存のオファーを更新する](./update-existing-offer.md)
