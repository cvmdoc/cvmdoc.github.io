---
sidebar_position: 1
title: HRISDB
---

#### 修改日期：2025/01/17 13:53

### CEmpFlowShare - 中國-員工簽核公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | EmpID | 員工編號 | char | 6 | V |  |  |
| 3 | DeptID | 部門代碼 | varchar | 12 |  |  |  |
| 4 | DeptName | 部門名稱 | nvarchar | 60 |  |  |  |
| 5 | OrganID | 最小簽核單位 | varchar | 12 |  |  |  |
| 6 | OrganName | 最小簽核單位名稱 | nvarchar | 60 |  |  |  |
| 7 | GroupType | 事業群類別 | char | 3 |  |  |  |
| 8 | GroupID | 事業群代碼 | varchar | 12 |  |  |  |
| 9 | GroupName | 事業群名稱 | nvarchar | 60 |  |  |  |
| 10 | LastChgComp | 最後異動公司 | varchar | 6 |  |  |  |
| 11 | LastChgID | 最後異動者 | varchar | 6 |  |  |  |
| 12 | LastChgDate | 最後異動日期 | datetime | 8 |  |  |  |

### CEmpShare - 中國-員工公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | EmpID | 員工編號 | char | 6 | V |  |  |
| 3 | NameN | 中文姓名 | nvarchar | 42 |  |  |  |
| 4 | EngName | 英文姓名 | nvarchar | 42 |  |  |  |
| 5 | Sex | 性別 | char | 1 |  |  | 1 : 男 <br/>2 : 女 |
| 6 | WorkStatus | 任職狀況 | char | 1 |  |  | 1 ─ 在職<br/>2 ─ 留停<br/>3 ─ 離職<br/>4 ─ 外派<br/>5 ─ 外調<br/>6 ─ 退休<br/>7 ─ 跨公司調動 |
| 7 | WorkTypeID | 工作性質代碼 | varchar | 50 |  |  |  |
| 8 | WorkType | 工作性質 | nvarchar | 200 |  |  |  |
| 9 | CompName | 公司名稱 | nvarchar | 20 |  |  |  |
| 10 | GroupID | 事業單位代碼 | varchar | 12 |  |  |  |
| 11 | GroupName | 事業單位名稱 | nvarchar | 30 |  |  |  |
| 12 | OrganID | 單位代碼 | varchar | 12 |  |  |  |
| 13 | OrganName | 單位名稱 | nvarchar | 30 |  |  |  |
| 14 | DeptID | 部門代碼 | varchar | 12 |  |  |  |
| 15 | DeptName | 部門名稱 | nvarchar | 30 |  |  |  |
| 16 | WorkSite | 工作地點 | nvarchar | 20 |  |  |  |
| 17 | RankID | 職等代碼 | char | 2 |  |  |  |
| 18 | TitleName | 職稱 | nvarchar | 20 |  |  |  |
| 19 | HoldingRankID | 金控職等 | varchar | 2 |  |  | 保留欄位，DB無資料 |
| 20 | HoldingTitleName | 金控職稱 | nvarchar | 50 |  |  | 保留欄位，DB無資料 |
| 21 | EmpDate | 到職日期 | datetime | 8 |  |  |  |
| 22 | SinopacEmpDate | 企業團到職日 | datetime | 8 |  |  |  |
| 23 | QuitDate | 離職/留停/外派日期 | datetime | 8 |  |  |  |
| 24 | NotEmpDay | 不計算年資天數 | int | 4 |  |  | 保留欄位，DB無資料 |
| 25 | EMail | 電子郵件地址 | varchar | 60 |  |  |  |
| 26 | CompTel | 公司電話 | varchar | 22 |  |  |  |
| 27 | LastChgComp | 最後異動公司 | varchar | 6 |  |  |  |
| 28 | LastChgID | 最後異動者 | varchar | 6 |  |  |  |
| 29 | LastChgDate | 最後異動日期 | datetime | 8 |  |  |  |

