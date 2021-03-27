---
description: Representa a coleção de verbos de um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.
title: Objeto FolderItemVerbs (shldisp. h)
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
ms.openlocfilehash: 651f439ea34a55203da852f2907a27ba87bdd275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828301"
---
# <a name="folderitemverbs-object"></a><span data-ttu-id="3ca47-104">Objeto FolderItemVerbs</span><span class="sxs-lookup"><span data-stu-id="3ca47-104">FolderItemVerbs object</span></span>

<span data-ttu-id="3ca47-105">Representa a coleção de verbos de um item em uma pasta do Shell.</span><span class="sxs-lookup"><span data-stu-id="3ca47-105">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="3ca47-106">Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.</span><span class="sxs-lookup"><span data-stu-id="3ca47-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="3ca47-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3ca47-107">Members</span></span>

<span data-ttu-id="3ca47-108">O objeto **FolderItemVerbs** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3ca47-108">The **FolderItemVerbs** object has these types of members:</span></span>

-   [<span data-ttu-id="3ca47-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ca47-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ca47-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ca47-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ca47-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ca47-111">Methods</span></span>

<span data-ttu-id="3ca47-112">O objeto **FolderItemVerbs** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3ca47-112">The **FolderItemVerbs** object has these methods.</span></span>



| <span data-ttu-id="3ca47-113">Método</span><span class="sxs-lookup"><span data-stu-id="3ca47-113">Method</span></span>                                        | <span data-ttu-id="3ca47-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ca47-114">Description</span></span>                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca47-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="3ca47-115">**\_NewEnum**</span></span>](folderitemverbs--newenum.md) | <span data-ttu-id="3ca47-116">Cria e retorna um novo objeto **FolderItemVerbs** que é uma cópia desse objeto FolderItemVerbs.</span><span class="sxs-lookup"><span data-stu-id="3ca47-116">Creates and returns a new **FolderItemVerbs** object that is a copy of this FolderItemVerbs object.</span></span><br/>   |
| [<span data-ttu-id="3ca47-117">**Item**</span><span class="sxs-lookup"><span data-stu-id="3ca47-117">**Item**</span></span>](folderitemverbs-item.md)          | <span data-ttu-id="3ca47-118">Recupera o objeto [**FolderItemVerb**](folderitemverb.md) para um item especificado na coleção.</span><span class="sxs-lookup"><span data-stu-id="3ca47-118">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3ca47-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3ca47-119">Properties</span></span>

<span data-ttu-id="3ca47-120">O objeto **FolderItemVerbs** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3ca47-120">The **FolderItemVerbs** object has these properties.</span></span>



| <span data-ttu-id="3ca47-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3ca47-121">Property</span></span>                                                      | <span data-ttu-id="3ca47-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="3ca47-122">Access type</span></span>          | <span data-ttu-id="3ca47-123">Description</span><span class="sxs-lookup"><span data-stu-id="3ca47-123">Description</span></span>                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="3ca47-124">**Aplicativo**</span><span class="sxs-lookup"><span data-stu-id="3ca47-124">**Application**</span></span>](folderitemverbs-application.md)<br/> | <span data-ttu-id="3ca47-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ca47-125">Read-only</span></span><br/> | <span data-ttu-id="3ca47-126">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="3ca47-126">Not implemented.</span></span><br/>                                |
| [<span data-ttu-id="3ca47-127">**Contar**</span><span class="sxs-lookup"><span data-stu-id="3ca47-127">**Count**</span></span>](folderitemverbs-count.md)<br/>             | <span data-ttu-id="3ca47-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ca47-128">Read-only</span></span><br/> | <span data-ttu-id="3ca47-129">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="3ca47-129">Contains the number of items in the collection.</span></span><br/> |
| [<span data-ttu-id="3ca47-130">**Pai**</span><span class="sxs-lookup"><span data-stu-id="3ca47-130">**Parent**</span></span>](folderitemverbs-parent.md)<br/>           | <span data-ttu-id="3ca47-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3ca47-131">Read-only</span></span><br/> | <span data-ttu-id="3ca47-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="3ca47-132">Not implemented.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="3ca47-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ca47-133">Requirements</span></span>



| <span data-ttu-id="3ca47-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ca47-134">Requirement</span></span> | <span data-ttu-id="3ca47-135">Valor</span><span class="sxs-lookup"><span data-stu-id="3ca47-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ca47-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ca47-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3ca47-137">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ca47-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ca47-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ca47-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3ca47-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ca47-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ca47-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ca47-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ca47-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ca47-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3ca47-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ca47-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ca47-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ca47-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3ca47-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3ca47-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ca47-145"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3ca47-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




