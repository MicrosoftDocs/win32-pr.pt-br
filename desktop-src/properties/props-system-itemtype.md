---
description: O tipo canônico do item.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171564"
---
# <a name="systemitemtype"></a><span data-ttu-id="923f6-103">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="923f6-103">System.ItemType</span></span>

<span data-ttu-id="923f6-104">O tipo canônico do item.</span><span class="sxs-lookup"><span data-stu-id="923f6-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="923f6-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="923f6-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="923f6-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="923f6-106">Remarks</span></span>

<span data-ttu-id="923f6-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="923f6-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="923f6-108">O valor de System. ItemType deve ser analisado programaticamente e pode ser:</span><span class="sxs-lookup"><span data-stu-id="923f6-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="923f6-109">Uma extensão de arquivo que aponta para um valor de ProgID ( \_ raiz de classes hKey) que \_ \\ <ProgID> mantém o nome de exibição do tipo.</span><span class="sxs-lookup"><span data-stu-id="923f6-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="923f6-110">Um valor ProgID (HKEY \_ classes \_ RROOT \\ <ProgID> ), que contém o nome de exibição do tipo.</span><span class="sxs-lookup"><span data-stu-id="923f6-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="923f6-111">O elemento FriendlyTypeName de um ProgID deve ser uma versão localizada do nome do aplicativo ( @winword.dll ,-42), enquanto o valor padrão da chave ProgID é um nome não localizado (Word.Document. 12).</span><span class="sxs-lookup"><span data-stu-id="923f6-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="923f6-112">Se não houver nenhum tipo canônico, o valor será VT \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="923f6-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="923f6-113">Se o item for um arquivo ([System. FileName](./props-system-filename.md) não for VT \_ Empty), o valor será o mesmo que [System. FileExtension](./props-system-fileextension.md).</span><span class="sxs-lookup"><span data-stu-id="923f6-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="923f6-114">Use [System. ItemTypeText](./props-system-itemtypetext.md) quando desejar exibir o tipo para usuários finais em uma exibição.</span><span class="sxs-lookup"><span data-stu-id="923f6-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="923f6-115">Se o item for um arquivo, passar o valor de [System. ItemType]() para [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) resultará no mesmo valor que [System. ItemTypeText](./props-system-itemtypetext.md).</span><span class="sxs-lookup"><span data-stu-id="923f6-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="923f6-116">Valores de exemplo:</span><span class="sxs-lookup"><span data-stu-id="923f6-116">Example values:</span></span>



| <span data-ttu-id="923f6-117">Caminho</span><span class="sxs-lookup"><span data-stu-id="923f6-117">Path</span></span>                                   | <span data-ttu-id="923f6-118">ItemType</span><span class="sxs-lookup"><span data-stu-id="923f6-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="923f6-119">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="923f6-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="923f6-120">.txt</span><span class="sxs-lookup"><span data-stu-id="923f6-120">.txt</span></span>             |
| <span data-ttu-id="923f6-121">\\\\mydir de compartilhamento de servidor \\ \\ \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="923f6-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="923f6-122">.doc</span><span class="sxs-lookup"><span data-stu-id="923f6-122">.doc</span></span>             |
| <span data-ttu-id="923f6-123">\\\\\\pasta de compartilhamento do servidor \\</span><span class="sxs-lookup"><span data-stu-id="923f6-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="923f6-124">Diretório</span><span class="sxs-lookup"><span data-stu-id="923f6-124">Directory</span></span>        |
| <span data-ttu-id="923f6-125">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="923f6-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="923f6-126">Diretório</span><span class="sxs-lookup"><span data-stu-id="923f6-126">Directory</span></span>        |
| <span data-ttu-id="923f6-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="923f6-127">\[desktop\]</span></span>                            | <span data-ttu-id="923f6-128">Pasta</span><span class="sxs-lookup"><span data-stu-id="923f6-128">Folder</span></span>           |
| <span data-ttu-id="923f6-129">/Mailbox conta/caixa de entrada/' re: Olá! '</span><span class="sxs-lookup"><span data-stu-id="923f6-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="923f6-130">MAPI/IPM. Mensagem</span><span class="sxs-lookup"><span data-stu-id="923f6-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="923f6-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="923f6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="923f6-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="923f6-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="923f6-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="923f6-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="923f6-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="923f6-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="923f6-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="923f6-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="923f6-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="923f6-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="923f6-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="923f6-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="923f6-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="923f6-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="923f6-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="923f6-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="923f6-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="923f6-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="923f6-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="923f6-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="923f6-142">drawControl</span><span class="sxs-lookup"><span data-stu-id="923f6-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="923f6-143">editControl</span><span class="sxs-lookup"><span data-stu-id="923f6-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="923f6-144">filterControl</span><span class="sxs-lookup"><span data-stu-id="923f6-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="923f6-145">queryControl</span><span class="sxs-lookup"><span data-stu-id="923f6-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="923f6-146">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="923f6-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