### Company - 公司基本資料檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | CompName | 公司名稱 | nvarchar | 40 |  |  |  |
| 3 | CompEngName | 公司英文名稱 | varchar | 50 |  |  |  |
| 4 | CompChnName | 公司中文名稱 | varchar | 50 |  |  |  |
| 5 | FeeShareFlag | 費用分攤註記 | char | 1 |  |  |  |
| 6 | NotesCompName | NotesID之公司名稱 | varchar | 50 |  |  |  |
| 7 | InValidFlag | 無效註記 | char | 1 |  |  | 0-有效<br/>1-無效 |
| 8 | NotShowFlag | 不顯示註記 | char | 1 |  |  | 0-顯示<br/>1-不顯示 |
| 9 | ReturnDB | 程式用參數 | varchar | 20 |  |  | 程式用參數 |
| 10 | StopFromAS400 | 程式用參數 | char | 1 |  |  | 程式用參數 |

### COrgFlowShare - 中國-簽核流程組織公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | varchar | 6 |  |  |  |
| 2 | OrganID | 單位代碼 | varchar | 12 | V |  |  |
| 3 | OrganName | 單位名稱 | nvarchar | 60 |  |  |  |
| 4 | UpOrganID | 上階部門代號 | varchar | 12 |  |  |  |
| 5 | DeptID | 所屬一級部門代號 | varchar | 12 |  |  |  |
| 6 | GroupType | 事業單位類別 | varchar | 3 |  |  |  |
| 7 | GroupID | 事業單位代碼 | varchar | 12 |  |  |  |
| 8 | GroupName | 事業單位名稱 | nvarchar | 30 |  |  |  |
| 9 | Boss | 部門主管 | varchar | 6 |  |  |  |
| 10 | BossCompID | 部門主管公司代碼 | varchar | 6 |  |  |  |
| 11 | BossType | 主管任用方式 | char | 1 |  |  | 1 – 主要<br/>2 – 兼任 |
| 12 | SecBoss | 部門副主管 | varchar | 6 |  |  |  |
| 13 | SecBossCompID | 部門副主管公司代碼 | varchar | 6 |  |  |  |
| 14 | VirtualFlag | 虛擬部門註記 | char | 1 |  |  | 0 – 非虛擬部門<br/>1 – 虛擬部門 |
| 15 | InValidFlag | 無效註記 | char | 1 |  |  | 0 – 有效<br/>1 – 無效 |
| 16 | Depth | 單位層級 | varchar | 2 |  |  |  |
| 17 | BranchFlag | 分行註記 | varchar | 1 |  |  |  |
| 18 | DelegateFlag | 授權註記 | char | 1 |  |  | 1.是 0.否<br/>請假系統使用 |
| 19 | RoleCode | 單位角色 | varchar | 2 |  |  | 保留欄位，DB無資料<br/>10-子公司科級主管<br/>20-子公司部級主管<br/>30-子公司處級主管<br/>40-子公司事業群總經理<br/>50-子公司總經理<br/>60-子公司董事長<br/>70-金控組長<br/>80-金控處長/主任<br/>98-金控副執行長<br/>99-金控執行長<br/>AA-金控董事長 |
| 20 | LastChgComp | 組織架構檔最後異動公司 | varchar | 6 |  |  |  |
| 21 | LastChgID | 組織架構檔最後異動者 | varchar | 6 |  |  |  |
| 22 | LastChgDate | 組織架構檔最後異動日期 | datetime | 8 |  |  |  |

