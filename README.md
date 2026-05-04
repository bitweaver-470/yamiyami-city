# Yami-Yami City BepInEx Mods

Yami-Yami City 用の BepInEx 6 IL2CPP mod です。

## 必要環境

- Yami-Yami City / Unity 6000.2.6f2
- BepInEx 6 IL2CPP win-x64 `6.0.0-be.755` 以降推奨

この環境では `be.755` へ更新し、`BepInEx/config/BepInEx.cfg` の `UnityLogListening = false` で動作確認しています。

## インストール

1. BepInEx 6 IL2CPP win-x64 をゲームフォルダに導入します。
2. 一度ゲームを起動して `BepInEx/plugins` と `BepInEx/config` を生成します。
3. このフォルダの DLL を `BepInEx/plugins` にコピーします。
4. ゲームを起動します。

## DLL

- `YamiYamiNoMosaic.dll`
  - モザイク候補の Renderer / GameObject を自動で非表示にします。
- `YamiYamiUtilityMods.dll`
  - フリーカメラ、男/局部非表示、ライト切替、シーン dump を追加します。

## キー操作

| キー | 機能 |
| --- | --- |
| F8 | 男/局部非表示 ON/OFF |
| F9 | フリーカメラ ON/OFF 
| F12 | シーンライト ON/OFF |

## フリーカメラ操作

| 操作 | 機能 |
| --- | --- |
| WASD / 矢印キー | 移動 |
| Q / E | 下 / 上 |
| Ctrl | 低速移動 |
| Alt | 高速移動 |
| 左クリックまたは右クリック中にマウス移動 | 視点回転 |
| Shift 押し中 | UI モード、カーソル解放 |

## 設定ファイル

初回起動後に以下が生成されます。

- `BepInEx/config/local.yamiyami.nomosaic.cfg`
- `BepInEx/config/local.yamiyami.utilitymods.cfg`

主な設定:

```ini
[HideObjects]
ToggleKey = F8
StartActive = false
ContinuousScan = false

[FreeCamera]
ToggleKey = F9
MoveSpeed = 3
LookSensitivity = 1.2
RequireMouseButtonForLook = true

[Lights]
ToggleKey = F12
ToggleLightMeshes = true

```

`ContinuousScan = false` のため、男/局部非表示は F8 を押した瞬間だけスキャンします。
新しくロードされた対象を消したい場合は F8 を押し直してください。
