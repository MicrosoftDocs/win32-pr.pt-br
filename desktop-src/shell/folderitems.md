---
description: Representa a coleção de itens em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.
title: Objeto FolderItems (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 6f9a6fa978c64c788cbd224cf3a39454c644a57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646563"
---
# <a name="folderitems-object"></a><span data-ttu-id="68eb1-104">Objeto FolderItems</span><span class="sxs-lookup"><span data-stu-id="68eb1-104">FolderItems object</span></span>

<span data-ttu-id="68eb1-105">Representa a coleção de itens em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="68eb1-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="68eb1-106">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="68eb1-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="68eb1-107">Membros</span><span class="sxs-lookup"><span data-stu-id="68eb1-107">Members</span></span>

<span data-ttu-id="68eb1-108">O objeto **FolderItems** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68eb1-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="68eb1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="68eb1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="68eb1-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68eb1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68eb1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="68eb1-111">Methods</span></span>

<span data-ttu-id="68eb1-112">O objeto **FolderItems** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="68eb1-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="68eb1-113">Método</span><span class="sxs-lookup"><span data-stu-id="68eb1-113">Method</span></span>                                    | <span data-ttu-id="68eb1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="68eb1-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68eb1-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="68eb1-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="68eb1-116">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="68eb1-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="68eb1-117">**Item**</span><span class="sxs-lookup"><span data-stu-id="68eb1-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="68eb1-118">Recupera o objeto [**FolderItem**](folderitem.md) para um item especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="68eb1-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68eb1-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68eb1-119">Properties</span></span>

<span data-ttu-id="68eb1-120">O objeto **FolderItems** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="68eb1-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="68eb1-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="68eb1-121">Property</span></span>                                                  | <span data-ttu-id="68eb1-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="68eb1-122">Access type</span></span>          | <span data-ttu-id="68eb1-123">Description</span><span class="sxs-lookup"><span data-stu-id="68eb1-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68eb1-124">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="68eb1-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="68eb1-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68eb1-125">Read-only</span></span><br/> | <span data-ttu-id="68eb1-126">Contém o objeto de [**aplicativo**](folderitems-application.md) da coleção de itens de pasta.</span><span class="sxs-lookup"><span data-stu-id="68eb1-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="68eb1-127">**Contar**</span><span class="sxs-lookup"><span data-stu-id="68eb1-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="68eb1-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68eb1-128">Read-only</span></span><br/> | <span data-ttu-id="68eb1-129">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="68eb1-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="68eb1-130">**Pai**</span><span class="sxs-lookup"><span data-stu-id="68eb1-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="68eb1-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68eb1-131">Read-only</span></span><br/> | <span data-ttu-id="68eb1-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="68eb1-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="68eb1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68eb1-133">Requirements</span></span>



| <span data-ttu-id="68eb1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="68eb1-134">Requirement</span></span> | <span data-ttu-id="68eb1-135">Valor</span><span class="sxs-lookup"><span data-stu-id="68eb1-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68eb1-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68eb1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="68eb1-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="68eb1-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="68eb1-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68eb1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="68eb1-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="68eb1-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="68eb1-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="68eb1-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="68eb1-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68eb1-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="68eb1-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="68eb1-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68eb1-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68eb1-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="68eb1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="68eb1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68eb1-145"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="68eb1-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