### COrgShare - 中國-組織公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | varchar | 6 | V |  |  |
| 2 | OrganID | 單位代碼 | varchar | 12 | V |  |  |
| 3 | OrganName | 單位名稱 | nvarchar | 30 |  |  |  |
| 4 | OrganEngName | 單位英文名稱 | nvarchar | 60 |  |  |  |
| 5 | UpOrganID | 上階部門代號 | varchar | 12 |  |  |  |
| 6 | DeptID | 所屬一級部門代號 | varchar | 12 |  |  |  |
| 7 | GroupType | 事業單位類別 | varchar | 3 |  |  |  |
| 8 | GroupID | 事業單位代碼 | varchar | 12 |  |  |  |
| 9 | GroupName | 事業單位名稱 | nvarchar | 30 |  |  |  |
| 10 | Boss | 部門主管 | varchar | 6 |  |  |  |
| 11 | BossCompID | 部門主管公司代碼 | varchar | 6 |  |  |  |
| 12 | BossType | 主管任用方式 | char | 1 |  |  | 1 – 主要<br/>2 – 兼任 |
| 13 | SecBoss | 部門副主管 | varchar | 6 |  |  |  |
| 14 | SecBossCompID | 部門副主管公司代碼 | varchar | 6 |  |  |  |
| 15 | PersonPart | 部門角色─人事管理員 | varchar | 6 |  |  | 保留欄位，DB無資料 |
| 16 | WorkSite | 工作地點 | nvarchar | 20 |  |  | 保留欄位，DB無資料 |
| 17 | WorkType | 工作性質 | nvarchar | 200 |  |  | 保留欄位，DB無資料 |
| 18 | VirtualFlag | 虛擬部門註記 | char | 1 |  |  | 0 – 非虛擬部門<br/>1 – 虛擬部門 |
| 19 | InValidFlag | 無效註記 | char | 1 |  |  | 0 – 有效<br/>1 – 無效 |
| 20 | Depth | 單位層級 | varchar | 2 |  |  |  |
| 21 | BranchFlag | 分行註記 | varchar | 1 |  |  |  |
| 22 | RoleCode | 單位角色 | varchar | 2 |  |  | 保留欄位，DB無資料<br/>10科級單位<br/>20部/中心級主管<br/>30處級主管<br/>40事業群總經理<br/>50總經理<br/>60董事長<br/>70金控組長 |
| 23 | SortOrder | 單位排序 | varchar | 1 |  |  | 保留欄位，DB無資料 |
| 24 | LastChgComp | 組織架構檔最後異動公司 | varchar | 6 |  |  |  |
| 25 | LastChgID | 組織架構檔最後異動者 | varchar | 6 |  |  |  |
| 26 | LastChgDate | 組織架構檔最後異動日期 | datetime | 8 |  |  |  |

### Daily_EmpShareLog - 每日員工比對異動記錄檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | LogDate | 記錄日期 | char | 10 | V |  | 格式yyyy/MM/dd<br/>系統比對產生資料的系統日<br/>2014/02/17上午取得人員異動檔資料的 LogDate 為 ‘2014/02/17’ |
| 2 | LogSeq | 記錄序號 | smallint | 2 | V |  | 從1開始，每天原則上只做一次比對。 |
| 3 | CompID | 公司代碼 | char | 6 | V |  |  |
| 4 | EmpID | 員工編號 | char | 6 | V |  |  |
| 5 | ChgID | 異動代碼 | char | 2 | V |  | 01-任職狀態異動<br/>02-工作性質(主兼)異動<br/>03-職位異動<br/>11-公司異動=>這邊是針對”任職狀態”異動為”7-跨公司調動”，提供異動前後的公司代碼及名稱，EX:銀行轉調證券<br/>12-部門異動<br/>13-科組課異動<br/>21-新增資料<br/>=>前一天EmpShare無資料，當天有資料者(如新進員工)，”異動前後的欄位值”固定都是空白<br/>91-當天無資料(異常) =>異常資料，前一天EmpShare有資料，當天無資料者，屬HR要處理的異常問題資料，其他系統請忽略<br/>92-多公司在職(異常) =>異常資料，同樣員工編號在多個公司皆在職者，屬HR要處理的異常問題資料，其他系統請忽略 |
| 6 | ChgRemark | 異動說明 | varchar | 100 |  |  |  |
| 7 | NameN | 中文姓名 | nvarchar | 12 |  |  |  |
| 8 | BeforeID | 異動前代碼 | varchar | 200 |  |  | 異動代碼21，91，92不寫入 |
| 9 | BeforeRemark | 異動前名稱 | varchar | 500 |  |  | 異動代碼21，91，92不寫入 |
| 10 | AfterID | 異動後代碼 | varchar | 200 |  |  | 異動代碼21，91，92不寫入 |
| 11 | AfterRemark | 異動後名稱 | varchar | 500 |  |  | 異動代碼21，91，92不寫入 |
| 12 | CreateDate | 建檔日期時間 | datetime | 8 |  |  |  |

