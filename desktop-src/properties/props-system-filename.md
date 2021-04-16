---
description: O nome do arquivo, incluindo sua extensão.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779329"
---
# <a name="systemfilename"></a><span data-ttu-id="bb4a7-103">System. FileName</span><span class="sxs-lookup"><span data-stu-id="bb4a7-103">System.FileName</span></span>

<span data-ttu-id="bb4a7-104">O nome do arquivo, incluindo sua extensão.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-104">The file name, including its extension.</span></span> <span data-ttu-id="bb4a7-105">System. FileExtension é derivado dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-105">System.FileExtension is derived from this property.</span></span>

<span data-ttu-id="bb4a7-106">É possível que o item não exista em um sistema de arquivos (ou seja, ele não pode ser aberto usando CreateFile).</span><span class="sxs-lookup"><span data-stu-id="bb4a7-106">It is possible that the item might not exist on a filesystem (that is, it may not be opened using CreateFile).</span></span> <span data-ttu-id="bb4a7-107">No entanto, se o item for representado como um arquivo e seu nome seguir a sintaxe padrão de nomenclatura de arquivo do Win32, a fonte de dados deverá emitir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-107">Nonetheless, if the item is represented as a file and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="bb4a7-108">Se o item não for um arquivo, a fonte de dados deverá emitir essa propriedade como VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-108">If the item is not a file, then the data source should emit this property as VT\_EMPTY.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="bb4a7-109">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb4a7-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="bb4a7-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb4a7-110">Windows Vista</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a><span data-ttu-id="bb4a7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb4a7-111">Remarks</span></span>

<span data-ttu-id="bb4a7-112">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-112">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="bb4a7-113">Talvez o item não exista em um sistema de arquivos (ou seja, ele não pode ser aberto usando CreateFile), mas se o item for representado como um arquivo do sensor lógico e seu nome seguir a sintaxe de nomeação de arquivo Win32 padrão, a fonte de dados deverá emitir essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-113">The item might not exist on a filesystem (that is, it may not be opened using CreateFile), but if the item is represented as a file from the logical sense and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="bb4a7-114">Se um item não for um arquivo, o valor dessa propriedade será VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-114">If an item is not a file, then the value for this property is VT\_EMPTY.</span></span> <span data-ttu-id="bb4a7-115">Consulte System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-115">See System.ItemNameDisplay.</span></span> <span data-ttu-id="bb4a7-116">Isso tem o mesmo valor que System. ParsingName para itens que são fornecidos pela pasta de arquivos do Shell.</span><span class="sxs-lookup"><span data-stu-id="bb4a7-116">This has the same value as System.ParsingName for items that are provided by the Shell's file folder.</span></span>

<span data-ttu-id="bb4a7-117">A tabela a seguir lista exemplos de valores de propriedade Path e filename:</span><span class="sxs-lookup"><span data-stu-id="bb4a7-117">The following table lists examples of path and filename property values:</span></span>



| <span data-ttu-id="bb4a7-118">Caminho</span><span class="sxs-lookup"><span data-stu-id="bb4a7-118">Path</span></span>                               | <span data-ttu-id="bb4a7-119">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bb4a7-119">Property Value</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="bb4a7-120">c: \\ arquivos \\ \\hello.txt pessoais</span><span class="sxs-lookup"><span data-stu-id="bb4a7-120">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="bb4a7-121">olá.txt</span><span class="sxs-lookup"><span data-stu-id="bb4a7-121">hello.txt</span></span>      |
| <span data-ttu-id="bb4a7-122">\\\\mydir de compartilhamento de servidor \\ \\ \\news.doc</span><span class="sxs-lookup"><span data-stu-id="bb4a7-122">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="bb4a7-123">news.doc</span><span class="sxs-lookup"><span data-stu-id="bb4a7-123">news.doc</span></span>       |
| <span data-ttu-id="bb4a7-124">\\\\\\numbers.xls de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="bb4a7-124">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="bb4a7-125">numbers.xls</span><span class="sxs-lookup"><span data-stu-id="bb4a7-125">numbers.xls</span></span>    |
| <span data-ttu-id="bb4a7-126">c: \\ itens \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="bb4a7-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="bb4a7-127">MyFolder</span><span class="sxs-lookup"><span data-stu-id="bb4a7-127">MyFolder</span></span>       |
| <span data-ttu-id="bb4a7-128">\[mensagem de email\]</span><span class="sxs-lookup"><span data-stu-id="bb4a7-128">\[email message\]</span></span>                  | <span data-ttu-id="bb4a7-129">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="bb4a7-129">VT\_EMPTY</span></span>      |
| <span data-ttu-id="bb4a7-130">\[Song. WMA no dispositivo portátil\]</span><span class="sxs-lookup"><span data-stu-id="bb4a7-130">\[song.wma on portable device\]</span></span>    | <span data-ttu-id="bb4a7-131">Song. WMA</span><span class="sxs-lookup"><span data-stu-id="bb4a7-131">song.wma</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="bb4a7-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb4a7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb4a7-133">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="bb4a7-133">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-134">searchInfo</span><span class="sxs-lookup"><span data-stu-id="bb4a7-134">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-135">labelInfo</span><span class="sxs-lookup"><span data-stu-id="bb4a7-135">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-136">typeInfo</span><span class="sxs-lookup"><span data-stu-id="bb4a7-136">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-137">displayInfo</span><span class="sxs-lookup"><span data-stu-id="bb4a7-137">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="bb4a7-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="bb4a7-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="bb4a7-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bb4a7-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="bb4a7-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-143">drawControl</span><span class="sxs-lookup"><span data-stu-id="bb4a7-143">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-144">editControl</span><span class="sxs-lookup"><span data-stu-id="bb4a7-144">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-145">filterControl</span><span class="sxs-lookup"><span data-stu-id="bb4a7-145">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="bb4a7-146">queryControl</span><span class="sxs-lookup"><span data-stu-id="bb4a7-146">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
