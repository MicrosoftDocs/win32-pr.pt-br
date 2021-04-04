---
description: O nome de exibição no &\# 0034; mais completo&\# 0034; Form.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647552"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="d8f4b-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="d8f4b-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="d8f4b-104">O nome de exibição no formulário "mais completo".</span><span class="sxs-lookup"><span data-stu-id="d8f4b-104">The display name in "most complete" form.</span></span> <span data-ttu-id="d8f4b-105">É a representação exclusiva do nome do item mais apropriada para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="d8f4b-106">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8f4b-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="d8f4b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8f4b-107">Remarks</span></span>

<span data-ttu-id="d8f4b-108">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="d8f4b-109">Esse valor é o concatentation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="d8f4b-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="d8f4b-110">Se o item for um arquivo, essa propriedade incluirá o nome de exibição, conforme mostrado no explorador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="d8f4b-111">Há casos aceitáveis quando [System. FileName](./props-system-filename.md) é fornecido, mas o valor dessa propriedade é completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="d8f4b-112">As mensagens de email são um bom exemplo.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-112">E-mail messages are a good example.</span></span> <span data-ttu-id="d8f4b-113">Se o item for uma mensagem de email, o nome do item normalmente será o assunto.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="d8f4b-114">Nesse caso, o valor deve ser a concatenação de [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="d8f4b-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="d8f4b-115">Como o valor de System. ItemNamePrefix exclui espaços à direita, a concatenação deve incluir um espaço ao gerar [System. ItemNameDisplay]().</span><span class="sxs-lookup"><span data-stu-id="d8f4b-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="d8f4b-116">Observe que essa propriedade não tem garantia de ser exclusiva, mas foi projetada para promover o candidato mais provável que pode ser exclusivo e também faz sentido para os usuários finais.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="d8f4b-117">Por exemplo, para documentos, o [System. title](./props-system-title.md) pode ser usado como [System. ItemNameDisplay](), mas na prática o título dos documentos pode não ser útil ou exclusivo o suficiente para funcionar como o único System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="d8f4b-118">Em vez disso, fornecer [System. FileName](./props-system-filename.md) como o valor de System. ItemNameDisplay é uma opção melhor.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="d8f4b-119">No Windows Mail, o email é armazenado no sistema de arquivos como arquivos. eml.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="d8f4b-120">Os valores de System. FileName para esses arquivos não são amigáveis para o homem, pois são GUIDs.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="d8f4b-121">Neste exemplo, promover [System. Subject](./props-system-subject.md) como System. ItemNameDisplay faz mais sentido.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="d8f4b-122">**Notas de compatibilidade:**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="d8f4b-123">Implementações de pastas do Shell no Windows Vista: Use PKEY \_ ItemNameDisplay para a coluna nome quando desejar que o Windows Explorer chame [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ normal) para obter o valor do nome.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="d8f4b-124">Use outro PKEY, como PKEY \_ ItemName, quando você quiser que o Windows Explorer chame o repositório de propriedades da pasta ou [**IShellFolder2:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) para obter o valor do nome.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="d8f4b-125">Implementações de pastas do Shell no Windows XP: a primeira coluna deve ser a coluna Name e o Windows Explorer chama [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para obter o valor do nome.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="d8f4b-126">O PKEY/SCID não importa.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="d8f4b-127">Tipo de item</span><span class="sxs-lookup"><span data-stu-id="d8f4b-127">Item type</span></span>     | <span data-ttu-id="d8f4b-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="d8f4b-129">Arquivo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-129">File</span></span>          | <span data-ttu-id="d8f4b-130">olá.txt</span><span class="sxs-lookup"><span data-stu-id="d8f4b-130">hello.txt</span></span>                 |
| <span data-ttu-id="d8f4b-131">Mensagem</span><span class="sxs-lookup"><span data-stu-id="d8f4b-131">Message</span></span>       | <span data-ttu-id="d8f4b-132">Re: onde está a reunião?</span><span class="sxs-lookup"><span data-stu-id="d8f4b-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="d8f4b-133">Pasta do dispositivo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-133">Device folder</span></span> | <span data-ttu-id="d8f4b-134">Song. WMA</span><span class="sxs-lookup"><span data-stu-id="d8f4b-134">song.wma</span></span>                  |
| <span data-ttu-id="d8f4b-135">Pasta</span><span class="sxs-lookup"><span data-stu-id="d8f4b-135">Folder</span></span>        | <span data-ttu-id="d8f4b-136">Documentos</span><span class="sxs-lookup"><span data-stu-id="d8f4b-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="d8f4b-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8f4b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8f4b-138">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="d8f4b-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-139">searchInfo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-140">labelInfo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-141">typeInfo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-142">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d8f4b-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-143">stringFormat</span><span class="sxs-lookup"><span data-stu-id="d8f4b-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-144">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="d8f4b-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-145">numberFormat</span><span class="sxs-lookup"><span data-stu-id="d8f4b-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d8f4b-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-147">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="d8f4b-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-148">drawControl</span><span class="sxs-lookup"><span data-stu-id="d8f4b-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-149">editControl</span><span class="sxs-lookup"><span data-stu-id="d8f4b-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-150">filterControl</span><span class="sxs-lookup"><span data-stu-id="d8f4b-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="d8f4b-151">queryControl</span><span class="sxs-lookup"><span data-stu-id="d8f4b-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