### EmpAddition - 員工調兼現況檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | ValidDate | 生效日 | datetime | 8 | V |  |  |
| 2 | CompID | 公司代碼 | char | 6 | V |  |  |
| 3 | EmpID | 員工代碼 | char | 6 | V |  |  |
| 4 | AddCompID | 調兼公司代碼 | char | 6 | V |  |   |
| 5 | AddDeptID | 調兼部門代碼 | varchar | 12 | V |  | 實體組織OrgShare |
| 6 | AddOrganID | 調兼科組課代碼 | varchar | 12 | V |  | 實體組織OrgShare |
| 7 | Reason | 狀態 | char | 1 |  | V | 1-調兼 |
| 8 | FileNo | 人令 | varchar | 50 |  | V |  |
| 9 | Remark | 備註 | varchar | 500 |  | V |  |
| 10 | CreateDate | 建檔日 | datetime | 8 |  | V |  |
| 11 | CreateComp | 建檔人員公司 | char | 6 |  | V |  |
| 12 | CreateID | 建檔人員 | char | 6 |  | V |  |
| 13 | LastChgDate | 修改日 | datetime | 8 |  | V |  |
| 14 | LastChgComp | 修改人員公司 | char | 6 |  | V |  |
| 15 | LastChgID | 修改人員 | char | 6 |  | V |  |
| 16 | AdditionFlag | 調兼註記 | char | 2 |  |  | A專任<br/>B專職兼任<br/>C調兼專任<br/>D1調兼兼任-數據資料<br/>D2調兼兼任-作業處理<br/>Z其他 |
| 17 | AdditionFlagName | 調兼註記名稱 | nvarchar | 20 |  |  |  |

### EmpFlowShare - 員工簽核公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | EmpID | 員工編號 | char | 6 | V |  |  |
| 2 | CompID | 公司代碼 | char | 6 | V |  |  |
| 3 | ActionID | 簽核類別 | char | 2 | V |  | 01:請假作業<br/>02:升等作業<br/>03:考核作業 |
| 4 | OrganID | 最小簽核單位 | varchar | 12 |  |  |  |
| 5 | OrganName | 最小簽核單位名稱 | varchar | 60 |  |  |  |
| 6 | GroupType | 事業群類別 | char | 3 |  |  |  |
| 7 | GroupID | 事業群代碼 | varchar | 12 |  |  |  |
| 8 | GroupName | 事業群名稱 | varchar | 30 |  |  |  |
| 9 | LastChgID | 最後異動人員 | char | 6 |  |  |  |
| 10 | LastChgDate | 最後異動日期 | datetime | 8 |  |  |  |
| 11 | BusinessType | 業務類別 | char | 2 |  | V |  |
| 12 | BusinessTypeName | 業務類別名稱 | nvarchar | 100 |  | V |  |
| 13 | EmpFlowRemarkID | 功能備註 | varchar | 2 |  | V |  |
| 14 | EmpFlowRemarkName | 功能備註名稱 | nvarchar | 100 |  | V |  |

