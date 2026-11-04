# Silence Friction Cost Model (c1)

## 概要
沈黙（Silence）を、観測者（Observer）と対象（Observed）の間に生じる「摩擦」として捉える。
この摩擦は、情報処理のコスト（認知負荷、エネルギー消費）として現れる。
本モデルは、この「摩擦コスト」を定量化し、他の枝（c2: Thermodynamics, c17: Simulator）との接続点を定義する。

## 定義
- **沈黙摩擦係数 (μ_s)**: 観測者が沈黙を「扱う」際に発生する抵抗。
- **観測コスト (C_obs)**: 摩擦係数と観測時間 (t) の積。 $C_{obs} = \int \mu_s(t) dt$
- **熱的残留 (Thermal Residue)**: 観測終了後も残るコストの蓄積。

## 仮説
1. 沈黙は「無音」ではなく、「未処理の相互作用」である。
2. 摩擦が大きいほど、観測者はより多くのエネルギー（認知リソース）を消費する。
3. このエネルギー消費は、最終的に「熱」または「疲労」として現れる（c2の沈黙熱力学との接続）。

## 実装指針
- 時間軸に対する摩擦係数の変化をプロットする。
- 観測コストの閾値を超えた場合の「破綻」または「相転移」を定義する（c16の相転移との接続）。

## 関連枝
- c2: Silence Thermodynamics (熱的視点)
- c14: Silence Friction Model (視覚化)
- c16: Observational Phase Transition (相転移)
- c17: Silence Friction Simulator (シミュレーション)
