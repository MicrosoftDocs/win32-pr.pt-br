---
description: A orientação da foto quando ela foi realizada, conforme especificado nas informações de EXIF (arquivo de imagem intercambiável) e em termos de linhas e colunas.
ms.assetid: d6186248-8944-4bd6-8f04-bab5ea15b169
title: System. Photo. Orientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac8cec8e199bd8eff52a92c7518a998d805d18d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789608"
---
# <a name="systemphotoorientation"></a><span data-ttu-id="de2d6-103">System. Photo. Orientation</span><span class="sxs-lookup"><span data-stu-id="de2d6-103">System.Photo.Orientation</span></span>

<span data-ttu-id="de2d6-104">A orientação da foto quando ela foi realizada, conforme especificado nas informações de EXIF (arquivo de imagem intercambiável) e em termos de linhas e colunas.</span><span class="sxs-lookup"><span data-stu-id="de2d6-104">The orientation of the photo when it was taken, as specified in the Exchangeable Image File (EXIF) information and in terms of rows and columns.</span></span> <span data-ttu-id="de2d6-105">Isso permite que os aplicativos e o Shell orientem a imagem corretamente, em vez de orientar os pixels e persistir a imagem na orientação de exibição solicitada, o que pode resultar em uma perda de fidelidade.</span><span class="sxs-lookup"><span data-stu-id="de2d6-105">This allows applications and the Shell to properly orient the image, instead of orienting the pixels and persisting the image in the requested display orientation, which can result in a loss of fidelity.</span></span> <span data-ttu-id="de2d6-106">Essa propriedade não deve ser exibida na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="de2d6-106">This property is not meant to be displayed in the UI.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="de2d6-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="de2d6-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 1
            text = Normal
            defineToken = PHOTO_ORIENTATION_NORMAL
         enum
            name = FlipHorizontal
            value = 2
            text = Flip horizontal
            defineToken = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            name = Rotate180
            value = 3
            text = Rotate 180 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE180
         enum
            name = FlipVertical
            value = 4
            text = Flip vertical
            defineToken = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            name = Transpose
            value = 5
            text = Transpose
            defineToken = PHOTO_ORIENTATION_TRANSPOSE
         enum
            name = Rotate270
            value = 6
            text = Rotate 270 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE270
         enum
            name = Transverse
            value = 7
            text = Transverse
            defineToken = PHOTO_ORIENTATION_TRANSVERSE
         enum
            name = Rotate90
            value = 8
            text = Rotate 90 degrees
            defineToken = PHOTO_ORIENTATION_ROTATE90
```

## <a name="windows-vista"></a><span data-ttu-id="de2d6-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de2d6-108">Windows Vista</span></span>

```
propertyDescription
   name = System.Photo.Orientation
   shellPKey = PKEY_Photo_Orientation
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 274
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Normal
            defineName = PHOTO_ORIENTATION_NORMAL
         enum
            value = 2
            text = Flip horizontal
            defineName = PHOTO_ORIENTATION_FLIPHORIZONTAL
         enum
            value = 3
            text = Rotate 180 degrees
            defineName = PHOTO_ORIENTATION_ROTATE180
         enum
            value = 4
            text = Flip vertical
            defineName = PHOTO_ORIENTATION_FLIPVERTICAL
         enum
            value = 5
            text = Transpose
            defineName = PHOTO_ORIENTATION_TRANSPOSE
         enum
            value = 6
            text = Rotate 270 degrees
            defineName = PHOTO_ORIENTATION_ROTATE270
         enum
            value = 7
            text = Transverse
            defineName = PHOTO_ORIENTATION_TRANSVERSE
         enum
            value = 8
            text = Rotate 90 degrees
            defineName = PHOTO_ORIENTATION_ROTATE90
```

## <a name="remarks"></a><span data-ttu-id="de2d6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="de2d6-109">Remarks</span></span>

<span data-ttu-id="de2d6-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="de2d6-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de2d6-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de2d6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de2d6-112">Formato de arquivo de imagem intercambiável para câmeras digitais ainda: Exif versão 2,2</span><span class="sxs-lookup"><span data-stu-id="de2d6-112">Exchangeable Image File Format for Digital Still Cameras: Exif Version 2.2</span></span>](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

[<span data-ttu-id="de2d6-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="de2d6-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="de2d6-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="de2d6-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="de2d6-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="de2d6-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="de2d6-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="de2d6-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="de2d6-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="de2d6-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="de2d6-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="de2d6-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="de2d6-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="de2d6-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="de2d6-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="de2d6-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="de2d6-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="de2d6-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="de2d6-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="de2d6-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="de2d6-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="de2d6-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="de2d6-124">editControl</span><span class="sxs-lookup"><span data-stu-id="de2d6-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="de2d6-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="de2d6-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="de2d6-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="de2d6-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
