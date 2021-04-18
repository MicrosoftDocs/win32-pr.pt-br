---
description: O título do item.
ms.assetid: 8fb948d6-2677-4e5d-b283-8757c3df574d
title: System.Title
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee57037a35c08fd3a6be4f4a0ce7a8475f82cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760598"
---
# <a name="systemtitle"></a><span data-ttu-id="67258-103">System.Title</span><span class="sxs-lookup"><span data-stu-id="67258-103">System.Title</span></span>

<span data-ttu-id="67258-104">O título do item.</span><span class="sxs-lookup"><span data-stu-id="67258-104">The title of the item.</span></span> <span data-ttu-id="67258-105">Por exemplo, o título de um documento, o assunto de uma mensagem, a legenda de uma fotografia ou o nome de uma música.</span><span class="sxs-lookup"><span data-stu-id="67258-105">For example, the title of a document, the subject of a message, the caption of a photo, or the name of a music track.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="67258-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67258-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Title
   shellPKey = PKEY_Title
   formatID = F29F85E0-4FF9-1068-AB91-08002B27B3D9
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
```

## <a name="remarks"></a><span data-ttu-id="67258-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="67258-107">Remarks</span></span>

<span data-ttu-id="67258-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="67258-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="67258-109">Essa propriedade é mapeada para o *título* da Propriedade do documento OLE.</span><span class="sxs-lookup"><span data-stu-id="67258-109">This property maps to the OLE document property *Title*.</span></span> <span data-ttu-id="67258-110">[System. title]() é uma propriedade comumente usada, especialmente em listas heterogêneas de itens em que os itens podem ser de muitos tipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="67258-110">[System.Title]() is a commonly used property, particularly in heterogeneous lists of items where the items can be of many different types.</span></span> <span data-ttu-id="67258-111">Portanto, é recomendável que os manipuladores de propriedade populem essa propriedade mesmo se ela for redundante; por exemplo, um email, que preencheria System. Title e [System. Subject](./props-system-subject.md) com o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="67258-111">Therefore, it is recommended that property handlers populate this property even if it is redundant; for example, an e-mail, which would populate both System.Title and [System.Subject](./props-system-subject.md) with the same value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67258-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67258-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67258-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="67258-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="67258-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="67258-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="67258-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="67258-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="67258-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="67258-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="67258-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="67258-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="67258-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="67258-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="67258-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="67258-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="67258-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="67258-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="67258-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="67258-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="67258-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="67258-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="67258-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="67258-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="67258-124">editControl</span><span class="sxs-lookup"><span data-stu-id="67258-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="67258-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="67258-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="67258-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="67258-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
