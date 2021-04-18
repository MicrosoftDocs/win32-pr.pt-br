---
description: A ID de arquivo exclusiva, também conhecida como o número de referência do arquivo.
ms.assetid: 65189671-1b55-4933-9dee-a120b38caa98
title: System. FileFRN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aa536e0cdda3f42fd9e03315156716ef499c5f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756286"
---
# <a name="systemfilefrn"></a><span data-ttu-id="6df17-103">System. FileFRN</span><span class="sxs-lookup"><span data-stu-id="6df17-103">System.FileFRN</span></span>

<span data-ttu-id="6df17-104">A ID de arquivo exclusiva, também conhecida como o número de referência do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6df17-104">The unique file ID, also known as the File Reference Number.</span></span> <span data-ttu-id="6df17-105">Para um determinado arquivo, esse é o mesmo valor que o membro **FileID** da ID do arquivo da estrutura de [**\_ \_ \_ \_ informações de dir**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) , que é obtida por uma chamada para [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span><span class="sxs-lookup"><span data-stu-id="6df17-105">For a given file, this is the same value as the **FileId** member of the [**FILE\_ID\_BOTH\_DIR\_INFO**](/windows/win32/api/winbase/ns-winbase-file_id_both_dir_info) structure, which is obtained by a call to [**GetFileInformationByHandleEx**](/windows/win32/api/winbase/nf-winbase-getfileinformationbyhandleex).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="6df17-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6df17-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileFRN
   shellPKey = PKEY_FileFRN
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 21
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6df17-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6df17-107">Remarks</span></span>

<span data-ttu-id="6df17-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6df17-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6df17-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6df17-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6df17-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6df17-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6df17-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6df17-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6df17-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6df17-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6df17-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="6df17-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6df17-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6df17-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6df17-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6df17-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6df17-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6df17-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6df17-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="6df17-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6df17-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6df17-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6df17-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6df17-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6df17-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="6df17-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6df17-121">editControl</span><span class="sxs-lookup"><span data-stu-id="6df17-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6df17-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="6df17-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6df17-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="6df17-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