### EmpPosition - 員工職位檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | EmpID | 員工編號 | char | 6 | V |  |  |
| 3 | PositionID | 職位代碼 | char | 6 | V |  |  |
| 4 | PrincipalFlag | 主要工作性質註記 | char | 1 |  |  | 0– 兼任<br/>1– 主要 |
| 5 | LastChgComp | 最後異動公司 | char | 6 |  |  |  |
| 6 | LastChgID | 最後異動者 | char | 6 |  |  |  |
| 7 | LastChgDate | 最後異動日期 | datetime | 8 |  |  |  |

### EmpShare - 員工公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | EmpID | 員工編號 | char | 6 | V |  |  |
| 3 | Name | 中文姓名 | varchar | 12 |  |  | 顯示為 柯”田井”宇 |
| 4 | EngName | 英文姓名 | varchar | 20 |  |  |  |
| 5 | Sex | 性別 | char | 1 |  |  |  1 : 男 <br/>2 : 女 |
| 6 | WorkStatus | 任職狀況 | char | 1 |  |  | 1 ─ 在職<br/>2 ─ 留停<br/>3 ─ 離退<br/>7 ─ 跨公司任職 |
| 7 | WorkTypeID | 工作性質代碼 | varchar | 50 |  |  | BOC003|BOC004|BOC007|BOC009 |
| 8 | WorkType | 工作性質 | varchar | 200 |  |  | 分行服務台經辦|分行企放作業|分行企放窗口|分行個放作業 |
| 9 | CompName | 公司名稱 | varchar | 20 |  |  |  |
| 10 | GroupID | 事業單位代碼 | varchar | 8 |  |  |  |
| 11 | GroupName | 事業單位名稱 | varchar | 30 |  |  |  |
| 12 | OrganID | 單位代碼 | varchar | 8 |  |  |  |
| 13 | OrganName | 單位名稱 | varchar | 30 |  |  |  |
| 14 | DeptID | 部門代碼 | varchar | 8 |  |  |  |
| 15 | DeptName | 部門名稱 | varchar | 30 |  |  |  |
| 16 | WorkSite | 工作地點 | varchar | 20 |  |  |  |
| 17 | RankID | 職等代碼 | char | 2 |  |  | 職等不外顯，僅提供系統邏輯使用 |
| 18 | TitleName | 職稱 | varchar | 20 |  |  |  |
| 19 | HoldingRankID | 金控職等 | char | 2 |  |  | 已無使用，值都放ZZ |
| 20 | HoldingTitleName | 金控職稱 | varchar | 50 |  |  | 已無使用，值都放ZZ |
| 21 | EmpDate | 到職日期 | datetime | 8 |  |  |  |
| 22 | SinopacEmpDate | 企業團到職日 | datetime | 8 |  |  |  |
| 23 | QuitDate | 離職/留停/外派日期 | datetime | 8 |  |  |  |
| 24 | NotEmpDay | 不計算年資天數 | int | 4 |  |  |  |
| 25 | AdjustHour | 調休時數(Only 證券Data) | decimal | 5 |  |  |  |
| 26 | LastChgDate | 員工主檔最近異動日期 | datetime | 8 |  |  |  |
| 27 | EMail | 電子郵件地址 | varchar | 60 |  |  |  |
| 28 | CompTel | 公司電話 | varchar | 22 |  |  |  |
| 29 | WTID | 班別代碼 | char | 2 |  |  |  |
| 30 | LicenseData | 證照資料(Only 證券Data) | varchar | 500 |  |  |  |
| 31 | ProbFlag | 試用考核註記(Only 證券Data) | char | 1 |  |  |  |
| 32 | RegStatus | SSO註冊狀態 | char | 1 |  |  |  |
| 33 | RegIP | SSO註冊 Client IP | varchar | 50 |  |  |  |
| 34 | LoginTime | 登入時間 | datetime | 8 |  |  |  |
| 35 | AOCode | AOCode | varchar | 6 |  |  |  |
| 36 | WorkSiteCode | 工作地點郵遞區號 | varchar | 5 |  |  |  |
| 37 | NameN | 中文姓名(Unicode,難字) | nvarchar | 12 |  |  | 顯示為  柯”畊”宇<br/>依統一各系統行員姓名顯示規則，建議使用此欄 |
| 38 | EmpIDOld | 員工編號Old | varchar | 6 |  |  |  |
| 39 | PositionID | 職位代碼 | varchar | 50 |  |  | 030003|030004 |
| 40 | Position | 職位 | nvarchar | 200 |  |  | 系統設計人員|程式設計人員 |

