---
description: Classe de coleção
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Objeto de coleção
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296769"
---
# <a name="collection-object"></a><span data-ttu-id="b0b50-103">Objeto de coleção</span><span class="sxs-lookup"><span data-stu-id="b0b50-103">Collection object</span></span>

<span data-ttu-id="b0b50-104">Classe de coleção</span><span class="sxs-lookup"><span data-stu-id="b0b50-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="b0b50-105">Membros</span><span class="sxs-lookup"><span data-stu-id="b0b50-105">Members</span></span>

<span data-ttu-id="b0b50-106">O objeto de **coleção** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b0b50-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="b0b50-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0b50-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0b50-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0b50-108">Properties</span></span>

<span data-ttu-id="b0b50-109">O objeto de **coleção** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0b50-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="b0b50-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b0b50-110">Property</span></span>                                           | <span data-ttu-id="b0b50-111">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b0b50-111">Access type</span></span>          | <span data-ttu-id="b0b50-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b0b50-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="b0b50-113">**Contar**</span><span class="sxs-lookup"><span data-stu-id="b0b50-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="b0b50-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0b50-114">Read-only</span></span><br/> | <span data-ttu-id="b0b50-115">Retorna o número de membros na coleção</span><span class="sxs-lookup"><span data-stu-id="b0b50-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="b0b50-116">**Item**</span><span class="sxs-lookup"><span data-stu-id="b0b50-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="b0b50-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0b50-117">Read-only</span></span><br/> | <span data-ttu-id="b0b50-118">Retorna o item especificado na coleção</span><span class="sxs-lookup"><span data-stu-id="b0b50-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="b0b50-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0b50-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="b0b50-120">Criar \\ funções de acesso</span><span class="sxs-lookup"><span data-stu-id="b0b50-120">Creation\\Access Functions</span></span>

<span data-ttu-id="b0b50-121">Use qualquer um dos seguintes para recuperar uma referência ao objeto:</span><span class="sxs-lookup"><span data-stu-id="b0b50-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="b0b50-122">**GetItemsFromUI**</span><span class="sxs-lookup"><span data-stu-id="b0b50-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="b0b50-123">**Children**</span><span class="sxs-lookup"><span data-stu-id="b0b50-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="b0b50-124">**Dispositivos**</span><span class="sxs-lookup"><span data-stu-id="b0b50-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="b0b50-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0b50-125">Requirements</span></span>



| <span data-ttu-id="b0b50-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0b50-126">Requirement</span></span> | <span data-ttu-id="b0b50-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b0b50-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b50-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0b50-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b50-129">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b0b50-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0b50-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0b50-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b50-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0b50-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b0b50-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b0b50-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0b50-133"><dt>Wiascr.dll (versão 4,90 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b50-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




