# Kubernetesコントリビューターチートシート

Kubernetesへ貢献する際の一般的なリソース、ヒント、コツ、およびKubernetesプロジェクト内で使用される一般的なベストプラクティスのリストです。
それはあなたのGitHub貢献経験をより良くするするための有益な情報の簡易リファレンスや "TL;DR" です。

**目次**
- [有益なリソース](#有益なリソース)
  - [はじめに](#はじめに)
  - [SIGとその他のグループ](#sigとその他のグループ)
  - [コミュニティ](#コミュニティ)
  - [重要なEメールエイリアス](#重要なeメールエイリアス)
  - [ワークフロー](#ワークフロー)
  - [テスト](#テスト)
  - [その他便利なリンク](#その他便利なリンク)
- [GitHubでの効率的なコミュニケーション](#githubでの効率的なコミュニケーション)
  - [お互いに良くなる方法](#お互いに良くなる方法)
    - [良い/悪いコミュニケーションの例](#良い/悪いコミュニケーションの例)
- [貢献をする](#貢献をする)
  - [CLAの署名](#claの署名)
  - [Issueを作成し対応する](#issueを作成し対応する)
    - [Issueを作成](#issueを作成)
    - [Issueへの対応](#issueへの対応)
  - [Pull Requestを開く](#pull-requestを開く)
    - [Pull Requestの作成](#pull-requestの作成)
    - [PRの概要の例](#prの概要の例)
    - [Pull Requestのトラブルシューティング](#pull-requestのトラブルシューティング)
  - [ラベル](#ラベル)
- [ローカルでの作業](#ローカルでの作業)
  - [ブランチ戦略](#ブランチ戦略)
    - [アップストリーム追加](#アップストリーム追加)
    - [Forkを同期させる](#forkを同期させる)
  - [スカッシュコミット](#スカッシュコミット)

---

## 有益なリソース

### はじめに

- [コントリビューターガイド] - Kubernetesプロジェクトへの貢献の始め方のガイド
- [開発者ガイド] - Kubernetesへのコードへ直接貢献する際のガイド
- [セキュリティと公開情報] - 脆弱性のレポートとセキュリティリリースプロセスについてのガイド

### SIGとその他のグループ

- [マスターグループリスト][sigs]

### コミュニティ

- [カレンダー] - Kubernetesコミュニティのイベントの全て表示(SIG/WGのミーティング、イベントなど)
- [kubernetes-dev] - Kubernetes開発者のメーリングリスト
- [Kubernetesフォーラム] - 公式のKubernetesフォーラム
- [Slackチャンネル] - 公式のKubernetes Slack
- [Stack Overflow] - Kubernetesエンドユーザーが質問をする場所
- [YouTubeチャンネル] - Kubernetesコミュニティの公式チャンネル


### ワークフロー

- [Gubernatorダッシュボード] - 注意が必要な着信と発信のPull Requestの表示
- [Prow] - KubernetesのCI/CDシステム
- [Tide] - マージやテストを管理するProwプラグイン [Tideダッシュボード]
- [Botコマンド] - Kubernetes Botと対話するために使用するコマンド (例: `/cc` 、 `/lgtm` 、や `/retest`)
- [GitHubラベル] - Kubernetesプロジェクト全体で使用されているラベルのリスト
- [Kubernetes Code Search]、[@dims]によってメンテナンスされています


### テスト

- [Prow] - KubernetesのCI/CDシステム
- [テストグリッド] - 過去のテストとそれらに関連する情報の表示
- [トリアージダッシュボード] - より良いトラブルシューティングのために関連する障害のまとめ
- [Velodrome] - ジョブとテストの状態を追跡するためのダッシュボード


### 重要なEメールエイリアス

- community@kubernetes.io - コミュニティの問題についてはコミュニティチーム(SIG Contributor Experience)の誰かへメールしてください
- conduct@kubernetes.io - 行動規範委員会の連絡先、プライベートなメーリングリスト
- steering@kubernetes.io - 運営委員会への連絡先。公開アーカイブ付きの公開アドレス
- steering-private@kubernetes.io - 運営委員会へのプライベートな連絡先、機密扱いな内容向け
- social@cncf.io - CNCFのソーシャルチームへの連絡先。ブログ、Twitterアカウントやその他の社会的財産について


### その他便利なリンク

- [開発者統計] - CNCFで管理されている全てのプロジェクトについての開発者統計の表示

---

## GitHubでの効率的なコミュニケーション


### お互いに良くなる方法

まず最初のステップとして、行動規範を理解しましょう。


#### 良い/悪いコミュニケーションの例

問題提起したり、援助を求める際は、要求を丁寧に伝えましょう:

  🙂 “YをしたときにXXをコンパイルできなかったのですが、何か提案はありますか？”

  😞 “XXが動きません！修正してください！”

PRを閉じる時、なぜそれがマージされるべき要件を満たさないかという説明を
丁寧なメッセージで伝えてください。

🙂 “この機能はXというユースケースでサポートできないためこのPRを閉じます。
   その提案での方式では、Yツールを使って実装したほうが良いでしょう。
   この作業に取り組んでくれてありがとうございます。”

😞 “なぜこれはAPIの規約に従っていないのですか？これは他でやるべきです！”

---

## 貢献をする

### CLAの署名

貢献をする前に、[Contributor License Agreement(CLA)に署名][cla]しなければなりません。
Kubernetesプロジェクトはあなた、もしくはあなたの企業がCLAに署名した場合 _だけ_ 
貢献を受けることができます。

CLAに署名する際に問題が発生した場合には、[CLAトラブルシューティングガイドライン]に従ってください。


### Issueを作成し対応する

GitHub Issueはバグ報告や機能拡張の要求、またはテスト失敗などの他の問題の報告などを追跡するための主要な手段です。
それらは[ユーザーサポートリクエスト]を意図して **いません** 。
それらの場合は[トラブルシューティングガイド]を確認し、[Stack Overflow]へ問題を報告するか
[Kubernetesフォーラム]で追求してください。

**参考文献:**
- [ラベル]
- [Prowコマンド][commands]


#### Issueを作成

- Issueテンプレートがある場合はそれを使用します。
  正しいテンプレートを選択すると他のコントリビューターが対応する際に役立ちます。
  - Issueテンプレート自体に記載されている支持に従ってください。
- あなたが提起している問題を説明してください。 
- 適切な[ラベル]を割り当てます。わからない場合は[k8s-ci-robot][prow]ボット
  ([Kubernetes CIボット][prow])が効果的にトリアージするために必要なラベル
  を付けてIssueへ返信します。
- [`/assign @<username>`][assign]や[`/cc @<username>`][cc]を使って
  Issueを割り当てる際は選択的にしてください。Issueは多くの人を割り当てるよりも、
  より効果的に正しいラベルを割り当てことでトリアージされます。


#### Issueへの対応

- Issueに取り組む際、重複した作業を避けるために自分が取り組んでいることを
  他の人に知らせてください。
- あなたが将来自分自身で何かを解決した際は、Issueを閉じる前にIssueで人々に知らせてください。
- 他のPRをやIssue(またはアクセス可能な資料)への参照を含めてください。
  例: _"ref: #1234"_ 。関連する作業が他の場所で扱われたことを確認することは有用です。


### Pull Requestを開く

Pull Request(PR)はgitリポジトリに保存されているコードやドキュメント、
その他の作業を寄稿する主な手段です。

**参考文献:**
- [ラベル]
- [Prowコマンド][commands]
- [Pull Requestのプロセス]
- [GitHubワークフロー]


#### Pull Requestの作成

- 利用可能な場合、Pull Requestテンプレートの指示に従います。
  それはあなたのPRに対応する人々の助けになります。
- リンク切れやタイプミス、文法の間違いなどの[簡単な修正]の場合、
  他の可能性のある間違いについてドキュメント全体を見直してください。
  同じドキュメントの小さな修正で複数のPRを作成しないでください。
- PRに関連するIssueやPRで解決する可能性があるIssueを参照してください。
- 一度のコミットで過大な変更を加えないでください。
  代わりに、PRを複数の小さなコミットに分割してください。
  これによりPRのレビューが容易になります。
- 何か説明を加える必要があると思われる場合は、PRにコメントしてください。
- [`/assign @<username>`][assign]でPRに割り当てるときは選択的にしてください。
  過剰なレビュー担当者を割り当てたからといって、 迅速なレビューが得られるわけではありません。
- あなたのPRが _"進行中"_ とされる場合、名前の前に `[WIP]` を付けるか、
  [`/hold`][hold]コマンドを使用してください。これは `[WIP]` またはHoldが解除されるまで
  PRがマージされるのを防ぎます。
- あなたのPRがレビューされてない場合に、閉じて同じ変更のPRを新しく作成しないでください。
  `@<github username>` とコメントでレビュアーにPingしてください。
  

#### PRの概要の例

```
Ref. #3064 #3097
All files owned by SIG testing were moved from `/devel` to the new folder `/devel/sig-testing`.

/sig contributor-experience
/cc @stakeholder1 @stakeholder2
/kind cleanup
/area developer-guide
/assign @approver1 @approver2 @approver3
```

PRの内容:
- **1行目** - 他のIssueやPRへの参照(#3064 #3097)
- **2行目** - PRで行われていることの簡単な説明
- **4行目** - `/sig contributor-experience` [コマンド][commands]での
  [SIG][sigs]の割り当て
- **5行目** - この特定のIssueやPRに関心があるレビュアーを[`/cc`][cc]コマンドで指定
- **6行目** - [`/kind cleanup`][kind]コマンドでコードやプロセス、技術的負債の整理
  に関してIssueやPRを分類する[ラベル][ラベル]を追加
- **7行目** - [`/area developer-guide`][kind]コマンドで開発者ガイドに関して
  IssueやPRを分類
- **8行目** - [`/assign`][assign]コマンドでPRにApproverを割り当て。
  Approverは[k8s-ci-robot][prow]によって提案され、[OWNERS]ファイルのオーナーの
  リストから選択される。
  彼らはレビューされた後のPRに[`/approve`][approve]ラベルを追加するだろう


#### Pull Requestのトラブルシューティング

PRが作成された後、KubernetesのCIプラットフォームの[Prow]によって一連のテスト
が実行されます。テストのいずれかが失敗した場合、[k8s-ci-robot][prow]は
失敗したテストへのリンクと有効なログをPRに返信します。

新しいコミットをPRにがプッシュすると、自動的にテストが再実行されます。

時折KubernetesのCIプラットフォームに問題がある場合があります。
あなたの貢献が全てのローカルテストに合格したとしても、
これらは様々な理由で発生する場合があります。`/retest` コマンドでテストを
再実行することができます。

特定のテストのトラブルシューティングの詳細については[テストガイド]を参照してください。


### ラベル

KubernetesはIssueとPull Requestを分類し、トリアージするために[ラベル]を使用します。
正しいラベルを付けることであなたのIssueやPRをより効果的にトリアージすることができます。

**参考文献:**
- [ラベル]
- [Prowコマンド][commands]

よく使用されるラベル:
- [`/sig <sig name>`][kind]はIssueやPRの所有権を[SIG][SIGs]に割り当てます。
- [`/area <area name>`][kind]はIssueやPRを特定の[エリア][ラベル]に関連付けます。
- [`/kind <category>`][kind]はIssueやPRを分類します。

---

## ローカルでの作業

Pull Requestを作成する前に、ローカルである程度の作業を行う必要があります。
もしあなたがgitに慣れていない場合、[Atlassian gitチュートリアル]は良い出発点です。
他に、Stanfordの[Git magic]チュートリアルは多言語に対応しています。

**References:**
- [Atlassian gitチュートリアル]
- [Git magic]
- [GitHubワークフロー]
- [ローカルでのテスト]
- [開発者ガイド]


### ブランチ戦略

KubernetesプロジェクトはGitHubの標準である _"Fork and Pull"_ ワークフローを使います。
gitの用語で、あなたの個人的なフォークは _"`origin`"_ と呼ばれ、実際のプロジェクトの
gitリポジトリのことを _"`upstream`"_ と呼ばれます。
あなたの個人的なブランチ(`origin`)をプロジェクト(`upstream`)の最新に保つために、
ローカルの作業コピー内で設定されてなければなりません。


#### アップストリームの追加

`upstream` をリモートとして追加し、プッシュできないように設定してください。

```
# replace <upstream git repo> with the upstream repo url
# example:
#  https://github.com/kubernetes/kubernetes.git
#  git@github.com/kubernetes/kubernetes.git

git remote add upstream <upstream git repo>
git remote set-url --push upstream no_push
```

これは設定したリモートを一覧表示する `git remote -v` を実行して確認することができます。


#### Forkを同期させる

`upstream` から全ての変更を取得し、ローカルの `master` ブランチに _"rebase"_ します。
これはローカルのリポジトリを `upstream` プロジェクトと同期させます。

```
git fetch upstream
git checkout master
git rebase upstream/master
```

あなたは機能への取り組みや修正をするためにブランチを作成する前に、
最低限これをやるべきです。

```
git checkout -b myfeature
```

#### スカッシュコミット

[スカッシュコミット]の主な目的はきれいに読めるgitの履歴や加えられた変更のログ
を作成することです。通常これはPRの改定の最終段階に行われます。
コミットをスカッシュするべきかわからない場合は、作業を止めてPRのレビューと承認
を担当する他のコントリビューターの判断に任せることをおすすめします。


[コントリビューターガイド]: /contributors/guide/README.md
[開発者ガイド]: /contributors/devel/README.md
[Gubernatorダッシュボード]: https://gubernator.k8s.io/pr
[prow]: https://prow.k8s.io
[tide]: http://git.k8s.io/test-infra/prow/cmd/tide/pr-authors.md
[tideダッシュボード]: https://prow.k8s.io/tide
[Botコマンド]: https://go.k8s.io/bot-commands
[GitHubラベル]: https://go.k8s.io/github-labels
[Kubernetes Code Search]: https://cs.k8s.io/
[@dims]: https://github.com/dims
[カレンダー]: https://calendar.google.com/calendar/embed?src=cgnt364vd8s86hr2phapfjc6uk%40group.calendar.google.com
[kubernetes-dev]: https://groups.google.com/forum/#!forum/kubernetes-dev
[slackチャンネル]: http://slack.k8s.io/
[Stack Overflow]: https://stackoverflow.com/questions/tagged/kubernetes
[youtubeチャンネル]: https://www.youtube.com/c/KubernetesCommunity/
[トリアージダッシュボード]: https://go.k8s.io/triage
[テストグリッド]: https://testgrid.k8s.io
[Velodrome]: https://go.k8s.io/test-health
[開発者統計]: https://k8s.devstats.cncf.io
[行動規範]: /code-of-conduct.md
[ユーザーサポートリクエスト]: /contributors/guide/issue-triage.md#determine-if-its-a-support-request
[トラブルシューティングガイド]: https://kubernetes.io/docs/tasks/debug-application-cluster/troubleshooting/
[Kubernetesフォーラム]: https://discuss.kubernetes.io/
[Pull Requestのプロセス]: /contributors/guide/pull-requests.md
[GitHubワークフロー]: /contributors/guide/github-workflow.md
[Prow]: https://git.k8s.io/test-infra/prow#prow
[cla]: /CLA.md#how-do-i-sign
[CLAトラブルシューティングガイドライン]: /CLA.md#troubleshooting
[commands]: https://prow.k8s.io/command-help
[kind]: https://prow.k8s.io/command-help#kind
[cc]: https://prow.k8s.io/command-help#cc
[hold]: https://prow.k8s.io/command-help#hold
[assign]: https://prow.k8s.io/command-help#assign
[SIGs]: /sig-list.md
[テストガイド]: /contributors/devel/sig-testing/testing.md
[ラベル]: https://git.k8s.io/test-infra/label_sync/labels.md
[簡単な修正]: /contributors/guide/pull-requests.md#10-trivial-edits
[GitHubワークフロー]: /contributors/guide/github-workflow.md#3-branch
[スカッシュコミット]: /contributors/guide/pull-requests.md#6-squashing-and-commit-titles
[owners]: /contributors/guide/owners.md
[ローカルでのテスト]: /contributors/guide/README.md#testing
[Atlassian gitチュートリアル]: https://www.atlassian.com/ja/git/tutorials
[git magic]: http://www-cs-students.stanford.edu/~blynn/gitmagic/
[セキュリティと公開情報]: https://kubernetes.io/docs/reference/issues-security/security/
[approve]: https://prow.k8s.io/command-help#approve
