---
description: Representa a coleção de itens em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.
title: Objeto FolderItems (Shldisp.h)
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
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840647"
---
# <a name="folderitems-object"></a><span data-ttu-id="5f3e7-104">Objeto FolderItems</span><span class="sxs-lookup"><span data-stu-id="5f3e7-104">FolderItems object</span></span>

<span data-ttu-id="5f3e7-105">Representa a coleção de itens em uma pasta shell.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="5f3e7-106">Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="5f3e7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5f3e7-107">Members</span></span>

<span data-ttu-id="5f3e7-108">O **objeto FolderItems** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5f3e7-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="5f3e7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f3e7-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5f3e7-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f3e7-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5f3e7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5f3e7-111">Methods</span></span>

<span data-ttu-id="5f3e7-112">O **objeto FolderItems** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="5f3e7-113">Método</span><span class="sxs-lookup"><span data-stu-id="5f3e7-113">Method</span></span>                                    | <span data-ttu-id="5f3e7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f3e7-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f3e7-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="5f3e7-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="5f3e7-116">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="5f3e7-117">**Item**</span><span class="sxs-lookup"><span data-stu-id="5f3e7-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="5f3e7-118">Recupera o [**objeto FolderItem**](folderitem.md) para um item especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5f3e7-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5f3e7-119">Properties</span></span>

<span data-ttu-id="5f3e7-120">O **objeto FolderItems** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="5f3e7-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5f3e7-121">Property</span></span>                                                  | <span data-ttu-id="5f3e7-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="5f3e7-122">Access type</span></span>          | <span data-ttu-id="5f3e7-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f3e7-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f3e7-124">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="5f3e7-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="5f3e7-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f3e7-125">Read-only</span></span><br/> | <span data-ttu-id="5f3e7-126">Contém o [**objeto Application**](folderitems-application.md) da coleção de itens de pasta.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="5f3e7-127">**Contagem**</span><span class="sxs-lookup"><span data-stu-id="5f3e7-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="5f3e7-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f3e7-128">Read-only</span></span><br/> | <span data-ttu-id="5f3e7-129">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="5f3e7-130">**Pai**</span><span class="sxs-lookup"><span data-stu-id="5f3e7-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="5f3e7-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5f3e7-131">Read-only</span></span><br/> | <span data-ttu-id="5f3e7-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="5f3e7-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="5f3e7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f3e7-133">Requirements</span></span>



| <span data-ttu-id="5f3e7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f3e7-134">Requirement</span></span> | <span data-ttu-id="5f3e7-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5f3e7-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f3e7-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f3e7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5f3e7-137">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5f3e7-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5f3e7-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f3e7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5f3e7-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5f3e7-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5f3e7-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5f3e7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f3e7-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5f3e7-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5f3e7-142">Idl</span><span class="sxs-lookup"><span data-stu-id="5f3e7-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f3e7-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f3e7-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5f3e7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5f3e7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f3e7-145"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5f3e7-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




