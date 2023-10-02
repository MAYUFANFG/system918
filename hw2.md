# 甘特圖
``` mermaid
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    研擬計畫           :a1, 2023-10-02, 1d
    任務分配            :a2,after a1  , 4d
    取得硬體      :a3,after a1  ,17d
    程式開發      :a4,after a2  ,70d
    安裝硬體      :a5,after a3  ,10d
    程式測試      :a6,after a4  ,30d
    撰寫使用手冊      :a7,after a5  ,25d
    轉換檔案      :a8,after a5  ,20d
    系統測試      :a9,after a6  ,25d
    使用者訓練      :a10,after a7,20d
    使用者測試      :a11,after a10  ,25d

# PERT圖

# 關鍵路徑
graph LR
    subgraph A[起始事件]
        A1[活動1: 2天] --> A2[活動2: 3天]
    end
    subgraph B[關鍵事件]
        B1[活動3: 5天] --> B2[活動4: 4天]
    end
    subgraph C[結束事件]
        C1[活動5: 2天] --> C2[活動6: 3天]
    end
    A2 --> B1
    A2 --> B2
    B1 --> C2
    B2 --> C1



