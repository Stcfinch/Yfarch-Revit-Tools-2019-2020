# 永豐工坊｜Revit 2019／2020 工具集

永豐工坊是一套支援 Autodesk Revit 2019 與 2020 的外掛工具集，協助處理建模、接合、尺寸標註、視圖整理、圖紙編排與匯出等工作。

Yfarch Revit Tools supports Autodesk Revit 2019 and 2020 with modeling, joining, dimensioning, view preparation, sheet placement, and export tools.

## 下載 Download

最新版本：[`v2026.11.04`](updates/2026-11-04.md)。

請到 GitHub Releases 頁面下載最新版安裝檔：

Download the latest installer from the GitHub Releases page:

https://github.com/Stcfinch/Yfarch-Revit-Tools-2019-2020/releases

目前建議下載檔案：

Recommended release package:

```text
Yfarch-Revit-Tools-2019-2020.zip
```

## 支援環境 Supported Environment

- Autodesk Revit 2019 或 2020
- Windows
- .NET Framework 4.7.2 或相容環境

## 語言支援 Language Support

安裝程式可選繁體中文或英文。Revit 頁籤「永豐工坊」與功能分組固定為繁體中文；英文設定可顯示英文按鈕及部分提示。視圖裁切、視圖命名等操作視窗仍以繁體中文為主。

The installer supports Traditional Chinese and English. The Revit ribbon tab and panel names stay in Traditional Chinese; English settings translate buttons and some prompts. Some feature dialogs are primarily Traditional Chinese.


## 安裝方式 Installation

中文：

1. 關閉要安裝的 Autodesk Revit 2019 或 2020。
2. 到 Releases 頁面下載最新版安裝包。
3. 如下載的是 `.zip` 檔，請先解壓縮。
4. 執行安裝程式，選擇 Revit 2019 或 2020。
5. 若兩版都要使用，完成第一版安裝後再執行一次安裝程式，選擇另一版。
6. 重新開啟 Revit，在「永豐工坊」頁籤使用功能。

English:

1. Close Autodesk Revit 2019 or 2020 before installing.
2. Download the latest release package from the Releases page.
3. Extract the `.zip` file if needed.
4. Run setup and choose Revit 2019 or 2020.
5. To use both versions, run setup again and choose the other version.
6. Restart Revit and open the 「永豐工坊」 ribbon tab.

## 功能介紹 Features

### 1. 樓層 Auto Levels

以表格方式建立與管理 Revit 樓層，可讀取既有 Level，調整樓層名稱、樓高與標高，並支援新增地上層、地下層與刪除樓層。套用後會一次寫回 Revit，並同步調整 Grid 的垂直 3D 範圍。

Provides a table-based Revit Level editor for managing level names, floor heights, elevations, above-ground floors, basement floors, deleted levels, and related Grid 3D extents.

### 2. 網格 Auto Grids

由 CAD 軸線圖層產生 Revit Grid，協助快速建立模型基準，減少手動建立軸線、檢查軸號與調整定位基準的時間。

Creates Revit grids from CAD grid layers to speed up early model setup and reduce repetitive grid creation and checking work.

### 3. 結構柱 Auto Structural Columns

由 CAD 柱位圖層產生 Revit 結構柱，支援混凝土柱與 RHS 鋼構柱建模，可讀取 DWG 圖塊屬性與柱號，並輔助柱型比對、Grid 距離校正、修正報告與修訂雲形線標示，適合將平面圖柱位快速轉換為可檢查的結構模型。

Generates Revit structural columns from CAD column layers, supporting both concrete columns and RHS steel columns. It can read DWG block attributes and column marks, assist with type matching, grid-distance correction, correction reports, and revision cloud marking for more checkable structural modeling workflows.

### 4. 結構樑 Auto Structural Beams

選取已連結 CAD 的樑雙線與標號圖層，產生 Revit 結構樑。樑寬取自雙線；樑深優先讀取標號旁的尺寸，否則依標號查同一份 CAD 中可辨識的表格。可讀取圖塊屬性中的編號與尺寸，並輸出未配對或尺寸不符的檢查結果。

Generates Revit structural beams from selected layers in a linked CAD file. Width comes from the beam lines; depth comes from a nearby annotation or, when available, a matching table in the same CAD file. Block attributes can supply marks and sizes, and the tool reports unmatched marks and size discrepancies.

此版本另加入鋼構樑生成、細部尺寸表匯入與匹配、支承端點調整，以及圈出未生成樑編號。補尺寸紀錄依目前樓層篩選，避免混入其他樓層。

This version also adds steel-beam generation, detail-table import and matching, support-end adjustment, and marking of uncreated beam numbers. Missing-size supplementation filters records by the active level.

### 5. 建築牆 Auto Architecture Walls

依牆壁類型讀取 CAD 圖層，自動建立 Revit 建築牆，並支援完成面、牆型與開口相關圖層判讀，適合將建築平面 CAD 牆線轉換為 Revit 牆模型。

Generates Revit architecture walls from CAD wall layers, including wall type, finish wall, and opening-related interpretation workflows.

### 6. 結構樓板 Auto Structural Slabs

