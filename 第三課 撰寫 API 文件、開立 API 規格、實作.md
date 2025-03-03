# 📌 第三課: 撰寫 API 文件、開立 API 規格、實作

XUMI [api文件參考](https://sunnetcloud.sharepoint.com/:x:/s/WMPro6/EUOB6-lDDIZAuk3tjeB1nM8Byr4s2O5YffuVHqnPv95xkw?e=cJorWC&clickparams=eyJBcHBOYW1lIjoiVGVhbXMtRGVza3RvcCIsIkFwcFZlcnNpb24iOiI0OS8yNDA1MzEwMTQyMSIsIkhhc0ZlZGVyYXRlZFVzZXIiOmZhbHNlfQ%3D%3D)

檔案內紀錄所有api文件規格，以個人資訊為例:
![image](https://github.com/user-attachments/assets/baeffb3c-5cec-40fe-9891-8da713c7b2d2)
![{8E465736-A02E-44F0-8D8C-C0FDCAA184A1}](https://github.com/user-attachments/assets/39c9cf1e-9330-4a3b-aa4d-8672c0cc7036)
![{93EDA5A0-5F51-4BB7-9B2C-07DE61254BEF}](https://github.com/user-attachments/assets/4eb7b20a-7b16-4f8a-ae71-b1a7991fe877)

- 1.名稱: api用途
- 2.url: api路徑以及呼叫方式
- 3.request: 請求api參數
- 4.response: api回應參數(此結構與介面定義相同)
- 5.success sample: 成功回應結構樣式
- 6.error: 錯誤代碼
- 7.error sample: 錯誤代碼範例

>[!NOTE]
>可以參考其他檔案之規格修改成新的所需文件參數

## 📌 **api 實作**
當完成api文件開立之後，在api資料夾新增檔案，以課程api為例:
```
export class CourseService {
  constructor(
    private restfulApiService: RestfulApiService,
    private httpUtils: HttpUtilService
  ) {}

  /**
   * 取得課程章節教材
   * @param {RequestCourseNode} params
   * @return {*}  {Observable<ResponseCourseNode>}
   * @memberof CourseService
   */
  getCourseMaterial(
    params: RequestCourseNode(帶入參數，定義介面所需參數)
  ): Observable<RestfulApiSuccess<ResponseCourseNode>> {
    const { course_id } = params;
    return this.restfulApiService.request(
      this.httpUtils.getPath(ApiPathLearning.GetCourseNodes, [`${course_id}`])(放置api路徑內所需夾帶參數)
    );
  }
}
```
依照此格式撰寫呼叫api方法，後續利用服務元件將api引入使用。

---
參考文件
- 📌 teams -> 99_舊資料 -> frontend traning -> 前端假資料.mp4