### EmpWorkType - 員工工作性質檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | EmpID | 員工編號 | char | 6 | V |  |  |
| 3 | WorkTypeID | 工作性質編號 | char | 6 | V |  | 參照Table “WorkType” |
| 4 | PrincipalFlag | 主要工作性質註記 | char | 1 |  |  | 0 – 兼任工作性質<br/>1 – 主要工作性質 |
| 5 | LastChgComp | 最後異動公司 | varchar | 6 |  |  |  |
| 6 | LastChgID | 最後異動者 | varchar | 6 |  |  |  |
| 7 | LastChgDate | 最後異動日期 | datetime | 8 |  |  |  |

### OrgFlowShare - 簽核流程組織公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 |  |  |  |
| 2 | OrganID | 單位代碼 | varchar | 12 | V |  |  |
| 3 | OrganName | 單位名稱 | varchar | 60 |  |  |  |
| 4 | GroupType | 事業單位類別 | char | 3 |  |  |  |
| 5 | GroupID | 事業單位代碼 | varchar | 12 |  |  |  |
| 6 | GroupName | 事業單位名稱 | varchar | 30 |  |  |  |
| 7 | UpOrganID | 上階部門代號 | varchar | 12 |  |  |  |
| 8 | DeptID | 所屬一級部門代號 | varchar | 12 |  |  |  |
| 9 | Boss | 部門主管 | char | 6 |  |  |  |
| 10 | BossCompID | 部門主管公司代碼 | char | 6 |  |  |  |
| 11 | BossType | 主管任用方式 | char | 1 |  |  | 1 – 主要<br/>2 – 兼任 |
| 12 | SecBoss | 部門副主管 | char | 6 |  |  |  |
| 13 | SecBossCompID | 部門副主管公司代碼 | char | 6 |  |  |  |
| 14 | VirtualFlag | 虛擬部門註記 | char | 1 |  |  | 0 – 非虛擬部門<br/>1 – 虛擬部門 |
| 15 | InValidFlag | 無效註記 | char | 1 |  |  | 0 – 有效<br/>1 – 無效 |
| 16 | LastChgDate | 組織架構檔最近異動日期 | datetime | 8 |  |  |  |
| 17 | Depth | 單位層級 | varchar | 2 |  |  |  |
| 18 | BranchFlag | 分行註記 | char | 1 |  |  |  |
| 19 | DelegateFlag | 授權註記 | char | 1 |  |  | 1.是 0.否<br/>請假系統使用 |
| 20 | RoleCode | 單位角色 | varchar | 2 |  |  | 10子公司科級主管<br/>20子公司部級主管<br/>30子公司處級主管<br/>40子公司事業群總經理<br/>50子公司總經理<br/>60子公司董事長<br/>70金控組長<br/>80金控處長/主任<br/>98金控副執行長<br/>99金控執行長<br/>AA金控董事長 |
| 21 | BusinessType | 業務類別 | char | 2 |  |  | 01法金<br/>02零售<br/>03作業<br/>99其他 |

