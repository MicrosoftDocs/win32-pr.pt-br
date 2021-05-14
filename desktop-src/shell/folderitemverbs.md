---
description: Representa a coleção de verbos para um item em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.
title: Objeto FolderItemVerbs (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 8206c2113e2fa60abef41e43e4739b6eefd77dd4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840597"
---
# <a name="folderitemverbs-object"></a><span data-ttu-id="6aa68-104">Objeto FolderItemVerbs</span><span class="sxs-lookup"><span data-stu-id="6aa68-104">FolderItemVerbs object</span></span>

<span data-ttu-id="6aa68-105">Representa a coleção de verbos para um item em uma pasta shell.</span><span class="sxs-lookup"><span data-stu-id="6aa68-105">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="6aa68-106">Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="6aa68-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="6aa68-107">Membros</span><span class="sxs-lookup"><span data-stu-id="6aa68-107">Members</span></span>

<span data-ttu-id="6aa68-108">O **objeto FolderItemVerbs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6aa68-108">The **FolderItemVerbs** object has these types of members:</span></span>

-   [<span data-ttu-id="6aa68-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="6aa68-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="6aa68-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6aa68-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6aa68-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6aa68-111">Methods</span></span>

<span data-ttu-id="6aa68-112">O **objeto FolderItemVerbs** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6aa68-112">The **FolderItemVerbs** object has these methods.</span></span>



| <span data-ttu-id="6aa68-113">Método</span><span class="sxs-lookup"><span data-stu-id="6aa68-113">Method</span></span>                                        | <span data-ttu-id="6aa68-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aa68-114">Description</span></span>                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6aa68-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="6aa68-115">**\_NewEnum**</span></span>](folderitemverbs--newenum.md) | <span data-ttu-id="6aa68-116">Cria e retorna um novo **objeto FolderItemVerbs** que é uma cópia desse objeto FolderItemVerbs.</span><span class="sxs-lookup"><span data-stu-id="6aa68-116">Creates and returns a new **FolderItemVerbs** object that is a copy of this FolderItemVerbs object.</span></span><br/>   |
| [<span data-ttu-id="6aa68-117">**Item**</span><span class="sxs-lookup"><span data-stu-id="6aa68-117">**Item**</span></span>](folderitemverbs-item.md)          | <span data-ttu-id="6aa68-118">Recupera o [**objeto FolderItemVerb**](folderitemverb.md) para um item especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="6aa68-118">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6aa68-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6aa68-119">Properties</span></span>

<span data-ttu-id="6aa68-120">O **objeto FolderItemVerbs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6aa68-120">The **FolderItemVerbs** object has these properties.</span></span>



| <span data-ttu-id="6aa68-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6aa68-121">Property</span></span>                                                      | <span data-ttu-id="6aa68-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="6aa68-122">Access type</span></span>          | <span data-ttu-id="6aa68-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="6aa68-123">Description</span></span>                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="6aa68-124">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="6aa68-124">**Application**</span></span>](folderitemverbs-application.md)<br/> | <span data-ttu-id="6aa68-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6aa68-125">Read-only</span></span><br/> | <span data-ttu-id="6aa68-126">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6aa68-126">Not implemented.</span></span><br/>                                |
| [<span data-ttu-id="6aa68-127">**Contagem**</span><span class="sxs-lookup"><span data-stu-id="6aa68-127">**Count**</span></span>](folderitemverbs-count.md)<br/>             | <span data-ttu-id="6aa68-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6aa68-128">Read-only</span></span><br/> | <span data-ttu-id="6aa68-129">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="6aa68-129">Contains the number of items in the collection.</span></span><br/> |
| [<span data-ttu-id="6aa68-130">**Pai**</span><span class="sxs-lookup"><span data-stu-id="6aa68-130">**Parent**</span></span>](folderitemverbs-parent.md)<br/>           | <span data-ttu-id="6aa68-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6aa68-131">Read-only</span></span><br/> | <span data-ttu-id="6aa68-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="6aa68-132">Not implemented.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="6aa68-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6aa68-133">Requirements</span></span>



| <span data-ttu-id="6aa68-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aa68-134">Requirement</span></span> | <span data-ttu-id="6aa68-135">Valor</span><span class="sxs-lookup"><span data-stu-id="6aa68-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aa68-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aa68-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6aa68-137">Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6aa68-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6aa68-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6aa68-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6aa68-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6aa68-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6aa68-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6aa68-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aa68-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6aa68-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6aa68-142">Idl</span><span class="sxs-lookup"><span data-stu-id="6aa68-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6aa68-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6aa68-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6aa68-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6aa68-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aa68-145"><dt>Shell32.dll (versão 4.71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6aa68-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