由 CAD 或模型邊界產生 Revit 結構樓板，減少手動描繪樓板邊界與重複設定構件的時間，適合樓層平面建模與結構板配置作業。

Creates Revit structural slabs from CAD or model boundaries to reduce repetitive slab boundary drafting and setup work.

### 7. 接合面修正 Auto Join Face Align

以結構柱邊界面為基準，修正牆端接柱位置的極小面偏差，減少牆柱接合後產生的雜線或細縫。

Aligns tiny wall-to-column face offsets against structural column faces to reduce join display artifacts caused by very small positioning drift.

### 8. 接合牆體 Auto Wall Join

依照指定樓層範圍，自動處理牆體與相關構件的 Join Geometry，減少牆交接位置的手動整理時間。

Automatically processes Join Geometry for walls and related elements within selected levels, reducing manual wall cleanup work.

### 9. 接合樓層交界 Auto Floor Boundary Join

依照指定樓層範圍，自動處理樓層交界附近的 Join Geometry，改善樓板、牆體或上下樓層邊界附近的幾何整理效率。

Processes Join Geometry around floor or level boundaries to improve model cleanup near slab, wall, and level transition conditions.

### 10. 切換柱樑接合 Column And Beam Join Switch

依照指定樓層範圍，批次切換柱樑之間的接合順序，協助整理柱、樑交接時的顯示與幾何關係。

Batch switches column-beam join order within selected levels to help control visibility and geometry behavior at intersections.

### 11. 切割樑牆 Auto Cut Beam-Wall

在平面圖中依使用者選取的切割線處理結構樑與牆體，可批次切割樑牆交會位置，並搭配 Join Geometry 讓平面表現維持乾淨。

Cuts beam-wall intersections based on selected plan-view cut lines and supports cleanup with Join Geometry for clearer plan representation.

### 12. 車位編號 Parking Space Numbering

依照選取路徑與設定規則，批次建立或更新停車位編號，降低地下室、停車場與大量車位平面逐一輸入編號的時間與錯誤。

Creates or updates parking space numbers in batches based on selected paths and numbering rules.

### 13. 軸線尺寸 Grid Dimension

在平面圖中選取同方向平行 Grid，自動產生連續軸線尺寸與總長尺寸，適合快速完成軸線到軸線的外層尺寸標註。

Creates continuous grid dimensions and overall dimensions from selected parallel grids in plan views.

### 14. 樓層尺寸 Level Dimension

在立面圖或剖面圖中依 Level 建立逐層高度與分段總高度尺寸，可依 GL、R1FL 與屋突段落整理樓層高度標註。

Creates level height dimensions in elevation or section views, including floor-by-floor dimensions and grouped overall height dimensions.

### 15. 柱位尺寸 Column Layout Dimension

針對柱位放樣圖產生柱位定位尺寸，可依選取柱與軸線建立柱中心、柱邊或軸線定位尺寸，並支援混凝土包覆 RHS 鋼柱的分層標註邏輯。完成後會輸出診斷資訊，協助檢查未成功標註或特殊配對的位置。

Creates column layout dimensions from selected columns and grids, supporting column center, column edge, and grid-based positioning dimensions, including layered dimensioning for concrete-encased RHS steel columns. Diagnostic output helps review skipped, failed, or special pairing conditions.

### 16. 外牆大尺寸 Facade Major Dimension

依結構柱與建築牆標註外牆主要進退面尺寸。使用者選取同一面向的柱牆並點選尺寸線側，工具會建立主要段落尺寸與總尺寸。

Creates major facade dimensions from selected structural columns and architecture walls, including primary facade steps and overall dimensions.

### 17. 外牆小尺寸 Facade Detail Dimension

標註外牆面內的門窗、開口、Grid 與柱牆細部尺寸，適合整理外牆面段落內的局部小尺寸與開口關係。

Creates detailed facade dimensions for openings, grids, columns, walls, and local facade segments.

### 18. 外牆大小尺寸 Facade Auto Dimension

依選取的外牆相關物件自動判斷面向，並整合產生外牆大尺寸與外牆小尺寸，減少分開操作的時間。

Automatically determines the facade direction from selected elements and creates both major and detail facade dimensions.

### 19. 內牆尺寸 Interior Wall Dimension

選取內牆與使用者事先繪製的尺寸輔助線，沿輔助線自動標註牆面間距、牆厚與房間尺寸，適合室內隔間尺寸整理。

Creates interior wall dimensions along user-drawn guide lines, including wall spacing, wall thickness, and room-related distances.

### 20. 樑位尺寸 Structural Beam Dimension

用於筏基層平面，依使用者繪製的 Detail Line 輔助線，自動標註結構樑邊界與樑距，協助整理筏基層樑位尺寸。

Creates structural beam dimensions in raft foundation plans using user-drawn Detail Line guides, helping annotate beam boundaries and spacing more efficiently.

### 21. 地下外牆尺寸 Basement Exterior Wall Dimension

針對地下層外牆平面，選取同一面向的結構柱與 Grid，自動建立柱寬、柱距，以及柱邊與 Grid 關係尺寸，協助整理地下外牆定位標註。

