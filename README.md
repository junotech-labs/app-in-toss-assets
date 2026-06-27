# app-in-toss-assets

앱인토스(Apps-in-Toss) 미니앱들의 **공용 에셋 저장소**. 각 앱의 `granite.config.ts`가
여기의 raw URL을 **커밋 SHA로 고정**해 아이콘 등을 참조한다. (브랜치 이동/삭제와 무관하게
고정된 이미지를 받기 위함)

## 구조

앱별 폴더(`appName` 기준)로 관리한다.

```
common-sense/icon.png       # 당신의 상식은? (common-sense)
engilish-worddle/icon.png   # 잉글워뜰 (engilish-worddle)
my-values/icon.png          # 가치 월드컵 (my-values)
you-must-have/icon.png      # 가져야한다! (you-must-have) — 전용 아이콘 준비 전 임시
```

## 사용법 (granite.config.ts)

```ts
icon: 'https://raw.githubusercontent.com/junotech-labs/app-in-toss-assets/<commit-sha>/<appName>/icon.png',
```

에셋을 교체하면 새 커밋 SHA로 각 앱의 config URL을 갱신한 뒤 `ait deploy`로 반영한다.
