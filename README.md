# xeokit-bim-viewer

[![npm version](https://badge.fury.io/js/%40xeokit%2Fxeokit-bim-viewer.svg)](https://badge.fury.io/js/%40xeokit%2Fxeokit-bim-viewer)
[![](https://data.jsdelivr.com/v1/package/npm/@xeokit/xeokit-bim-viewer/badge)](https://www.jsdelivr.com/package/npm/@xeokit/xeokit-bim-viewer)
[![@xeokit/xeokit-bim-viewer](https://snyk.io/advisor/npm-package/@xeokit/xeokit-bim-viewer/badge.svg)](/advisor/npm-package/@xeokit/xeokit-bim-viewer)

[![Screenshot](https://github.com/xeokit/xeokit-bim-viewer/raw/master/images/xeokit-bim-viewer.png)](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=OTCConferenceCenter&tab=storeys)

* [Chạy demo](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=OTCConferenceCenter&tab=storeys)

---
Nếu bạn quan tâm đến **Hệ sinh thái xem BIM/3D sẵn sàng sử dụng cho Giải pháp của riêng bạn**, hãy xem thêm:
* [xeoVision - xem mô hình của bạn ngay bây giờ!](https://xeo.vision/)
* [xeoServices](https://docs.xeo.vision/)
---

**[xeokit-bim-viewer](https://github.com/xeokit/xeokit-bim-viewer)** là trình xem BIM 2D/3D mã nguồn mở chạy trên
trình duyệt và tải mô hình từ hệ thống tệp của bạn.

Trình xem được xây dựng trên **[xeokit](http://xeokit.io)**, và được đóng gói như một phần của **[xeokit SDK](http://xeokit.io)**.

Trình xem được phát triển bởi [xeolabs](http://xeolabs.com) và [OpenProject](https://www.openproject.org/), và hiện được hỗ trợ bởi [Creoox AG](https://creoox.com/).
Nó được tích hợp trong [OpenProject BIM 10.4](https://www.openproject.org/openproject-bim-10-4/) và các phiên bản mới hơn.

Trình xem có thể được sử dụng như một ứng dụng JavaScript độc lập. Kết hợp với các công cụ chuyển đổi mô hình CLI mã nguồn mở,
nó đại diện cho một cách chi phí thấp, hiệu suất cao để đưa các mô hình IFC của bạn lên Web, cho phép bạn tự do
chuyển đổi và lưu trữ mô hình trên máy chủ hoặc kho lưu trữ GitHub của riêng bạn. Để chuyển đổi IFC mạnh mẽ và hiệu quả nhất, chúng tôi khuyên bạn nên
xem [IFC -> binary glTF (GLB) cxConverter](https://github.com/Creoox/creoox-ifc2gltfcxconverter/releases).

## 📜 Giấy phép & Sử dụng Thương mại

xeokit SDK được cấp phép theo **AGPLv3**, yêu cầu mọi sửa đổi hoặc tích hợp xeokit SDK vào dự án cũng phải được mã nguồn mở theo AGPLv3.

🪧 **Cần giấy phép thương mại?** Nếu công ty của bạn yêu cầu xeokit SDK theo mô hình cấp phép khác cho các ứng dụng **độc quyền hoặc mã nguồn đóng**, chúng tôi cung cấp **các tùy chọn cấp phép thương mại linh hoạt**.

📩 **Liên hệ với chúng tôi** tại [contact@creoox.com](mailto:contact@creoox.com) hoặc truy cập [xeokit.io](https://xeokit.io/index.html#pricing) để biết thêm thông tin.
---

## Cách sử dụng

Để xem mô hình của bạn với trình xem này:

**Phương pháp 1**

1. Fork kho lưu trữ [xeokit-bim-viewer](https://github.com/xeokit/xeokit-bim-viewer) trên GitHub.
1. Chuyển đổi các tệp IFC STEP của bạn bằng [công cụ CLI mã nguồn mở](https://www.notion.so/xeokit/Viewing-an-IFC-Model-with-xeokit-c373e48bc4094ff5b6e5c5700ff580ee).
3. Thêm các mô hình đã chuyển đổi vào thư mục data của fork.
4. Phục vụ fork của bạn bằng [GitHub Pages](https://pages.github.com/).

Then users can view your models in their browsers, with URLs like this:

[````https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=OTCConferenceCenter&tab=storeys````](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=OTCConferenceCenter&tab=storeys)

Remember to add the `projectId` parameter to your URL as in the example:
`https://user.github.io/xeokit-bim-viewer/app/index.html?projectId=<your projectID here>`

**Phương pháp 2**

1. Cài đặt NodeJS từ https://nodejs.org/en
2. Clone hoặc fork kho lưu trữ này và cài đặt các phụ thuộc cần thiết

```bash
git clone https://github.com/xeokit/xeokit-bim-viewer
cd xeokit-bim-viewer
npm install
```

3. Thêm các mô hình đã chuyển đổi vào thư mục `data`.
4. Chạy trình xem trên máy cục bộ của bạn bằng:

```bash
npm run serve
```

5. Truy cập `http://localhost:8080/app/index.html?projectId=<ID dự án của bạn>`

## Tương thích phiên bản với xeokit-sdk

Bắt đầu từ phiên bản 2.6.0, các bản phát hành của xeokit-bim-viewer đã được căn chỉnh với xeokit-sdk bằng cách khớp số phiên bản chính và phụ của chúng.
Điều này có nghĩa là đối với bất kỳ bản phát hành xeokit-sdk nào có phiên bản 2.6.x, bản phát hành xeokit-bim-viewer tương ứng sẽ tuân theo số 2.6.y.
Lưu ý rằng các số phiên bản vá giữa hai dự án được quản lý độc lập. Ví dụ, xeokit-bim-viewer 2.6.0 được xây dựng trên xeokit-sdk 2.6.67.


## Các bước tiếp theo

Đọc tài liệu bên dưới để bắt đầu.

---

* [Releases / Changelog](https://github.com/xeokit/xeokit-bim-viewer/releases)
* [Source Code](https://github.com/xeokit/xeokit-bim-viewer)
* [API Docs](https://xeokit.github.io/xeokit-bim-viewer/docs)
* [xeokit SDK](http://xeokit.io)

---

# Contents

- [Features](#features)
- [Demos](#demos)
- [License](#license)
- [The Viewer Application](#the-viewer-application)
- [Model Database](#model-database)
- [Viewer Configurations](#viewer-configurations)
    * [Viewer States](#viewer-states)
- [Deploying XKT V7 and Earlier](#deploying-xkt-v7-and-earlier)
- [Support for Multi-Part (Split) Models](#support-for-multi-part--split--models)
- [Split Model with Separate Metadata Files](#split-model-with-separate-metadata-files)
- [Programming API](#programming-api)
    * [Creating a Viewer](#creating-a-viewer)
    * [Configuring the Viewer](#configuring-the-viewer)
    * [Querying Projects, Models and Objects](#querying-projects--models-and-objects)
        + [Getting Info on Available Projects](#getting-info-on-available-projects)
        + [Getting Info on a Project](#getting-info-on-a-project)
        + [Getting Info on an Object](#getting-info-on-an-object)
    * [Loading Projects and Models](#loading-projects-and-models)
        + [Loading a Project](#loading-a-project)
        + [Loading a Model](#loading-a-model)
    * [Controlling Viewer State](#controlling-viewer-state)
    * [Saving and Loading BCF Viewpoints](#saving-and-loading-bcf-viewpoints)
- [Customizing Viewer Style](#customizing-viewer-style)
    * [Modal Busy Dialog](#modal-busy-dialog)
    * [Tooltips](#tooltips)
    * [Customizing Appearances of IFC Types](#customizing-appearances-of-ifc-types)
    * [Localizing a Viewer](#localizing-a-viewer)
- [xeokit Components Used in the Viewer](#xeokit-components-used-in-the-viewer)
- [Building the Viewer](#building-the-viewer)
    * [Installing from NPM](#installing-from-npm)
    * [Building the Binary](#building-the-binary)
    * [Building the Documentation](#building-the-documentation)

---

# Tính năng

* Sử dụng [xeokit](https://xeokit.io) để tải và hiển thị mô hình hiệu quả.
* Hoạt động trên tất cả các trình duyệt chính, bao gồm cả mobile.
* Có thể tải mô hình từ hệ thống tệp.
* Tải nhiều mô hình.
* Lưu và tải các điểm nhìn BCF.
* Chế độ xem 3D và 2D.
* Tương tác xuyên thấu, làm nổi bật, hiển thị, ẩn và cắt các đối tượng.
* Chế độ xem cây của cấu trúc, lớp và tầng.
* Hình học độ chính xác đầy đủ.
* Đám mây điểm.
* Hỗ trợ IFC2x3 và IFC4.
* Tùy chỉnh giao diện trình xem bằng CSS của riêng bạn.
* Hỗ trợ địa phương hóa.
* API lập trình JavaScript cho tất cả các chức năng của trình xem.

# Demo

Nhấp vào các liên kết bên dưới để chạy một số demo.

| Demo Trực tiếp | Nguồn Mô hình |
|---|---|
| [Double-Precision Model](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=MAP) | [BIMData](https://bimdata.io) |
| [Point Cloud](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=MAPPointCloud)| [BIMData](https://bimdata.io) |
| [OTC Conference Center](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=OTCConferenceCenter&tab=storeys) | [Details](http://openifcmodel.cs.auckland.ac.nz/Model/Details/301) |
| [OTC Conference Center (web component)](https://xeokit.github.io/xeokit-bim-viewer/webComponentExample.html) | [Details](http://openifcmodel.cs.auckland.ac.nz/Model/Details/301) |
| [Revit Sample Project](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=RevitSamples&tab=models) | [Details](https://knowledge.autodesk.com/support/revit-products/getting-started/caas/CloudHelp/cloudhelp/2020/ENU/Revit-GetStarted/files/GUID-61EF2F22-3A1F-4317-B925-1E85F138BE88-htm.html) |
| [Holter Tower](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=HolterTower&tab=storeys)| [Details](http://openifcmodel.cs.auckland.ac.nz/Model/Details/316) |
| [West Riverside Hospital](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=WestRiversideHospital&tab=models)| [Details](http://openifcmodel.cs.auckland.ac.nz/Model/Details/308) |
| [Schependomlaan](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=Schependomlaan&tab=storeys)| [Details](https://github.com/openBIMstandards/DataSetSchependomlaan) |
| [Schependomlaan Ground Floor](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=Schependomlaan_selectedStorey&tab=storeys)| [Details](https://github.com/openBIMstandards/DataSetSchependomlaan) |
| [Duplex](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=Duplex&tab=storeys)| [Details](http://openifcmodel.cs.auckland.ac.nz/Model/Details/274) |

# Giấy phép

xeokit-bim-viewer được đóng gói trong [xeokit SDK](http://xeokit.io), được cấp phép theo AGPL3. Xem
trang [Giá](https://xeokit.io/index.html#pricing) của chúng tôi để biết các tùy chọn giấy phép tùy chỉnh.

# Ứng dụng Trình xem

Trang [````./app/index.html````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/index.html) cung cấp một
phát tạo sẵn sàng sử dụng của xeokit-bim-viewer. Từ bây giờ chúng ta sẽ gọi nó là *trình xem*.

Trình xem tải các dự án và mô hình từ
thư mục [````./app/data/projects````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/data/projects).

Để xem một dự án, tải trình xem với ID của dự án trên URL:

[````https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=WestRiversideHospital````](https://xeokit.github.io/xeokit-bim-viewer/app/index.html?projectId=WestRiversideHospital)

# Cơ sở dữ liệu Mô hình

> **Phần này hướng dẫn cách thêm mô hình của riêng bạn vào ứng dụng trình xem. Các hướng dẫn này dựa trên các
> phiên bản gần đây nhất của XKT (V8 trở lên) và các công cụ chuyển đổi, mà bạn có thể tìm hiểu trong
*[Xem Mô hình IFC với xeokit](https://www.notion.so/xeokit/Viewing-an-IFC-Model-with-xeokit-c373e48bc4094ff5b6e5c5700ff580ee)*
.**

Hãy kiểm tra cấu trúc của
thư mục [````./app/data/projects````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/data), nơi
trình xem lưu trữ các dự án và mô hình của nó.

Bên dưới là một phần của thư mục ````./app/data/projects````. Chúng ta sẽ mô tả nó từ thư mục gốc
xuống dưới.

Trong thư mục gốc, chúng ta có một thư mục cho mỗi dự án, cùng với bản khai báo các dự án trong ````index.json````.

Trong thư mục dự án, chúng ta có một thư mục cho mỗi mô hình trong dự án, cùng với bản khai báo các mô hình
trong ````index.json````.

Trong thư mục mô hình, chúng ta có tệp ````.XKT```` chứa hình học và metadata của mô hình.

````
.app/data/projects
  │
  ├── index.json
  │
  ├── Duplex
  │     │
  │     ├── index.json
  │     │
  │     └── models
  │           └── design
  │                   └── geometry.xkt
  │
  └── WestRiversideHospital
        │
        ├── index.json
        │
        └── models
              ├── architecture
              │       └── geometry.xkt
              ├── structure
              │       └── geometry.xkt
              └── electrical
                      └── geometry.xkt
````

The ````index.json```` at the root of ````./app/data/projects```` is shown below.

Within this file, the ````id```` of each project matches the name of that project's subdirectory.

````json
{
  "projects": [
    {
      "id": "Duplex",
      "name": "Duplex"
    },
    {
      "id": "WestRiversideHospital",
      "name": "West Riverside Hospital"
    }
    //..
  ]
}
````

Tệp ````index.json```` cho dự án "WestRiversideHospital" được hiển thị bên dưới.

Trong tệp này, ````id```` của mỗi mô hình khớp với tên thư mục con của mô hình đó. ````name```` của mỗi mô hình
là tên dễ đọc được hiển thị trong tab Mô hình của trình xem.

````json
{
  "id": "WestRiversideHospital",
  "name": "West Riverside Hospital Project",
  "models": [
    {
      "id": "architectural",
      "name": "Hospital Architecture"
    },
    {
      "id": "structure",
      "name": "Hospital Structure"
    },
    {
      "id": "electrical",
      "name": "Hospital Electrical",
      "saoEnabled": false
    }
  ],
  "viewerConfigs": {
    "backgroundColor": [
      0.9,
      0.9,
      1.0
    ]
  },
  "viewerContent": {
    "modelsLoaded": [
      "structure",
      "architectural"
    ]
  },
  "viewerState": {
    "tabOpen": "models"
  }
}
````

Phần ````viewerConfigs```` tùy chọn chỉ định các cấu hình cho trình xem đặt cho chính nó khi tải
dự án. Xem danh sách đầy đủ các cấu hình trình xem có sẵn trong [Cấu hình Trình xem](#viewer-configurations).

Mảng ````viewerContent```` tùy chọn chỉ định các ID của mô hình mà trình xem sẽ tải ban đầu, ngay sau khi
áp dụng các cấu hình.

Phần ````viewerState```` tùy chọn chỉ định cách trình xem nên thiết lập trạng thái ban đầu của giao diện, ngay sau khi
đã tải các mô hình ban đầu. Xem danh sách đầy đủ các trạng thái trình xem có sẵn trong [Trạng thái Trình xem](#viewer-states).

Tệp ````geometry.xkt```` cho mỗi mô hình được tạo từ tệp IFC bằng các công cụ CLI mã nguồn mở. Tìm hiểu cách
tạo những tệp đó trong
*[Xem Mô hình IFC với xeokit](https://www.notion.so/xeokit/Viewing-an-IFC-Model-with-xeokit-c373e48bc4094ff5b6e5c5700ff580ee)*
.

# Cấu hình Trình xem

Bảng bên dưới liệt kê tập hợp đầy đủ các cấu hình có sẵn. Hãy coi chúng như là tùy chọn của người dùng. Chúng có thể được
cung cấp cho trình xem trong các tệp thông tin dự án, như mô tả trong [Cơ sở dữ liệu Mô hình](#model-database), hoặc đặt
bằng lập trình trên trình xem
với [````BIMViewer#setConfigs()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html#instance-method-setConfigs)
, như mô tả trong [Cấu hình Trình xem](#configuring-the-viewer).

| Thuộc tính               | Kiểu    | Phạm vi                  | Giá trị Mặc định         | Mô tả                                                                                                                                                                                                                                                                                                    |
|:-----------------------|:--------|:-----------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "backgroundColor"      | Array   |                        | ````[1.0,1.0,1.0]```` | Màu nền canvas                                                                                                                                                                                                                                                                                        |
| "cameraNear"           | Number  | ````[0.01-0.1]````     | ````0.05````          | Khoảng cách đến mặt phẳng cắt gần                                                                                                                                                                                                                                                                                            |
| "cameraFar"            | Number  | ````[1-100000000]````  | ````3000.0````        | Khoảng cách đến mặt phẳng cắt xa                                                                                                                                                                                                                                                                                             |
| "smartPivot"           | Boolean |                        | ````true````          | Bật trải nghiệm xoay quanh trục tốt hơn khi kéo chuột vào không gian trống ở chế độ xoay camera.                                                                                                                                                                                                            |
| "saoEnabled"           | Boolean |                        | ````true````          | Bật hay tắt Scalable Ambient Obscurance (SAO)                                                                                                                                                                                                                                                     |
| "saoBias"              | Number  | ````[0.0...10.0]````   | ````0.5````           | SAO bias                                                                                                                                                                                                                                                                                                       |
| "saoIntensity"         | Number  | ````[0.0...200.0]````  | ````100.0````         | SAO intensity factor                                                                                                                                                                                                                                                                                           |
| "saoScale"             | Number  | ````[0.0...1000.0]```` | ````500.0````         | SAO scale factor                                                                                                                                                                                                                                                                                               |
| "saoKernelRadius"      | Number  | ````[0.0...200.0]````  | ````100.0````         | The maximum area that SAO takes into account when checking for possible occlusion                                                                                                                                                                                                                              |
| "saoBlur"              | Boolean |                        | ````true````          | Whether Guassian blur is enabled for SAO                                                                                                                                                                                                                                                                       |
| "edgesEnabled"         | Boolean |                        | ````true````          | Whether or not to enhance edges on objects                                                                                                                                                                                                                                                                     |
| "pbrEnabled"           | Boolean |                        | ````false````         | Whether or not to enable Physically Based rendering (PBR)                                                                                                                                                                                                                                                      |
| "viewFitFOV"           | Number  | ````[10.0...70.0]````  | ````30````            | When fitting objects to view, this is the amount in degrees of how much they should fit the user's field of view                                                                                                                                                                                               |
| "viewFitDuration"      | Number  | ````[0..5]````         | ````0.5````           | When fitting objects to view with an animated transition, this is the duration of the transition in seconds                                                                                                                                                                                                    |
| "perspectiveFOV"       | Number  | ````[10.0...70.0]````  | ````55````            | When in perspective projection, this is the field of view, in degrees, that the user sees                                                                                                                                                                                                                      |
| "objectColors"         | Object  |                        | ````undefined````     | A map of custom attributes for various IFC types                                                                                                                                                                                                                                                               |
| "externalMetadata"     | Boolean |                        | ````false````         | Whether to load a metadata.json file with each geometry.xkt file                                                                                                                                                                                                                                               |
| "xrayPickable"         | Boolean |                        | ````false````         | Whether we can interact with X-rayed objects using mouse/touch input                                                                                                                                                                                                                                           |
| "selectedGlowThrough"  | Boolean |                        | ````true````          | Whether selected objects appear to "glow through" other objects                                                                                                                                                                                                                                                |
| "highlightGlowThrough" | Boolean |                        | ````true````          | Whether highlighted objects appear to "glow through" other objects                                                                                                                                                                                                                                             |
| "dtxEnabled"           | Boolean |                        | ````false````         | Whether to enable xeokit's data texture-based (DTX) scene representation and rendering mode. This has a lower memory footprint than the standard vertex buffer object-based (VBO) mode, and loads fast, but may be slower on low-spec GPUs.                                                                    |
| "showSpaces"           | Boolean |                        | ````false````         | Whether to enable the visibility of IfcSpace elements. When this is ````false````, then even though we can instruct BIMViewer to make IfcSpaces visible in the tree view or context menus, they will remain invisible. This config is also dynamically controlled by the "Show IfcSpaces" tool in the toolbar. |

## Trạng thái Trình xem

Trong [Cơ sở dữ liệu Mô hình](#model-database) chúng ta đã thấy cách một dự án có thể chỉ định hướng dẫn về cách trình xem nên thiết lập
trạng thái ban đầu của giao diện, ngay sau khi dự án đã được tải. Bảng bên dưới liệt kê các hướng dẫn có sẵn. Chúng cũng có thể
được đặt trên trình xem bằng cách sử dụng
[````BIMViewer#setViewerState()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html#instance-method-setViewerState)
. Hiện tại, chúng ta có:

| Thuộc tính              | Kiểu              | Phạm vi                 | Giá trị Mặc định     | Mô tả                      |
|:----------------------|:------------------|:----------------------|:------------------|:----------------------------------|
| "focusObject"         | String            |                       |                   | ID của đối tượng để làm nổi bật        |
| "tabOpen"             | String            |  "objects", "classes" hoặc "storeys"  |                   | Tab khám phá nào sẽ mở           |
| "expandObjectsTree"   | Number            |  [0..*]               | 0                 | Mở rộng cây "objects" sâu bao nhiêu |
| "expandClassesTree"   | Number            |  [0..*]               | 0                 | Mở rộng cây "classes" sâu bao nhiêu |
| "expandStoreysTree"   | Number            |  [0..*]               | 0                 | Mở rộng cây "storeys" sâu bao nhiêu |
| "setCamera"           | { eye: Number[], look: Number[], up: Number[] } |  | 0        | Vị trí camera |

# Triển khai XKT V7 và Cũ hơn

> **Phần này mô tả cách triển khai các mô hình sử dụng các phiên bản XKT cũ hơn không kết hợp hình học và metadata.
Đối với những phiên bản cũ hơn đó,
> chúng ta cần một chút công việc bổ sung để triển khai một tệp JSON metadata bổ sung cho mỗi mô hình.**

Phần trước đã mô tả cách triển khai các mô hình sử dụng XKT V8 và mới hơn. Định dạng XKT V8+ kết hợp hình học và
metadata vào cùng một tệp XKT, và được giới thiệu trong
[bản phát hành xeokit v1.9](https://www.notion.so/xeokit/What-s-New-in-xeokit-1-9-b7503ca7647e43e4b9c76e1505fa4484).

Các phiên bản XKT trước V8 chỉ chứa hình học, và cần được kèm theo một tệp JSON chứa
metadata IFC của mô hình. Trong phần này, chúng ta sẽ mô tả cách triển khai các mô hình sử dụng các phiên bản XKT trước V8.

Hãy tưởng tượng chúng ta muốn triển khai các dự án Duplex và West Riverside Hospital, sử dụng XKT V7. Đối với mỗi mô hình
trong cơ sở dữ liệu của chúng ta, chúng ta sẽ triển khai một ````geometry.xkt````, đây là tệp XKT V7 chứa hình học của mô hình, và
một ````metadata.json ````, chứa metadata IFC cho mô hình.

Chúng ta sẽ giả định rằng bạn đã có những tệp đó rồi, và chưa sẵn sàng chuyển đổi các tệp IFC gốc của chúng thành XKT
V8+.

Đây là các tệp cơ sở dữ liệu của chúng ta một lần nữa, lần này với XKT V7 và các tệp metadata kèm theo:

````
.app/data/projects
  │
  ├── index.json
  │
  ├── Duplex
  │     │
  │     ├── index.json
  │     │
  │     └── models
  │           └── design
  │                   ├── geometry.xkt
  │                   └── metadata.json
  │
  └── WestRiversideHospital
        │
        ├── index.json
        │
        └── models
              ├── architecture
              │       ├── geometry.xkt
              │       └── metadata.json
              ├── structure
              │       ├── geometry.xkt
              │       └── metadata.json
              └── electrical
                      ├── geometry.xkt
                      └── metadata.json
````

To make BIMViewer load both the ````geometry.xkt```` and ````metadata.json```` files for each model, we need to add a
new  ````externalMetadata: true```` configuration to the ````viewerConfigs```` in the project's ````index.json```` file:

````json
{
  "id": "WestRiversideHospital",
  "name": "West Riverside Hospital",
  "models": [
    {
      "id": "architectural",
      "name": "Hospital Architecture"
    },
    {
      "id": "structure",
      "name": "Hospital Structure"
    },
    {
      "id": "electrical",
      "name": "Hospital Electrical",
      "saoEnabled": false
    }
  ],
  "viewerConfigs": {
    "externalMetadata": true, // <<------------ ADD THIS
    "backgroundColor": [
      0.9,
      0.9,
      1.0
    ]
  },
  "viewerContent": {
    "modelsLoaded": [
      "structure",
      "architectural"
    ]
  },
  "viewerState": {
    "tabOpen": "models"
  }
}
````

# Hỗ trợ Mô hình Nhiều phần (Tách)

Kể từ xeokit-bim-viewer 2.4, chúng ta có thể triển khai các mô hình được chia thành nhiều tệp XKT (với các tệp JSON
metadata bên ngoài tùy chọn).

Công cụ `ifc2gltf` từ Creoox, chuyển đổi các tệp IFC thành các tệp hình học glTF và metadata JSON, có tùy chọn
chia đầu ra của nó thành nhiều cặp tệp glTF và JSON, kèm theo một bản khai báo JSON liệt kê các tệp.

Để tích hợp với tùy chọn đó, công cụ `convert2xkt`, chuyển đổi các tệp hình học glTF và metadata JSON thành các tệp XKT,
cũng có tùy chọn chuyển đổi hàng loạt các tệp glTF+JSON trong bản khai báo, trong một lần gọi.

Khi chúng ta sử dụng tùy chọn này, convert2xkt sẽ xuất ra một loạt các tệp XKT, cùng với một tệp bản khai báo JSON liệt kê những
tệp XKT đó.

Tính năng này mở rộng BIMViewer với tùy chọn tải các mô hình gồm nhiều tệp XKT, kết hợp các tệp XKT vào một chế độ xem cây duy nhất cho mỗi mô hình, và cho phép bỏ tải mô hình để bỏ tải tất cả các tệp XKT của nó trong một lần. Nói cách khác, thay vì có một mô hình và chế độ xem cây riêng cho mỗi XKT, bây giờ chúng ta có thể nhóm một loạt các tệp XKT lại để hoạt động như một mô hình trong BIMViewer.

Tìm hiểu thêm về việc chuyển đổi các mô hình IFC thành nhiều tệp XKT trong [hướng dẫn này](https://www.notion.so/xeokit/Importing-Huge-IFC-Models-as-Multiple-XKT-Files-165fc022e94742cf966ee50003572259).

Để cho thấy cách triển khai một trong những mô hình multi-XKT này trong BIMViewer, hãy xem xét dự án Karhumaki.

---
* [Load the Karhumaki Project in BIMViewer](https://xeokit.io/demo.html?projectId=Karhumaki)
---

````
.app/data/projects
  │
  ├── index.json
  │
  └── Karhumaki
        │
        ├── index.json
        │
        └── models
              └──  KarhumakiBridge
                      ├── manifest.json
                      ├── model.xkt
                      ├── model_1.xkt
                      ├── model_2.xkt
                      ├── model_3.xkt
                      ├── model_4.xkt
                      ├── model_5.xkt
                      ├── model_6.xkt
                      ├── model_7.xkt
                      ├── model_8.xkt
                      └── model_9.xkt
````

Tệp bản khai báo XKT `manifest.json` trông như sau:

````json
{
  "xktFiles": [
    "model.xkt",
    "model_1.xkt",
    "model_2.xkt",
    "model_3.xkt",
    "model_4.xkt",
    "model_5.xkt",
    "model_6.xkt",
    "model_7.xkt",
    "model_8.xkt",
    "model_9.xkt"
  ]
}
````

Tệp ````index.json```` cho dự án "Karhumaki" được hiển thị bên dưới.

Trong tệp này, như thường lệ, ````id```` của mỗi mô hình khớp với tên thư mục con của mô hình đó. ````name```` của mỗi mô hình là tên dễ đọc được hiển thị trong tab Mô hình của trình xem.

Để chỉ ra rằng mô hình là mô hình nhiều phần, với nhiều XKT, mục mô hình nhận một thuộc tính ````manifest```` chứa tên tệp của tệp `manifest.json` của chúng ta.

Trong `viewerContent`, chúng ta chỉ định rằng mô hình nhiều phần của chúng ta được tải ngay lập tức, ngay khi dự án được tải.

````json
{
  "id": "Karhumaki",
  "name": "Karhumaki",
  "models": [
    {
      "id": "Karhumaki-Bridge",
      "name": "Karhumaki Bridge",
      "manifest": "manifest.json"
    }
  ],
  "viewerConfigs": {
    "backgroundColor": [
      0.9,
      0.9,
      1.0
    ]
  },
  "viewerContent": {
    "modelsLoaded": [
      "Karhumaki-Bridge"
    ]
  },
  "viewerState": {
    "tabOpen": "models"
  }
}
````

# Mô hình Tách với Các Tệp Metadata Riêng

Trong các phiên bản gần đây của xeokit, chúng ta kết hợp hình học và metadata vào các tệp XKT, để đơn giản trong quy trình, như chúng ta đã thực hiện trong ví dụ trên.

Trong các phiên bản cũ hơn của XKT, như đã đề cập ở trên, chúng ta sẽ có metadata trong các tệp JSON riêng biệt, do đó mỗi tệp XKT sẽ có hình học, và sẽ được kèm theo một tệp JSON chứa metadata IFC của nó.

BIMViewer, và phần còn lại của xeokit SDK, vẫn tương thích ngược với việc tách XKT+JSON này. Tính năng tải mô hình tách cũng vẫn tương thích ngược, như được minh họa trong dự án ví dụ "WestRiversideHospital_Combined", được mô tả bên dưới.

---
* [Load the WestRiversideHospital_Combined Project in BIMViewer](https://xeokit.io/demo.html?projectId=WestRiversideHospital_Combined)
---

Chúng ta có các tệp XKT và metadata JSON tách rời trong thư mục `models`:

````
.app/data/projects
  │
  ├── index.json
  │
  └── WestRiversideHospital_Combined
    ├── index.json
    │
    └── models
        │
        └── WestRiversideHospital
            ├── architectural.json
            ├── architectural.xkt
            ├── electrical.json
            ├── electrical.xkt
            ├── fireAlarms.json
            ├── fireAlarms.xkt
            ├── manifest.json
            ├── mechanical.json
            ├── mechanical.xkt
            ├── plumbing.json
            ├── plumbing.xkt
            ├── sprinklers.json
            ├── sprinklers.xkt
            ├── structure.json
            └── structure.xkt
````

Tệp bản khai báo XKT `manifest.json` trông như bên dưới. Lưu ý thuộc tính `metaModelFiles` bổ sung, liệt kê các tệp JSON bao gồm metamodel cho mô hình "WestRiversideHospital":

````
{
  "xktFiles": [
    "architectural.xkt",
    "electrical.xkt",
    "fireAlarms.xkt",
    "mechanical.xkt",
    "plumbing.xkt",
    "sprinklers.xkt",
    "structure.xkt"
  ],
  "metaModelFiles": [
    "architectural.json",
    "electrical.json",
    "fireAlarms.json",
    "mechanical.json",
    "plumbing.json",
    "sprinklers.json",
    "structure.json"
  ]
}
````

Cuối cùng, ````index.json```` cho dự án "WestRiversideHospital_Combined" được hiển thị bên dưới.

Trong tệp này, như trước, ````id```` của mỗi mô hình khớp với tên thư mục con của mô hình đó, và ````name```` của mỗi mô hình là tên dễ đọc được hiển thị trong tab Mô hình của trình xem.

Như trước, để chỉ ra rằng mô hình là mô hình nhiều phần, với nhiều XKT, mục mô hình nhận một thuộc tính ````manifest```` chứa tên tệp của tệp `manifest.json` của chúng ta.

Trong `viewerContent`, chúng ta chỉ định rằng mô hình nhiều phần của chúng ta được tải ngay lập tức, ngay khi dự án được tải.

````json
{
    "id": "WestRiversideHospital_Combined",
    "name": "West Riverside Hospital",
    "models": [
        {
            "id": "WestRiversideHospital",
            "name": "West Riverside Hospital",
            "saoEnabled": true,
            "manifest": "manifest.json"
        }
    ],
    "viewerConfigs": {
        "backgroundColor": [0.9, 0.9, 1.0],
        "externalMetadata": true
    },
    "viewerContent": {
        "modelsLoaded": [
            "WestRiversideHospital"
        ]
    },
    "viewerState": {
        "viewCubeEnabled": true,
        "threeDEnabled": true,
        "tabOpen": "models"
    }
}
````

# API Lập trình

> **Phần này đi sâu hơn vào trình xem, mô tả cách khởi tạo một trình xem và cách sử dụng API lập trình JavaScript
của nó.**

Trình xem được triển khai bởi lớp
JavaScript [````BIMViewer````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html)
, cung cấp một tập hợp đầy đủ các phương thức để điều khiển nó bằng lập trình.

Sử dụng các phương thức này, chúng ta có thể:

* tạo và cấu hình một trình xem,
* truy vấn những mô hình nào có sẵn,
* tải các dự án và mô hình,
* tương tác với chế độ xem 3D,
* lưu và tải các điểm nhìn BCF,
* điều khiển các công cụ khác nhau của trình xem, và
* điều khiển trạng thái giao diện của trình xem.

## Tạo một Trình xem

Trong ví dụ bên dưới, chúng ta sẽ tạo một
[````BIMViewer````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html), với
một [````Server````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/server/Server.js~Server.html) qua đó
nó sẽ tải các dự án và mô hình từ hệ thống tệp.

Chúng ta sẽ cấu hình ````Server```` để tải dữ liệu đó từ
thư mục [````./app/data````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/data).

Chúng ta cũng sẽ cấu hình ````BimViewer```` của chúng ta với các phần tử DOM để chứa bốn phần của giao diện, bao gồm:

1. canvas 3D,
2. bảng khám phá chứa các chế độ xem cây,
3. thanh công cụ,
4. NavCube, và
4. phần tử "backdrop", bao phủ mọi thứ trong giao diện để ngăn chặn tương tác bất cứ khi nào trình xem đang bận tải
   một mô hình.

````javascript
const server = new Server({
    dataDir: "./data"
});

const myBIMViewer = new BIMViewer(server, {
    canvasElement: document.getElementById("myCanvas"),                // Canvas WebGL 3D
    explorerElement: document.getElementById("myExplorer"),            // Container cho bảng khám phá
    toolbarElement: document.getElementById("myToolbar"),              // Container cho thanh công cụ
    navCubeCanvasElement: document.getElementById("myNavCubeCanvas"),  // Canvas cho NavCube
    busyModelBackdropElement: document.querySelector(".xeokit-busy-modal-backdrop") // Phần tử backdrop hộp thoại bận
});
````

Cấu hình ````BIMViewer```` với các vị trí riêng biệt trong tài liệu để định vị các phần của nó cho phép chúng ta tích hợp chúng
linh hoạt hơn vào trang web của chúng ta.

Trong trang [````app/index.html````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/app/index.html) của chúng ta, các
phần tử HTML trông như sau:

````html

<div id="myViewer" class="xeokit-busy-modal-backdrop">
    <div id="myExplorer" class="active"></div>
    <div id="myContent">
        <div id="myToolbar"></div>
        <canvas id="myCanvas"></canvas>
    </div>
</div>
<canvas id="myNavCubeCanvas"></canvas>
````

Xem [````app/css/style.css````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/app/css/style.css) để biết cách chúng ta đã
tạo kiểu cho các phần tử này.

Cũng
xem [````dist/xeokit-bim-viewer.css````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/dist/xeokit-bim-viewer.css)
cho các kiểu CSS mà BIMViewer áp dụng cho các phần tử nó tạo ra bên trong.

## Cấu hình Trình xem

Với trình xem của chúng ta đã được tầo, hãy
sử dụng [````BIMViewer#setConfigs()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html#instance-method-setConfigs)
để cấu hình nó.

Chúng ta sẽ chỉ đặt màu nền canvas thành trắng:

````javascript
myBIMViewer.setConfigs({
    "backgroundColor": [1.0, 1.0, 1.0]
});
````

See [Viewer Configurations](#viewer-configurations) for the list of available configurations.

## Truy vấn Dự án, Mô hình và Đối tượng

Với trình xem của chúng ta đã được tạo và cấu hình, hãy tìm hiểu nội dung nào có sẵn.

### Lấy Thông tin về Các Dự án Có sẵn

Hãy truy vấn những dự án nào có sẵn.

````javascript
myBIMViewer.getProjectsInfo((projectsInfo) => {
    console.log(JSON.stringify(projectsInfo, null, "\t"));
});
````

Bên trong, trình xem sẽ
gọi [````Server#getProjects()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/server/Server.js~Server.html#instance-method-getProjects)
để lấy thông tin dự án.

Như đã mô tả trước đó trong [Cơ sở dữ liệu Mô hình](#model-database), thông tin dự án là JSON
trong [````./app/data/projects/index.json````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/data/projects/index.json)
. Chúng ta sẽ chỉ ghi lại thông tin đó vào console.

Thông tin dự án sẽ trông tương tự:

````json
{
  "projects": [
    {
      "id": "Duplex",
      "name": "Duplex"
    },
    {
      "id": "Schependomlaan",
      "name": "Schependomlaan"
    },
    {
      "id": "WestRiversideHospital",
      "name": "West Riverside Hospital"
    }
  ]
}
````

### Lấy Thông tin về một Dự án

Bây giờ chúng ta biết những dự án nào có sẵn, chúng ta sẽ lấy thông tin về một trong những dự án đó.

````javascript
myBIMViewer.getProjectInfo("WestRiversideHospital", (projectInfo) => {
    console.log(JSON.stringify(projectInfo, null, "\t"));
});
````

Bên trong, trình xem sẽ
gọi [````Server#getProject()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/server/Server.js~Server.html#instance-method-getProject)
để lấy thông tin dự án đó. Giống như trước, chúng ta sẽ chỉ ghi lại nó vào console.

Thông tin dự án sẽ là nội dung
của [````./app/data/projects/WestRiversideHospital/index.json````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/data/projects/WestRiversideHospital/index.json)
.

Thông tin dự án sẽ tương tự:

````json
{
  "id": "WestRiversideHospital",
  "name": "West Riverside Hospital",
  "models": [
    {
      "id": "architectural",
      "name": "Hospital Architecture"
    },
    {
      "id": "structure",
      "name": "Hospital Structure"
    },
    {
      "id": "electrical",
      "name": "Hospital Electrical",
      "saoEnabled": false
    }
  ],
  "viewerConfigs": {
    "backgroundColor": [
      0.9,
      0.9,
      1.0
    ],
    "saoEnabled": true
  },
  "viewerContent": {
    "modelsLoaded": [
      "structure",
      "architectural"
    ]
  },
  "viewerState": {
    "tabOpen": "models"
  }
}
````

Trong thông tin dự án này, chúng ta có:

* **````id````** - ID của dự án,
* **````name````** - tên dễ đọc của dự án,
* **````models````** - thông tin về mỗi mô hình trong dự án này,
* **````viewerConfigs````** - các cấu hình cho trình xem áp dụng khi tải dự án,
* **````viewerContent````** - những mô hình nào trình xem nên tải ngay lập tức khi tải dự án, và
* **````viewerState````** - cách trình xem nên thiết lập giao diện sau khi tải dự án.

Khi chúng ta tải dự án sau trong phần [Tải một Dự án](#loading_a_project), trình xem sẽ truyền
````viewerConfigs````
cho [````BIMViewer#setConfigs()````](https://xeokit.github.io/xeokit-sdk/docs/class/src/BIMViewer.js~BIMViewer.html#instance-method-setConfigs)
, mà chúng ta đã mô tả trước đó trong [Cấu hình Trình xem](#configuring-the-viewer).

Trong ````viewerConfigs```` chúng ta đang bật hiệu ứng Scalable Ambient Obscurance của trình xem, sẽ tạo ra các bóng tối xung quanh
trong các rãnh của mô hình. Đây là một hiệu ứng tốn kém cho trình xem để render, nên chúng ta đã tắt nó cho
mô hình "electrical", chứa nhiều đối tượng dây dài và mỏng không thể hiện hiệu ứng SAO tốt.

### Lấy Thông tin về một Đối tượng

Hãy thử lấy một số thông tin về một đối tượng trong một trong các mô hình của dự án.

Chúng ta nói "thử" vì tùy thuộc vào
[````Server````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/server/Server.js~Server.html) để thử
tìm thông tin đó cho chúng ta, có thể không tồn tại.

Bên trong, trình xem sẽ
gọi [````Server#getObjectInfo()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/server/Server.js~Server.html#instance-method-getObjectInfo)
, sẽ thử tải thông tin đối tượng đó từ một tệp.

Nếu bạn thay thế ````Server```` bằng triển khai của riêng bạn, triển khai của bạn có thể lấy thông tin đó từ một
kho lưu trữ dữ liệu, chẳng hạn như cơ sở dữ liệu quan hệ, được điền với metadata cho tất cả các đối tượng trong mô hình của dự án, khóa
với ID của chúng.

Chúng ta sẽ tiếp tục và giả định rằng ````Server```` của chúng ta có thông tin về một đối tượng.

````javascript
myViewer.getObjectInfo("WestRiversideHospital", "architectural", "2HaS6zNOX8xOGjmaNi_r6b",
    (objectInfo) => {
        console.log(JSON.stringify(objectInfo, null, "\t"));
    },
    (errMsg) => {
        console.log("Oops! There was an error getting info for this object: " + errMsg);
    });
````

Nếu đối tượng không tồn tại trong dự án và mô hình được chỉ định, phương thức sẽ gọi callback lỗi của nó.

Cơ sở dữ liệu hệ thống tệp của chúng ta tình cờ có thông tin cho đối tượng đó, được lưu trữ
trong [````./app/data/projects/WestRiversideHospital/models/architectural/objects/2HaS6zNOX8xOGjmaNi_r6b.json````](https://github.com/xeokit/xeokit-bim-viewer/tree/master/app/data/projects/WestRiversideHospital/models/architectural/objects/2HaS6zNOX8xOGjmaNi_r6b.json)
.

Vì thông tin đối tượng của chúng ta tồn tại, chúng ta sẽ nhận được kết quả tương tự như sau:

````json
{
  "id": "2HaS6zNOX8xOGjmaNi_r6b",
  "projectId": "WestRiversideHospital",
  "modelId": "architectural",
  "name": "Basic Wall:Exterior - Metal Panel on Mtl. Stud:187578",
  "type": "IfcWall",
  "parent": "2hExBg8jj4NRG6zzD0RZML"
}
````

> Đến lúc này, bạn có thể đã nhận thấy rằng cơ sở dữ liệu hệ thống tệp của chúng ta được cấu trúc để
> hỗ trợ [RESTful](https://en.wikipedia.org/wiki/Representational_state_transfer) URI, mà
> [````Server````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/server/Server.js~Server.html) của chúng ta xây dựng
> từ các ID dự án, mô hình và đối tượng chúng ta cung cấp cho các phương thức truy vấn của trình xem.

## Tải Dự án và Mô hình

Bây giờ hãy tải một số dự án và mô hình mà chúng ta đã truy vấn trong phần trước.

### Tải một Dự án

Hãy bắt đầu bằng cách tải dự án mà chúng ta vừa truy vấn thông tin.

````javascript
myBIMViewer.loadProject("WestRiversideHospital",
    () => {
        console.log("Nice! The project loaded successfully.");
    },
    (errMsg) => {
        console.log("Oops! There was an error loading this project: " + errMsg);
    });
````

Nếu thành công, trình xem bây giờ sẽ có hai mô hình được tải, ````"architectural"```` và ````"structure"````, vì
những mô hình này được chỉ định trong ````viewerContent```` của thông tin dự án.

Trình xem cũng sẽ bật Scalable Ambient Obscurance, vì điều đó được chỉ định bởi thuộc tính ````saoEnabled```` trong
````viewerConfigs````. Trình xem cũng sẽ đặt nhiều cấu hình khác trên chính nó, như chỉ định trong phần đó.

Trình xem cũng sẽ mở tab "Models" của nó, nhờ vào thuộc tính ````tabOpen```` trong phần
````viewerState```` của thông tin dự án.

Chúng ta có thể xác nhận rằng hai mô hình đã được tải bằng cách truy vấn các ID của các mô hình hiện đang được tải trong trình xem:

````javascript
const modelIds = myBIMViewer.getModelLoadedIds();

console.log(modelIds);
````

The result would be:

````json
[
  "architectural",
  "structure"
]
````

### Tải một Mô hình

Với dự án của chúng ta đã được tải, hãy tải một mô hình khác của nó.

Chúng ta có thể bắt đầu bằng cách lấy ID của tất cả các mô hình trong dự án của chúng ta, chỉ để đảm bảo mô hình có sẵn:

````javascript
const modelIds = myBIMViewer.getModelIds();

console.log(modelIds);
````

The result would be:

````json
[
  "architectural",
  "structure",
  "electrical"
]
````

To load the model:

````javascript
myBIMViewer.loadModel("electrical",
    () => {
        console.log("Nice! The model loaded successfully.");
    },
    (errMsg) => {
        console.log("Oops! There was an error loading this model: " + errMsg);
    });
````

Nếu chúng ta không còn cần mô hình đó nữa, chúng ta có thể bỏ tải nó lại:

````javascript
myBIMViewer.unloadModel("electrical");
````

Khi chúng ta không còn cần dự án, bỏ tải như sau:

````javascript
myBIMViewer.unloadProject();
````

Lưu ý rằng chúng ta chỉ có thể tải một dự án tại một thời điểm.

## Điều khiển Trạng thái Trình xem

[````BIMViewer````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html) có nhiều
phương thức mà chúng ta có thể điều khiển trạng thái giao diện của nó bằng lập trình.

Hãy xem nhanh một số phương thức này để hiểu được loại trạng thái giao diện nào chúng ta có thể điều khiển với chúng. Đây
sẽ không phải là hướng dẫn toàn diện - xem tài liệu lớp ````BIMViewer```` để biết danh sách đầy đủ.

Sau khi đã tải một vài mô hình trong phần trước, hãy mở tab Objects của trình xem, chứa chế độ xem cây
của hệ thống phân cấp chứa các đối tượng trong những mô hình đó:

````javascript
myBIMViewer.openTab("objects");
````

To confirm which tab is currently open:

````javascript
const tabId = myBIMViewer.getOpenTab();

console.log("Currently open tab: '" + tabId + "'"); // "objects"
````

Now let's arrange the camera to fit an object in view:

````javascript
myBIMViewer.flyToObject("1fOVjSd7T40PyRtVEklS6X", () => { /* Done */
});
````

TODO: Complete this section once API methods are finalized

## Lưu và Tải Điểm nhìn BCF

[Bim Collaborative Format](https://en.wikipedia.org/wiki/BIM_Collaboration_Format) (BCF) là một định dạng để quản lý các vấn đề
trong dự án BIM. Một bản ghi BCF ghi lại trạng thái hình ảnh của trình xem BIM, bao gồm vị trí camera,
trạng thái hiển thị và chọn của các đối tượng, và bất kỳ mặt phẳng cắt nào hiện đang hoạt động.

Một bản ghi BCF được lưu từ một trình xem BIM có thể được tải vào trình xem khác, để đồng bộ trạng thái hình ảnh của cả hai
trình xem.

Lưu ý rằng các điểm nhìn BCF không ghi lại mô hình nào hiện đang được tải. Giả định rằng cả trình xem nguồn và đích
đều có các mô hình giống nhau được tải.

Sử dụng
[````BIMViewer#saveBCFViewpoint()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html#instance-method-saveBCFViewpoint)
để lưu bản ghi BCF JSON của chế độ xem hiện tại:

````javascript
const viewpoint = bimViewer.saveBCFViewpoint({
    // Options - see BIMViewer#saveBCFViewpoint() documentation for details
});
````

JSON điểm nhìn của chúng ta sẽ trông tương tự như bên dưới. Trước khi lưu điểm nhìn này, chúng ta đã ẩn một đối tượng, chọn một
đối tượng khác, và tạo mặt phẳng cắt để cắt mô hình của chúng ta. Điểm nhìn cũng chứa một ảnh chụp PNG của canvas của trình xem,
mà chúng ta đã cắt bớt ở đây cho ngắn gọn.

````
{
    perspective_camera: {
        camera_view_point: { x: 0.0, y: 0.0, z: 0.0 },
        camera_direction: { x: 1.0, y: 1.0, z: 2.0 },
        camera_up_vector: { x: 0.0, y: 0.0, z: 1.0 },
        field_of_view: 90.0
    },
    lines: [],
    clipping_planes: [{
        location: { x: 0.5, y: 0.5, z: 0.5 },
        direction: { x: 1.0, y: 0.0, z: 0.0 }
    }],
    bitmaps: [],
    snapshot: {
        snapshot_type: png,
        snapshot_data: "data:image/png;base64,......"
    },
    components: {
        visibility: {
            default_visibility: false,
            exceptions: [{
                ifc_guid: 4$cshxZO9AJBebsni$z9Yk,
                originating_system: xeokit.io,
                authoring_tool_id: xeokit/v1.0
            }]
       },
        selection: [{
           ifc_guid: "4$cshxZO9AJBebsni$z9Yk",
        }]
    }
}
````

Sử dụng
[````BIMViewer#loadBCFViewpoint()````](https://xeokit.github.io/xeokit-bim-viewer/docs/class/src/BIMViewer.js~BIMViewer.html#instance-method-loadBCFViewpoint)
để tải bản ghi BCF JSON:

````javascript
bimViewer.loadBCFViewpoint(viewpoint, {
    // Options - see BIMViewer#loadBCFViewpoint() documentation for details
});
````

# Tùy chỉnh Kiểu Trình xem

Tệp [````app/index.html````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/app/index.html) cho
trình xem độc lập chứa các quy tắc CSS cho các phần tử trình xem khác nhau, mà bạn có thể sửa đổi theo yêu cầu.

## Hộp thoại Bận Modal

Trình xem hiển thị một hộp thoại modal bất cứ khi nào chúng ta tải một mô hình. Hộp thoại có một phần tử backdrop, phủ lên
trình xem. Bất cứ khi nào hộp thoại hiển thị, backdrop sẽ chặn các sự kiện tương tác trên giao diện của trình xem.

Within our [````app/index.html````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/app/index.html) page, the
main ````<div>```` is the backdrop element:

````html

<div id="myBIMViewer" class="xeokit-busy-modal-backdrop">
    <div id="myExplorer" class="active"></div>
    <div id="myContent">
        <div id="myToolbar"></div>
        <canvas id="myCanvas"></canvas>
    </div>
</div>
<canvas id="myNavCubeCanvas"></canvas>
````

Như được định nghĩa trong [````css/BIMViewer.css````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/css/BIMViewer.css),
backdrop nhận kiểu sau, cho phép hộp thoại định vị chính xác bên trong backdrop:

````css
.xeokit-busy-modal-backdrop {
    position: relative;
}
````

Nếu bản cần điều chỉnh CSS liên quan đến hộp thoại, tìm kiếm "xeokit-busy-dialog"
trong [````css/BIMViewer.css````](https://github.com/xeokit/xeokit-bim-viewer/blob/master/css/BIMViewer.css).

## Chú thích công cụ

Chú thích công cụ không phải là một phần của JavaScript cốt lõi cho trình xem. Thay vào đó, các phần tử HTML của trình xem được đánh dấu
với các thuộc tính ````data-tippy-content```` cung cấp các chuỗi để hiển thị trong chú thích công cụ của chúng.

Ví dụ, phần tử nút *Toggle 2D/3D* trông như sau:

````html

<button type="button" class="xeokit-threeD xeokit-btn fa fa-cube fa-2x" data-tippy-content="Toggle 2D/3D"></button>
````

Trong tệp [app/index.html](https://github.com/xeokit/xeokit-bim-viewer/blob/master/app/index.html) cho trình xem độc lập,
chúng ta đang sử dụng [tippy.js](https://github.com/atomiks/tippyjs), tự động tạo chú thích công cụ cho những
phần tử đó.

## Tùy chỉnh Giao diện của Các Loại IFC

Mặc định, BIMViewer tải bất kỳ màu sắc và độ mờ đục nào có trong các tệp mô hình XKT, mà không thay đổi chúng.
Tuy nhiên, đôi khi, một số loại đối tượng nhất định có thể có màu sắc khiến chúng ta khó xem mô hình.

Ví dụ, trong một số mô hình IFC, các loại ````IfcPlate```` có thể được sử dụng để đại diện cho cửa sổ, và những loại đó thường được cho màu đục.
Điều đó dẫn đến các cửa sổ của mô hình chúng ta bị đục. Đối với ví dụ này, chúng ta có thể làm cho cửa sổ trong suốt
bằng cách cấu hình BIMViewer, hoặc chỉ mô hình đó, với màu sắc hoặc độ mờ đục tùy chỉnh, cho loại ````IfcPlate```` đó. Điều đó sẽ làm cho
tất cả các loại ````IfcPlate```` trong suốt trở lại. Có hai cách chúng ta có thể thực hiện điều này - bằng lập trình qua ````BIMViewer.setConfigs````, hoặc
cho mỗi dự án riêng lẻ, qua tệp `index.json` của dự án.

In the code below, we'll configure all ````IfcSpace````, ````IfcWindow````, ````IfcOpeningElement```` and ````IfcPlate```` types
to be transparent, and while we're at it, we'll make ````IfcWindow```` types to be always blue. Note that all values are in range ````[0..1]````.

---

 Lưu ý rằng trước v2.4, BIMViewer đã thay đổi màu sắc và độ mờ đục của `IfcOpening`, `IfcSpace`, `IfcWindow` và `IfcPlate` theo
 mặc định. Chúng tôi đã xóa điều đó trong v2.4, vì nó gây nhầm lẫn
 và người dùng tự hỏi tại sao những loại đối tượng đó không có màu sắc/độ mờ đục được định nghĩa cho chúng trong mô hình.

---

````javascript
// In case the model has opaque colors for IfcSpace, IfcWindow, IfcOpeningElement and IfcPlate
// objects, let's make those objects always transparent. To make the model look extra nice,
// let's force IfcWindows to always be blue, while we're at it. This will apply to all models,
// except where we override the settings per-project, as shown next.

bimViewer.setConfigs({
      "objectColors": {
            "IfcSpace": {
                "opacity": 0.3
            },
            "IfcWindow": {
                "opacity": 0.4,
                "color": [0, 0, 1]
            },
            "IfcOpeningElement": {
                "opacity": 0.3
            },
            "IfcPlate": {
                "opacity": 0.3
            }
        }
});
````

The other way we can set these color/opacity customizations is per-project, within the ````viewerConfigs```` section of
a project's ````index.json```` file. If we've also set them via ````BIMViewer.setConFigs````, then these will override
the ones set via that method.

As an example, we've done this for the `OTCConferenceCenter` demo model, which otherwise has its windows opaque, which would make it hard
for us to navigate around that model. Therefore, we provide a custom map of colors and opacities for certain IFC types via
the ```viewerConfigs``` in the [project ````index.json```` for that model](https://github.com/xeokit/xeokit-bim-viewer/blob/master/app/data/projects/OTCConferenceCenter/index.json), as shown below.

````json
{
    "id": "otcConferenceCenter",
    "name": "OTC Conference Center",
    "models": [
        {
            "id": "design",
            "name": "OTC Conference Center Design"
        }
    ],
    "viewerConfigs": {
        "backgroundColor": [
            0.95,
            0.95,
            1.0
        ],
        "objectColors": {
            "IfcSpace": {
                "opacity": 0.3
            },
            "IfcWindow": {
                "opacity": 0.4
            },
            "IfcOpeningElement": {
                "opacity": 0.3
            },
            "IfcPlate": {
                "opacity": 0.3
            }
        }
    },
    "viewerContent": {
        "modelsLoaded": [
            "design"
        ]
    },
    "viewerState": {
        "tabOpen": "objects",
        "expandObjectsTree": 3,
        "expandClassesTree": 1,
        "expandStoreysTree": 1
    }
}
````


## Địa phương hóa Trình xem

Cách dễ nhất để địa phương hóa BIMViewer là tải các chuỗi dịch vào dịch vụ locale của nó, được triển khai
bởi
xeokit [LocaleService](https://xeokit.github.io/xeokit-sdk/docs/class/src/viewer/localization/LocaleService.js~LocaleService.html)
.

Đoạn mã bên dưới cho thấy cách thực hiện, sử dụng một tập hợp một phần các bản dịch được mong đợi bởi các thành phần
trong BIMViewer. Chúng ta sẽ chỉ hiển thị các bản dịch cho các mặt của NavCube. Chúng ta cũng sẽ tải các bản dịch
nhanh chóng, thay vì lấy chúng từ một tệp JSON riêng biệt, như chúng ta sẽ làm trong thực tế.

Chúng ta gọi các bản dịch là "messages" (thông điệp). Ẩn dụ của chúng ta là giao diện "truyền tải thông điệp tới người dùng".

Để xem tất cả các bản dịch được mong đợi bởi BIMViewer, hãy xem các bản dịch chúng tôi đã cấu hình cho ứng dụng
BIMViewer demo đã đóng gói:  [````/app/locales/messages.js````](/app/locales/messages.js).

````javascript
myBIMViewer.localeService.loadMessages({
    "en": { // English
        "NavCube": {
            "front": "Front",
            "back": "Back",
            "top": "Top",
            "bottom": "Bottom",
            "left": "Left",
            "right": "Right"
        },
        //..
    },
    "mi": { // Māori
        "NavCube": {
            "front": "Mua",
            "back": "Tuarā",
            "top": "Runga",
            "bottom": "Raro",
            "left": "Mauī",
            "right": "Tika"
        },
        //..
    },
    "fr": { // French
        "NavCube": {
            "front": "Avant",
            "back": "Arrière",
            "top": "Supérieur",
            "bottom": "Inférieur",
            "left": "Gauche",
            "right": "Droit"
        },
        //..
    },
    "jp": { // Japanese
        "NavCube": {
            "front": "前部",
            "backLabel": "裏",
            "topLabel": "上",
            "bottomLabel": "底",
            "leftLabel": "左",
            "rightLabel": "右"
        },
        //..
    },
});
````

Sau khi chúng ta đã tải các bản dịch, chúng ta có thể chuyển đổi BIMViewer giữa các ngôn ngữ như sau:

````javascript
myBIMViewer.localeService.locale = "jp";
````

# Các Thành phần xeokit Được Sử dụng trong Trình xem

Trình xem được xây dựng trên nhiều thành phần và plugin [xeokit SDK](http://xeokit.io) được thiết kế để tăng tốc
việc phát triển các ứng dụng trực quan hóa BIM và CAD.

Bảng bên dưới liệt kê các thành phần chính được sử dụng trong trình xem này.

| Thành phần              | Mục đích          |
|:-----------------------|:------------------|
| [````Viewer````](https://xeokit.github.io/xeokit-sdk/docs/class/src/viewer/Viewer.js~Viewer.html) | Trình xem dựa trên WebGL ở tròng tâm của ````BIMViewer````. |
| [````XKTLoaderPlugin````](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/XKTLoaderPlugin/XKTLoaderPlugin.js~XKTLoaderPlugin.html)  | Tải hình học và metadata của mô hình. |
| [````NavCubePlugin````](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/NavCubePlugin/NavCubePlugin.js~NavCubePlugin.html)  | Công cụ hình khối điều hướng cho phép chúng ta xoay cảnh và di chuyển camera để nhìn theo trục hoặc đường chéo đã chọn. |
| [````TreeViewPlugin````](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/TreeViewPlugin/TreeViewPlugin.js~TreeViewPlugin.html)  | Triển khai các chế độ xem cây Objects, Classes và Storeys trong bảng khám phá. |
| [````SectionPlanesPlugin````](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/SectionPlanesPlugin/SectionPlanesPlugin.js~SectionPlanesPlugin.html) | Quản lý các mặt phẳng cắt tương tác, được sử dụng để cắt các đối tượng để hiển thị cấu trúc bên trong. |
| [````BCFViewpointsPlugin````](https://xeokit.github.io/xeokit-sdk/docs/class/src/plugins/BCFViewpointsPlugin/BCFViewpointsPlugin.js~BCFViewpointsPlugin.html) | Lưu và tải các điểm nhìn BCF. |
| [````ContextMenu````](https://xeokit.github.io/xeokit-sdk/docs/class/src/extras/ContextMenu/ContextMenu.js~ContextMenu.html)  | Triển khai các menu ngữ cảnh cho các chế độ xem cây khám phá và canvas 3D. |

# Xây dựng Trình xem

## Cài đặt từ NPM

Để cài đặt gói npm:

````
npm i @xeokit/xeokit-bim-viewer
````

## Xây dựng Tệp nhị phân

Chạy lệnh bên dưới để xây dựng mô-đun ES6 trong ````/dist/xeokit-bim-viewer.es.js````.

````
npm run build
````

## Xây dựng Tài liệu

Để xây dựng tài liệu API trong ````/docs/````:

````
npm run docs
````