Creates basement exterior wall dimensions from selected structural columns and grids on the same side, including column widths, column spacing, and column-edge-to-grid relationships.

### 22. 視圖裁切 View Crop

先以四個參考平面建立全區及分區範圍，再依實際視圖類型選擇樓層視圖。每張視圖可分別採用只裁全區或全區加分區，並自動開啟裁剪與範圍可見。可建立或更新分區從屬視圖，設定保存在 RVT，重跑時依最新參考平面位置更新。

Define overall and zone boundaries with reference planes, then select plan views by their actual view type. Each view can use overall-only or overall-plus-zone processing, with crop visibility enabled and dependent views created or updated.

### 23. 視圖命名 View Naming

同一按鈕提供中文命名與編號／重排兩個功能。中文命名依樓層及用途產生圖名，保留樑位高程等特殊用途，並以保留的視圖推算共用樓層範圍。分區從屬視圖附加區名。圖號依樓層由低到高，同層以比例數字 150、100、50 排序；主視圖顯示所含圖號範圍與實際比例，從屬視圖各占一號。新增視圖後可重排使後方順延，並提供預覽及重名檢查。

Provides separate Chinese-title and drawing-number workflows. Preserve drawing purposes and zones, infer shared-floor titles from retained views, and reorder by level then descending scale denominator. New views can be inserted by rerunning numbering; previews and duplicate-name checks are included.

### 24. 自動圖紙化 Auto Sheet View Placement

同一按鈕提供「圖紙修正定位」與「自動放圖紙」。前者可勾選專案已載入的圖框族與型別，自動偵測外框及可放區，不必先建立空白圖紙；後者依圖號建立圖紙並放置視圖，使用實際 Viewport 外框左右置中，並以下方可見圖框線為基準預留約 3 cm。同一主視圖拆出的從屬視圖會使用相同圖框型別。

Detects the outer border and usable area of loaded title block families without requiring blank sheets. It then creates sheets from view numbers and places viewports using their actual bounds. Dependent views from the same primary view use the same title block type.

### 25. SketchUp Export

將目前 Revit 3D 視圖先匯出為 DWG，再啟動 SketchUp 2020 轉成可開啟的 SKP 檔，協助模型交換、簡報與後續視覺化作業。工具會以目前作用中的 3D 視圖作為輸出範圍，輸出資料夾會建立在 RVT 檔案旁的 `RevitToSketchUpExports`，若 SketchUp 未自動完成轉換，也會保留批次檔與 Ruby 腳本供使用者重新執行。

Exports the active Revit 3D view to DWG and launches SketchUp 2020 to convert it into a compatible SKP file for model exchange, presentation, and visualization workflows. The output is saved beside the RVT file in `RevitToSketchUpExports`, with batch and Ruby fallback scripts kept for rerunning the conversion if SketchUp does not finish automatically.

### 26. 連線開關 AI Collaboration

開啟或關閉 AI 本機協作連線，讓 AI 在安全的本機流程中讀取目前模型脈絡，並依明確方案協助建立可復原的 Revit 平面配置。

Turns the local AI collaboration connection on or off, allowing AI-assisted workflows to read the current model context and apply explicit, undoable Revit layout plans through a local process.

### 27. 授權資訊 License Information

提供授權狀態查看功能，可確認試用狀態、機器碼、到期日，並依畫面指示申請或更新授權。

Shows license and trial information, including machine code, expiration status, and activation or renewal guidance.

## 適用對象 Who This Is For

本工具適合：

- 使用 Autodesk Revit 2019 或 2020 的建築與結構工作流程
- 需要處理大量重複建模工作的使用者
- 需要快速整理模型接合、編號或匯出流程的 BIM 團隊
- 想降低手動操作錯誤並提高建模一致性的專案

This toolset is designed for:

- Architecture and structure workflows using Autodesk Revit 2019 or 2020
- Users who need to reduce repetitive modeling tasks
- BIM teams that need faster model cleanup, numbering, joining, and export workflows
- Projects that require better modeling consistency and fewer manual mistakes

## 授權與啟用 License And Activation

本軟體安裝後可免費試用 7 天。試用期結束後，需要完成授權啟用才可繼續使用。您可在 Revit 內開啟「授權資訊」，查看試用狀態、機器碼、到期日，並依畫面指示申請或更新授權。

After installation, this software includes a 7-day free trial. After the trial period expires, license activation is required to continue using the tools. Open "License Information" in Revit to check the trial status, machine code, expiration date, and instructions for purchasing or renewing a license.

## 更新方式 Updates

新版會發布在 GitHub Releases 頁面。更新時請下載最新版安裝包，關閉 Revit 後再執行安裝。

New versions will be published on the GitHub Releases page. To update, download the latest release package, close Revit, and run the installer.

## 問題回報 Support

如果遇到問題，可以在本倉庫開 GitHub Issue，建議提供：

- Revit 版本
- Windows 版本
- 使用的工具名稱
- 操作步驟
- 錯誤訊息或截圖

If you find a problem, please open a GitHub Issue and include:

- Revit version
- Windows version
- Tool name
- Steps to reproduce
- Error message or screenshot