### OrgShare - 組織公用檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | OrganID | 單位代碼 | varchar | 8 | V |  |  |
| 3 | GroupType | 事業單位類別 | char | 3 |  |  |  |
| 4 | GroupID | 事業單位代碼 | varchar | 8 |  |  |  |
| 5 | GroupName | 事業單位名稱 | varchar | 30 |  |  |  |
| 6 | OrganName | 單位名稱 | varchar | 30 |  |  |  |
| 7 | OrganEngName | 單位英文名稱 | varchar | 60 |  |  |  |
| 8 | UpOrganID | 上階部門代號 | varchar | 8 |  |  |  |
| 9 | DeptID | 所屬一級部門代號 | varchar | 8 |  |  |  |
| 10 | Boss | 部門主管 | char | 6 |  |  |  |
| 11 | BossCompID | 部門主管公司代碼 | char | 6 |  |  |  |
| 12 | BossType | 主管任用方式 | char | 1 |  |  | 1 – 主要<br/>2 – 兼任 |
| 13 | SecBoss | 部門副主管 | char | 6 |  |  |  |
| 14 | SecBossCompID | 部門副主管公司代碼 | char | 6 |  |  |  |
| 15 | WorkSite | 工作地點 | varchar | 20 |  |  |  |
| 16 | Position | 職位 | nvarchar | 200 |  | V |  |
| 17 | WorkType | 工作性質 | varchar | 200 |  |  |  |
| 18 | VirtualFlag | 虛擬部門註記 | char | 1 |  |  | 0 – 非虛擬部門<br/>1 – 虛擬部門 |
| 19 | InValidFlag | 無效註記 | char | 1 |  |  | 0 – 有效<br/>1 – 無效 |
| 20 | LastChgDate | 組織架構檔最近異動日期 | datetime | 8 |  |  |  |
| 21 | Depth | 單位層級 | varchar | 2 |  |  |  |
| 22 | BranchFlag | 分行註記 | char | 1 |  |  |  |
| 23 | RoleCode | 單位角色 | varchar | 2 |  |  | 10科級單位<br/>20部/中心級主管<br/>30處級主管<br/>40事業群總經理<br/>50總經理<br/>60董事長<br/>70金控組長<br/> |
| 24 | SortOrder | 單位排序 | varchar | 6 |  |  |  |
| 25 | PersonPart | 部門角色─人事管理員 | char | 6 |  |  |  |

### Position - 職位代碼檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | PositionID | 職位代碼 | char | 6 | V |  |  |
| 3 | Remark | 說明 | nvarchar | 40 |  | V |  |
| 4 | InValidFlag | 無效註記 | char | 1 |  | V |  0有效<br/>1無效 |
| 5 | SortOrder | 排序 | varchar | 1 |  | V |  |
| 6 | LastChgComp | 最後異動公司 | char | 6 |  | V |  |
| 7 | LastChgID | 最後異動人員 | char | 6 |  | V |  |
| 8 | LastChgDate | 最後異動時間 | datetime | 8 |  | V |  |

