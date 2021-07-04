---
title: GitHub Insightsで利用できるメトリクス
product: '{% data reusables.gated-features.github-insights %}'
intro: '{% data variables.product.prodname_insights %}には、チームのソフトウェアデリバリのプロセスを可視化してくれる様々なメトリクスが含まれています。'
redirect_from:
  - /github/installing-and-configuring-github-insights/metrics-available-with-github-insights
  - /github/installing-and-configuring-github-insights/key-metrics-for-collaboration-in-pull-requests
versions:
  enterprise-server: '*'
---

### {% data variables.product.prodname_insights %}内のメトリクスについて

{% data reusables.github-insights.key-metrics-and-reports %}

{% data reusables.github-insights.about-key-metrics %} それぞれの主要なメトリクスについて、目標を設定して計測できます。 詳しい情報については「[目標の管理](/insights/installing-and-configuring-github-insights/managing-goals)」を参照してください。

{% data reusables.github-insights.about-reports %}

{% data reusables.github-insights.manage-metrics %}

### プルリクエストにおけるコラボレーションのための主要なメトリクス

プルリクエストにおけるコラボレーションのための主要なメトリクスは、チームがプロセスにおけるボトルネックを取り除き、コラボレーションを改善し、より素早く高品質でプロジェクトをデリバリすることを支援します。 これらのメトリクスを改善する事で、チームの生産性が高まります。

- [コードレビューの分布](#code-review-distribution)
- [コードレビューのターンアラウンド](#code-review-turnaround)
- [オープンまでの時間](#time-to-open)
- [プルリクエストのサイズ](#pull-request-size)
- [進行中の作業](#work-in-progress)

#### コードレビューの分布

チームあるいはOrganizationにわたるコードレビューの分布を計測します。 値が1に近ければ、分布が均等になっているということです。 以前にプルリクエストのオープン、レビュー、コミットをしたメンバーや、ブランチにコミットしたメンバーが含まれます。

この指数は、1からOrganizationあるいはチームのコードレビューのジニ係数を引いた値に等しくなります。 詳しい情報については、Wikipediaの[ ジニ係数](https://ja.wikipedia.org/wiki/ジニ係数)を参照してください。

#### コードレビューのターンアラウンド

レビューの割り当てから完了までにかかった時間です。

チームにとっての阻害要因としてのコードレビューに対処するために、Organizationはレビューの割り当てプロセスを最適化し、ターンアラウンド時間の目標を設定できます。

#### オープンまでの時間

ユーザがブランチに初めてコミットしてから、そのブランチに対するプルリクエストをオープンするまでの時間です。

この期間を短縮すれば、コントリビューターはプロセス中でフィードバックを早く受け取れるようになり、コラボレーションやイテレーションの時間を増すことができます。

#### プルリクエストのサイズ

プルリクエストの総差分サイズ（追加、削除、変更された行数の合計）。

大きなプルリクエストは、プロダクションへのデプロイに際してのリスクが大きくなり、レビュー、マージ、リリースが難しくなります。 適切なサイズのプルリクエストをデプロイすることで、チームは新しい機能を高頻度で自信を持ってレビューし、出荷できます。

#### 進行中の作業

指定されたチームもしくはOrganizationのオープンなプルリクエスト数で、開発者に対するオープンなプルリクエストの総数及び比率として表されます。

プルリクエストのバックログが大きくなっているということは、作業が最新の状態ではなくなっているかもしれず、チームの作業が無駄になっているかもしれないことを示します。 このメトリクスは、チームの誰もが阻害されたり過負荷になっていないようにしながら、チームが集中していられるよう支援します。

### 報告

| メトリック                        | 説明                                                                                                       |
| ---------------------------- | -------------------------------------------------------------------------------------------------------- |
| アクティビティ                      | アクティビティは以下のいずれかです。<ul><li>ブランチへのコミット</li><li>プルリクエストのオープン</li><li>プルリクエストをクローズする</li><li>プルリクエストをマージする</li><li>プルリクエストへコメントする</li><li>プルリクエストの承認</li></ul>                                                              |
| アクティビティ、時間                   | アクティビティのあった1時間は、少なくとも1人のコントリビューターがアクティビティを記録した1時間です。                                                     |
| チャーンコード                      | チャーンコードは、追加あるいは最後の変更から3週間以内の変更されたコードです。 これには、作者あるいは他のコントリビューターによって上書きされたコードの行が含まれます。                     |
| 追加及び変更されたコードの行               | 新たに追加された行数に変更された行数を加えた合計。 チャーンコードを含めることも、除外することもできます。                                                    |
| 所有権                          | 追加もしくは変更されたコードの各行に対する、最終のコントリビューターによって追加あるいは変更されたコードの行のパーセンテージの分析。                                       |
| ペアリング                        | 他のコントリビューターのコードを変更あるいは削除したコントリビューター。                                                                     |
| コードベースの変更のパーセンテージ            | コードベース中のコードの総行数に対するパーセンテージで表した、コードベース内の追加あるいは変更されたコード行数。                                                 |
| 新規及び変更コードのチャーンコードに対するパーセンテージ | チャーンコードを除いた、追加及び変更されたコードの行数の、チャーンコードを含む追加及び変更されたコードの総行数に対するパーセンテージ。                                      |
| オープンなプルリクエスト                 | 選択された期間、あるいはチャートに表示された期間の終わりの時点でオープンになっているすべてのプルリクエスト数。                                                  |
| リテンション                       | 行が作成された週ごとにグループ化した、各週の後にコードベース中で保持されたコードの行数のパーセンテージ。                                                     |
| マージまでの時間                     | ブランチへの最初のコミットと、そのブランチ上でのプルリクエストのマージアクションとの間の時間。 ブランチ上での最初のコミットのタイムスタンプが、プルリクエストのマージアクションのタイムスタンプから引かれます。 |