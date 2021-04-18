---
title: Método mediacollection. getStringCollectionByQuery
description: O método getStringCollectionByQuery recupera um objeto StringCollection que contém todas as cadeias de caracteres que correspondem às condições de consulta.
ms.assetid: 17442151-7eb1-4256-ac5f-142b11645216
keywords:
- método getStringCollectionByQuery Windows Media Player
- método getStringCollectionByQuery Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getStringCollectionByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getStringCollectionByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf304d22cb207d8a2bfb046522e8704e900d508
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789534"
---
# <a name="mediacollectiongetstringcollectionbyquery-method"></a><span data-ttu-id="7e42f-106">Método mediacollection. getStringCollectionByQuery</span><span class="sxs-lookup"><span data-stu-id="7e42f-106">MediaCollection.getStringCollectionByQuery method</span></span>

<span data-ttu-id="7e42f-107">O método **getStringCollectionByQuery** recupera um objeto **StringCollection** que contém todas as cadeias de caracteres que correspondem às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="7e42f-107">The **getStringCollectionByQuery** method retrieves a **StringCollection** object containing all strings that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e42f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e42f-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getStringCollectionByQuery(
  attribute,
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="7e42f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e42f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e42f-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e42f-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e42f-111">**Cadeia de caracteres** que contém o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="7e42f-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="7e42f-112">*consulta* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="7e42f-112">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e42f-113">Objeto de **consulta** .</span><span class="sxs-lookup"><span data-stu-id="7e42f-113">**Query** object.</span></span>

</dd> <dt>

<span data-ttu-id="7e42f-114">*MediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e42f-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e42f-115">**Cadeia de caracteres** que contém o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7e42f-115">**String** containing the media type.</span></span> <span data-ttu-id="7e42f-116">Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".</span><span class="sxs-lookup"><span data-stu-id="7e42f-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="7e42f-117">*tipo de classificação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e42f-117">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e42f-118">**Cadeia de caracteres** que contém o nome do atributo usado para classificação.</span><span class="sxs-lookup"><span data-stu-id="7e42f-118">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="7e42f-119">Uma cadeia de caracteres vazia ("") significa que nenhuma classificação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="7e42f-119">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="7e42f-120">*sortAscending* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7e42f-120">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e42f-121">**Booliano**, verdadeiro indicando que a **StringCollection** deve ser classificada em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="7e42f-121">**Boolean**, true indicating that the **StringCollection** must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e42f-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e42f-122">Return value</span></span>

<span data-ttu-id="7e42f-123">Esse método retorna um objeto **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="7e42f-123">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e42f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e42f-124">Remarks</span></span>

<span data-ttu-id="7e42f-125">Consultas compostas usando a **consulta** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7e42f-125">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="7e42f-126">Quando a consulta composta especificada pelo parâmetro de *consulta* contém uma condição criada no atributo **MediaType** , essa condição é ignorada.</span><span class="sxs-lookup"><span data-stu-id="7e42f-126">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="7e42f-127">O valor do parâmetro *MediaType* é sempre usado.</span><span class="sxs-lookup"><span data-stu-id="7e42f-127">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="7e42f-128">Por exemplo, se a consulta composta contiver a condição "MediaType igual a áudio" e o valor do parâmetro *MediaType* for "vídeo", a lista de reprodução resultante conterá apenas itens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7e42f-128">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e42f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e42f-129">Requirements</span></span>



| <span data-ttu-id="7e42f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e42f-130">Requirement</span></span> | <span data-ttu-id="7e42f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7e42f-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7e42f-132">Versão</span><span class="sxs-lookup"><span data-stu-id="7e42f-132">Version</span></span><br/> | <span data-ttu-id="7e42f-133">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="7e42f-133">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="7e42f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7e42f-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e42f-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e42f-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e42f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e42f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e42f-137">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="7e42f-137">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7e42f-138">**Atributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="7e42f-138">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="7e42f-139">**Objeto de consulta**</span><span class="sxs-lookup"><span data-stu-id="7e42f-139">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