### vw_EmpShare - 員工公用VIEW檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 |  |  |  |
| 2 | EmpID | 員工編號 | char | 6 |  |  |  |
| 3 | NameN | 中文姓名(Unicode,難字) | nvarchar | 12 |  |  | 顯示為  柯”畊”宇<br/>依統一各系統行員姓名顯示規則，建議使用此欄 |
| 4 | EngName | 英文姓名 | varchar | 20 |  |  |  |
| 5 | Sex | 性別 | char | 1 |  |  |  1 : 男 <br/>2 : 女 |
| 6 | WorkStatus | 任職狀況 | char | 1 |  |  | 1 ─ 在職<br/>2 ─ 留停<br/>3 ─ 離退<br/>7 ─ 跨公司任職 |
| 7 | WorkTypeID | 工作性質代碼 | varchar | 50 |  |  | BOC003|BOC004|BOC007|BOC009 |
| 8 | WorkType | 工作性質 | varchar | 200 |  |  | 分行服務台經辦|分行企放作業|分行企放窗口|分行個放作業 |
| 9 | CompName | 公司名稱 | varchar | 20 |  |  |  |
| 10 | GroupID | 事業單位代碼 | varchar | 8 |  |  |  |
| 11 | GroupName | 事業單位名稱 | varchar | 30 |  |  |  |
| 12 | OrganID | 單位代碼 | varchar | 8 |  |  |  |
| 13 | OrganName | 單位名稱 | varchar | 30 |  |  |  |
| 14 | DeptID | 部門代碼 | varchar | 8 |  |  |  |
| 15 | DeptName | 部門名稱 | varchar | 30 |  |  |  |
| 16 | WorkSite | 工作地點 | varchar | 20 |  |  |  |
| 17 | TitleName | 職稱 | varchar | 20 |  |  |  |
| 18 | EmpDate | 到職日期 | datetime | 8 |  |  |  |
| 19 | SinopacEmpDate | 企業團到職日 | datetime | 8 |  |  |  |
| 20 | QuitDate | 離職/留停/外派日期 | datetime | 8 |  |  |  |
| 21 | LastChgDate | 員工主檔最近異動日期 | datetime | 8 |  |  |  |
| 22 | EMail | 電子郵件地址 | varchar | 60 |  |  |  |
| 23 | CompTel | 公司電話 | varchar | 22 |  |  |  |
| 24 | WTID | 班別(Only 證券Data) | char | 2 |  |  |  |
| 25 | LicenseData | 證照資料(Only 證券Data) | varchar | 500 |  |  |  |
| 26 | ProbFlag | 試用考核註記(Only 證券Data) | char | 1 |  |  |  |
| 27 | AOCode | AOCode | varchar | 6 |  |  |  |
| 28 | WorkSiteCode | 工作地點郵遞區號 | varchar | 5 |  |  |  |
| 29 | PositionID | 職位代碼 | varchar | 50 |  |  | 030003|030004 |
| 30 | Position | 職位 | nvarchar | 200 |  |  | 系統設計人員|程式設計人員 |

### WorkSite - 工作地點代碼檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | WorkSiteID | 工作地點代碼 | char | 3 | V |  |  |
| 3 | Remark | 工作地點說明 | nvarchar | 20 |  |  |  |
| 4 | EmpCount | 人數 | int | 4 |  |  |  |
| 5 | BranchFlag | 分行註記 | varchar | 1 |  |  |  |
| 6 | BuildingFlag | 大樓註記 | varchar | 1 |  |  |  |
| 7 | InvoiceNo | 統一編號 | varchar | 8 |  |  |  |
| 8 | WorkSiteCode | 地址郵遞區號 | varchar | 5 |  |  |  |
| 9 | CountryCode | 國碼 | varchar | 6 |  |  |  |
| 10 | AreaCode | 區碼 | varchar | 3 |  |  |  |
| 11 | Telephone | 電話 | varchar | 20 |  |  |  |
| 12 | ExtNo | 分機 | varchar | 5 |  |  |  |
| 13 | Address | 地址 | varchar | 60 |  |  |  |
| 14 | DialIn | 撥入單位類別 | varchar | 20 |  |  |  |
| 15 | DialOut | 撥出單位類別 | varchar | 20 |  |  |  |
| 16 | LastChgComp | 最後異動公司 | varchar | 6 |  |  |  |
| 17 | LastChgID | 最後異動人員 | varchar | 6 |  |  |  |
| 18 | LastChgDate | 最後異動時間 | datetime | 8 |  |  |  |
| 19 | ExtYards | 分機號碼長度 | smallint | 2 |  |  |  |
| 20 | CityCode | 縣市代碼 | varchar | 2 |  |  |  |

### WorkType - 工作性質代碼檔
序號 | 欄位名稱 | 欄位中文 | 資料型態 | 長度 | 是否為主鍵 | 是否允許null| 備註 | 
|-----------|-----------|------------|------------|------------|------------|------------|-----------|
| 1 | CompID | 公司代碼 | char | 6 | V |  |  |
| 2 | WorkTypeID | 工作性質代碼 | char | 6 | V |  |  |
| 3 | Remark | 說明 | varchar | 22 |  |  |  |
| 4 | InValidFlag | 無效註記 | char | 1 |  |  | 0有效<br/>1無效 |
| 5 | SortOrder | 排序 | varchar | 1 |  |  |  |

