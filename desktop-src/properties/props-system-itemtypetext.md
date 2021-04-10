---
description: O nome de tipo amigável do item.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169267"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="91740-103">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="91740-103">System.ItemTypeText</span></span>

<span data-ttu-id="91740-104">O nome de tipo amigável do item.</span><span class="sxs-lookup"><span data-stu-id="91740-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="91740-105">Esse valor não se destina a ser analisado programaticamente.</span><span class="sxs-lookup"><span data-stu-id="91740-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="91740-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91740-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="91740-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="91740-107">Remarks</span></span>

<span data-ttu-id="91740-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="91740-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="91740-109">Se [System. ItemType](./props-system-itemtype.md) for VT \_ vazio, o valor dessa propriedade também será um VT \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="91740-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="91740-110">Se o item for um arquivo, o valor dessa propriedade será o mesmo que se você passasse o valor System. ItemType do arquivo para [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span><span class="sxs-lookup"><span data-stu-id="91740-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="91740-111">Essa propriedade não deve ser confundida com [System. Kind](./props-system-kind.md), que é um nome de tipo amigável de alto nível.</span><span class="sxs-lookup"><span data-stu-id="91740-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="91740-112">Por exemplo, para um arquivo de documento. doc, as várias propriedades são como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="91740-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="91740-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="91740-113">Property</span></span>                                               | <span data-ttu-id="91740-114">Valor</span><span class="sxs-lookup"><span data-stu-id="91740-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="91740-115">Sistema. Kind</span><span class="sxs-lookup"><span data-stu-id="91740-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="91740-116">Documento</span><span class="sxs-lookup"><span data-stu-id="91740-116">Document</span></span>                |
| [<span data-ttu-id="91740-117">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="91740-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="91740-118">.doc</span><span class="sxs-lookup"><span data-stu-id="91740-118">.doc</span></span>                    |
| [<span data-ttu-id="91740-119">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="91740-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="91740-120">Documento do Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="91740-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="91740-121">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="91740-121">Example values:</span></span>



| <span data-ttu-id="91740-122">Caminho</span><span class="sxs-lookup"><span data-stu-id="91740-122">Path</span></span>                                   | <span data-ttu-id="91740-123">ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="91740-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="91740-124">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="91740-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="91740-125">Arquivo de texto</span><span class="sxs-lookup"><span data-stu-id="91740-125">Text File</span></span>               |
| <span data-ttu-id="91740-126">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="91740-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="91740-127">Documento do Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="91740-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="91740-128">\\\\\\pasta de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="91740-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="91740-129">Pasta de arquivos</span><span class="sxs-lookup"><span data-stu-id="91740-129">File Folder</span></span>             |
| <span data-ttu-id="91740-130">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="91740-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="91740-131">Pasta de arquivos</span><span class="sxs-lookup"><span data-stu-id="91740-131">File Folder</span></span>             |
| <span data-ttu-id="91740-132">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="91740-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="91740-133">Mensagem de email do Outlook</span><span class="sxs-lookup"><span data-stu-id="91740-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="91740-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91740-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91740-135">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="91740-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="91740-136">searchInfo</span><span class="sxs-lookup"><span data-stu-id="91740-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="91740-137">labelInfo</span><span class="sxs-lookup"><span data-stu-id="91740-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="91740-138">typeInfo</span><span class="sxs-lookup"><span data-stu-id="91740-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="91740-139">displayInfo</span><span class="sxs-lookup"><span data-stu-id="91740-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="91740-140">stringFormat</span><span class="sxs-lookup"><span data-stu-id="91740-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="91740-141">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="91740-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="91740-142">numberFormat</span><span class="sxs-lookup"><span data-stu-id="91740-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="91740-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="91740-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="91740-144">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="91740-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="91740-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="91740-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="91740-146">editControl</span><span class="sxs-lookup"><span data-stu-id="91740-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="91740-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="91740-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="91740-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="91740-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
