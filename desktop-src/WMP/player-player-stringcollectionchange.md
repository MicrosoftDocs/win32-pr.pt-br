---
title: Evento Player. StringCollectionChange
description: O evento StringCollectionChange ocorre quando uma coleção de cadeia de caracteres é alterada. | Evento Player. StringCollectionChange
ms.assetid: 465ec694-afd1-4baa-b559-3ab75874388f
keywords:
- Evento StringCollectionChange do Windows Media Player
- Evento StringCollectionChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento StringCollectionChange
topic_type:
- apiref
api_name:
- Player.StringCollectionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29f72d7af0f73d74393d980b2506a3b7f05e578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790591"
---
# <a name="playerstringcollectionchange-event"></a><span data-ttu-id="0f459-107">Evento Player. StringCollectionChange</span><span class="sxs-lookup"><span data-stu-id="0f459-107">Player.StringCollectionChange event</span></span>

<span data-ttu-id="0f459-108">O evento StringCollectionChange ocorre quando uma coleção de cadeia de caracteres é alterada.</span><span class="sxs-lookup"><span data-stu-id="0f459-108">The StringCollectionChange event occurs when a string collection changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f459-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f459-109">Syntax</span></span>


```JScript
Player.StringCollectionChange(
  pdispStringCollection,
  change,
  lCollectionIndex
)
```



## <a name="parameters"></a><span data-ttu-id="0f459-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f459-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f459-111">*pdispStringCollection*</span><span class="sxs-lookup"><span data-stu-id="0f459-111">*pdispStringCollection*</span></span> 
</dt> <dd>

<span data-ttu-id="0f459-112">Objeto **StringCollection** que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="0f459-112">**StringCollection** object that changed.</span></span>

</dd> <dt>

<span data-ttu-id="0f459-113">*change*</span><span class="sxs-lookup"><span data-stu-id="0f459-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="0f459-114">Número (longo) indicando o tipo de alteração ocorrida na coleção de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0f459-114">Number (long)indicating the type of change that occurred to the string collection.</span></span> <span data-ttu-id="0f459-115">Inclui um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0f459-115">Includes one of the following values.</span></span>



|        |                                    |
|--------|------------------------------------|
| <span data-ttu-id="0f459-116">Número</span><span class="sxs-lookup"><span data-stu-id="0f459-116">Number</span></span> | <span data-ttu-id="0f459-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f459-117">Description</span></span>                        |
| <span data-ttu-id="0f459-118">0</span><span class="sxs-lookup"><span data-stu-id="0f459-118">0</span></span>      | <span data-ttu-id="0f459-119">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="0f459-119">Unknown.</span></span> <span data-ttu-id="0f459-120">(Não é um valor válido)</span><span class="sxs-lookup"><span data-stu-id="0f459-120">(Not a valid value)</span></span>       |
| <span data-ttu-id="0f459-121">1</span><span class="sxs-lookup"><span data-stu-id="0f459-121">1</span></span>      | <span data-ttu-id="0f459-122">Um item foi inserido.</span><span class="sxs-lookup"><span data-stu-id="0f459-122">An item was inserted.</span></span>              |
| <span data-ttu-id="0f459-123">2</span><span class="sxs-lookup"><span data-stu-id="0f459-123">2</span></span>      | <span data-ttu-id="0f459-124">A coleção de cadeia de caracteres foi alterada.</span><span class="sxs-lookup"><span data-stu-id="0f459-124">The string collection changed.</span></span>     |
| <span data-ttu-id="0f459-125">3</span><span class="sxs-lookup"><span data-stu-id="0f459-125">3</span></span>      | <span data-ttu-id="0f459-126">Um item foi excluído.</span><span class="sxs-lookup"><span data-stu-id="0f459-126">An item was deleted.</span></span>               |
| <span data-ttu-id="0f459-127">4</span><span class="sxs-lookup"><span data-stu-id="0f459-127">4</span></span>      | <span data-ttu-id="0f459-128">A coleção de cadeias de caracteres foi limpa.</span><span class="sxs-lookup"><span data-stu-id="0f459-128">The string collection was cleared.</span></span> |
| <span data-ttu-id="0f459-129">5</span><span class="sxs-lookup"><span data-stu-id="0f459-129">5</span></span>      | <span data-ttu-id="0f459-130">As atualizações em massa estão começando.</span><span class="sxs-lookup"><span data-stu-id="0f459-130">Bulk updates are beginning.</span></span>        |
| <span data-ttu-id="0f459-131">6</span><span class="sxs-lookup"><span data-stu-id="0f459-131">6</span></span>      | <span data-ttu-id="0f459-132">Atualizações em massa encerradas.</span><span class="sxs-lookup"><span data-stu-id="0f459-132">Bulk updates have ended.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="0f459-133">*lCollectionIndex*</span><span class="sxs-lookup"><span data-stu-id="0f459-133">*lCollectionIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="0f459-134">Número (longo) que contém o índice do item de coleção de cadeia de caracteres que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="0f459-134">Number (long) containing the index of the string collection item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f459-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f459-135">Return value</span></span>

<span data-ttu-id="0f459-136">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0f459-136">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f459-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f459-137">Remarks</span></span>

<span data-ttu-id="0f459-138">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="0f459-138">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f459-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f459-139">Requirements</span></span>



| <span data-ttu-id="0f459-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f459-140">Requirement</span></span> | <span data-ttu-id="0f459-141">Valor</span><span class="sxs-lookup"><span data-stu-id="0f459-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f459-142">Versão</span><span class="sxs-lookup"><span data-stu-id="0f459-142">Version</span></span><br/> | <span data-ttu-id="0f459-143">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="0f459-143">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="0f459-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0f459-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f459-145"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f459-145"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f459-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f459-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f459-147">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="0f459-147">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="0f459-148">**Objeto StringCollection**</span><span class="sxs-lookup"><span data-stu-id="0f459-148">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





