---
description: Identifica a extensão de arquivo do item baseado em arquivo, incluindo o período à esquerda.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755706"
---
# <a name="systemfileextension"></a><span data-ttu-id="36ded-103">System. FileExtension</span><span class="sxs-lookup"><span data-stu-id="36ded-103">System.FileExtension</span></span>

<span data-ttu-id="36ded-104">Identifica a extensão de arquivo do item baseado em arquivo, incluindo o período à esquerda.</span><span class="sxs-lookup"><span data-stu-id="36ded-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="36ded-105">Essa propriedade é derivada de System. FileName.</span><span class="sxs-lookup"><span data-stu-id="36ded-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="36ded-106">Se System. FileName não tiver uma extensão de arquivo ou for VT \_ Empty, o valor dessa propriedade deverá ser VT \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="36ded-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="36ded-107">Para obter o tipo de qualquer item (incluindo um item que não é um arquivo), use System. ItemType.</span><span class="sxs-lookup"><span data-stu-id="36ded-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="36ded-108">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36ded-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="36ded-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="36ded-109">Remarks</span></span>

<span data-ttu-id="36ded-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="36ded-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="36ded-111">Se [System. FileName](./props-system-filename.md) for VT \_ vazio, essa propriedade também deverá estar vazia.</span><span class="sxs-lookup"><span data-stu-id="36ded-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="36ded-112">Caso contrário, essa propriedade deve ser derivada adequadamente pela fonte de dados de System. FileName.</span><span class="sxs-lookup"><span data-stu-id="36ded-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="36ded-113">Se System. FileName não incluir uma extensão de arquivo, [System. FileExtension]() deverá ser VT \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="36ded-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="36ded-114">Para obter o tipo de qualquer item (incluindo um item que não é um arquivo), use [System. ItemType](./props-system-itemtype.md).</span><span class="sxs-lookup"><span data-stu-id="36ded-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="36ded-115">Exemplos de propriedade de extensão de arquivo e caminho.</span><span class="sxs-lookup"><span data-stu-id="36ded-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="36ded-116">Caminho</span><span class="sxs-lookup"><span data-stu-id="36ded-116">Path</span></span>                               | <span data-ttu-id="36ded-117">Extensão do arquivo</span><span class="sxs-lookup"><span data-stu-id="36ded-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="36ded-118">c: \\ arquivos \\ \\hello.txt pessoais</span><span class="sxs-lookup"><span data-stu-id="36ded-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="36ded-119">.txt</span><span class="sxs-lookup"><span data-stu-id="36ded-119">.txt</span></span>           |
| <span data-ttu-id="36ded-120">\\\\mydir de compartilhamento de servidor \\ \\ \\news.doc</span><span class="sxs-lookup"><span data-stu-id="36ded-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="36ded-121">.doc</span><span class="sxs-lookup"><span data-stu-id="36ded-121">.doc</span></span>           |
| <span data-ttu-id="36ded-122">\\\\\\numbers.xls de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="36ded-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="36ded-123">.xls</span><span class="sxs-lookup"><span data-stu-id="36ded-123">.xls</span></span>           |
| <span data-ttu-id="36ded-124">\\\\\\pasta de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="36ded-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="36ded-125">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="36ded-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="36ded-126">c: \\ itens \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="36ded-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="36ded-127">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="36ded-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="36ded-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="36ded-128">\[desktop\]</span></span>                        | <span data-ttu-id="36ded-129">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="36ded-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="36ded-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="36ded-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36ded-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="36ded-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="36ded-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="36ded-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="36ded-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="36ded-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="36ded-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="36ded-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="36ded-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="36ded-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="36ded-136">stringFormat</span><span class="sxs-lookup"><span data-stu-id="36ded-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="36ded-137">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="36ded-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="36ded-138">numberFormat</span><span class="sxs-lookup"><span data-stu-id="36ded-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="36ded-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="36ded-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="36ded-140">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="36ded-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="36ded-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="36ded-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="36ded-142">editControl</span><span class="sxs-lookup"><span data-stu-id="36ded-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="36ded-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="36ded-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="36ded-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="36ded-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
