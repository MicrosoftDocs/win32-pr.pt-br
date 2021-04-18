---
title: Método Query. beginNextGroup
description: O método beginNextGroup inicia um novo grupo de condição. | Método Query. beginNextGroup
ms.assetid: e0c59bd0-0789-413e-ade8-8d53c6f3e19b
keywords:
- método beginNextGroup Windows Media Player
- método beginNextGroup Windows Media Player, classe de consulta
- Classe de consulta Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- Query.beginNextGroup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c043b9a0ea506e054877b4d8122304ced75e28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814084"
---
# <a name="querybeginnextgroup-method"></a><span data-ttu-id="821a3-107">Método Query. beginNextGroup</span><span class="sxs-lookup"><span data-stu-id="821a3-107">Query.beginNextGroup method</span></span>

<span data-ttu-id="821a3-108">O método **beginNextGroup** inicia um novo grupo de condição.</span><span class="sxs-lookup"><span data-stu-id="821a3-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="821a3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="821a3-109">Syntax</span></span>


```JScript
Query.beginNextGroup()
```



## <a name="parameters"></a><span data-ttu-id="821a3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="821a3-110">Parameters</span></span>

<span data-ttu-id="821a3-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="821a3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="821a3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="821a3-112">Return value</span></span>

<span data-ttu-id="821a3-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="821a3-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="821a3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="821a3-114">Remarks</span></span>

<span data-ttu-id="821a3-115">Iniciar um novo grupo de condição implica que você concluiu o grupo de condições atual.</span><span class="sxs-lookup"><span data-stu-id="821a3-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="821a3-116">O novo grupo de condição sempre é concatenado ao grupo de condições anterior usando ou lógica.</span><span class="sxs-lookup"><span data-stu-id="821a3-116">The new condition group is always concatenated to the previous condition group using OR logic.</span></span>

## <a name="requirements"></a><span data-ttu-id="821a3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="821a3-117">Requirements</span></span>



| <span data-ttu-id="821a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="821a3-118">Requirement</span></span> | <span data-ttu-id="821a3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="821a3-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="821a3-120">Versão</span><span class="sxs-lookup"><span data-stu-id="821a3-120">Version</span></span><br/> | <span data-ttu-id="821a3-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="821a3-121">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="821a3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="821a3-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="821a3-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="821a3-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="821a3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="821a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821a3-125">**Mediacollection. createQuery**</span><span class="sxs-lookup"><span data-stu-id="821a3-125">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="821a3-126">**Mediacollection. getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="821a3-126">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="821a3-127">**Mediacollection. getStringCollectionByQuery**</span><span class="sxs-lookup"><span data-stu-id="821a3-127">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="821a3-128">**Objeto de consulta**</span><span class="sxs-lookup"><span data-stu-id="821a3-128">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="821a3-129">**Consulta. addcondition**</span><span class="sxs-lookup"><span data-stu-id="821a3-129">**Query.addCondition**</span></span>](query-addcondition.md)
</dt> </dl>

 

 





