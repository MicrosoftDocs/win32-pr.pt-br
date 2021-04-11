---
description: A tabela MIME associa um tipo de conteúdo MIME com uma extensão de nome de arquivo ou um CLSID para gerar a extensão ou as informações do servidor COM necessárias para o anúncio do conteúdo MIME (Multipurpose Internet Mail Extensions).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabela MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170834"
---
# <a name="mime-table"></a><span data-ttu-id="64df5-103">Tabela MIME</span><span class="sxs-lookup"><span data-stu-id="64df5-103">MIME Table</span></span>

<span data-ttu-id="64df5-104">A tabela MIME associa um tipo de conteúdo MIME com uma extensão de nome de arquivo ou um CLSID para gerar a extensão ou as informações do servidor COM necessárias para o anúncio do conteúdo MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="64df5-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="64df5-105">A tabela MIME tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="64df5-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="64df5-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="64df5-106">Column</span></span>      | <span data-ttu-id="64df5-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="64df5-107">Type</span></span>             | <span data-ttu-id="64df5-108">Chave</span><span class="sxs-lookup"><span data-stu-id="64df5-108">Key</span></span> | <span data-ttu-id="64df5-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="64df5-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="64df5-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="64df5-110">ContentType</span></span> | [<span data-ttu-id="64df5-111">Text</span><span class="sxs-lookup"><span data-stu-id="64df5-111">Text</span></span>](text.md) | <span data-ttu-id="64df5-112">S</span><span class="sxs-lookup"><span data-stu-id="64df5-112">Y</span></span>   | <span data-ttu-id="64df5-113">N</span><span class="sxs-lookup"><span data-stu-id="64df5-113">N</span></span>        |
| <span data-ttu-id="64df5-114">Extensão\_</span><span class="sxs-lookup"><span data-stu-id="64df5-114">Extension\_</span></span> | [<span data-ttu-id="64df5-115">Text</span><span class="sxs-lookup"><span data-stu-id="64df5-115">Text</span></span>](text.md) | <span data-ttu-id="64df5-116">N</span><span class="sxs-lookup"><span data-stu-id="64df5-116">N</span></span>   | <span data-ttu-id="64df5-117">N</span><span class="sxs-lookup"><span data-stu-id="64df5-117">N</span></span>        |
| <span data-ttu-id="64df5-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="64df5-118">CLSID</span></span>       | [<span data-ttu-id="64df5-119">GUID</span><span class="sxs-lookup"><span data-stu-id="64df5-119">GUID</span></span>](guid.md) | <span data-ttu-id="64df5-120">N</span><span class="sxs-lookup"><span data-stu-id="64df5-120">N</span></span>   | <span data-ttu-id="64df5-121">S</span><span class="sxs-lookup"><span data-stu-id="64df5-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="64df5-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="64df5-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="64df5-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span><span class="sxs-lookup"><span data-stu-id="64df5-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="64df5-124">Esta coluna é um identificador para o conteúdo MIME.</span><span class="sxs-lookup"><span data-stu-id="64df5-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="64df5-125">Normalmente, ele é escrito na forma de tipo/formato.</span><span class="sxs-lookup"><span data-stu-id="64df5-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="64df5-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extensão\_</span><span class="sxs-lookup"><span data-stu-id="64df5-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="64df5-127">Esta coluna contém a extensão de servidor que deve ser associada ao conteúdo MIME, sem o ponto.</span><span class="sxs-lookup"><span data-stu-id="64df5-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="64df5-128">Esta coluna é uma chave estrangeira na [tabela de extensão](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="64df5-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="64df5-129">A tabela de extensão contém informações de servidor de extensão de nome de arquivo que são usadas como parte do anúncio.</span><span class="sxs-lookup"><span data-stu-id="64df5-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="64df5-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="64df5-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="64df5-131">Esta coluna contém o CLSID do servidor COM que deve ser associado ao conteúdo MIME.</span><span class="sxs-lookup"><span data-stu-id="64df5-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="64df5-132">O CLSID nesta coluna pode ser uma chave estrangeira na tabela de [classes](class-table.md) ou pode ser um CLSID que já existe na máquina do usuário.</span><span class="sxs-lookup"><span data-stu-id="64df5-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="64df5-133">A tabela de classes contém informações relacionadas ao servidor COM que são usadas como parte do anúncio.</span><span class="sxs-lookup"><span data-stu-id="64df5-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64df5-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="64df5-134">Remarks</span></span>

<span data-ttu-id="64df5-135">Essa tabela é referida quando a ação [RegisterMIMEInfo](registermimeinfo-action.md) ou a [ação UnregisterMIMEInfo](unregistermimeinfo-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="64df5-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="64df5-136">No modo de anúncio, a ação RegisterMIMEInfo registra todas as informações de MIME para servidores da tabela MIME para a qual o recurso correspondente está habilitado.</span><span class="sxs-lookup"><span data-stu-id="64df5-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="64df5-137">Caso contrário, a ação registrará informações de MIME para servidores da tabela MIME para as quais o recurso correspondente está selecionado no momento para ser instalado.</span><span class="sxs-lookup"><span data-stu-id="64df5-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="64df5-138">A [ação UnregisterMIMEInfo](unregistermimeinfo-action.md) cancela o registro das informações do registro relacionadas a MIME do sistema.</span><span class="sxs-lookup"><span data-stu-id="64df5-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="64df5-139">A ação cancela o registro de informações de MIME para servidores da tabela MIME para a qual o recurso correspondente está selecionado no momento para ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="64df5-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="64df5-140">Validação</span><span class="sxs-lookup"><span data-stu-id="64df5-140">Validation</span></span>

<dl>

[<span data-ttu-id="64df5-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="64df5-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="64df5-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="64df5-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="64df5-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="64df5-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="64df5-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="64df5-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



