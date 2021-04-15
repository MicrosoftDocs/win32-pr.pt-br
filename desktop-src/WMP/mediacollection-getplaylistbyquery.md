---
title: Método mediacollection. getPlaylistByQuery
description: O método getPlaylistByQuery recupera um objeto playlist contendo objetos de mídia que correspondem às condições de consulta.
ms.assetid: 3487d442-a5bb-4519-ac45-d0138516305e
keywords:
- método getPlaylistByQuery Windows Media Player
- método getPlaylistByQuery Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getPlaylistByQuery
topic_type:
- apiref
api_name:
- MediaCollection.getPlaylistByQuery
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50b57d4303ba8784f912db9570faacb26d01677d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761436"
---
# <a name="mediacollectiongetplaylistbyquery-method"></a><span data-ttu-id="a808b-106">Método mediacollection. getPlaylistByQuery</span><span class="sxs-lookup"><span data-stu-id="a808b-106">MediaCollection.getPlaylistByQuery method</span></span>

<span data-ttu-id="a808b-107">O método **getPlaylistByQuery** recupera um objeto **playlist** contendo objetos de **mídia** que correspondem às condições de consulta.</span><span class="sxs-lookup"><span data-stu-id="a808b-107">The **getPlaylistByQuery** method retrieves a **Playlist** object containing **Media** objects that match the query conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a808b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a808b-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getPlaylistByQuery(
  query,
  mediaType,
  sortAttribute,
  sortAscending
)
```



## <a name="parameters"></a><span data-ttu-id="a808b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a808b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a808b-110">*consulta* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a808b-110">*query* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a808b-111">Objeto de **consulta** que define as condições usadas para criar a lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a808b-111">**Query** object that defines the conditions used to create the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="a808b-112">*MediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a808b-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a808b-113">**Cadeia de caracteres** que contém o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a808b-113">**String** containing the media type.</span></span> <span data-ttu-id="a808b-114">Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".</span><span class="sxs-lookup"><span data-stu-id="a808b-114">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> <dt>

<span data-ttu-id="a808b-115">*tipo de classificação* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a808b-115">*sortAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a808b-116">**Cadeia de caracteres** que contém o nome do atributo usado para classificação.</span><span class="sxs-lookup"><span data-stu-id="a808b-116">**String** containing the attribute name used for sorting.</span></span> <span data-ttu-id="a808b-117">Uma cadeia de caracteres vazia ("") significa que nenhuma classificação é aplicada.</span><span class="sxs-lookup"><span data-stu-id="a808b-117">An empty string ("") means no sorting is applied.</span></span>

</dd> <dt>

<span data-ttu-id="a808b-118">*sortAscending* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a808b-118">*sortAscending* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a808b-119">**Booliano**, verdadeiro indicando que a lista de reprodução deve ser classificada em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="a808b-119">**Boolean**, true indicating that the playlist must be sorted in ascending order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a808b-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a808b-120">Return value</span></span>

<span data-ttu-id="a808b-121">Esse método retorna um objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="a808b-121">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a808b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a808b-122">Remarks</span></span>

<span data-ttu-id="a808b-123">Consultas compostas usando a **consulta** não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a808b-123">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="a808b-124">Quando a consulta composta especificada pelo parâmetro de *consulta* contém uma condição criada no atributo **MediaType** , essa condição é ignorada.</span><span class="sxs-lookup"><span data-stu-id="a808b-124">When the compound query specified by the *query* parameter contains a condition built on the **MediaType** attribute, that condition is ignored.</span></span> <span data-ttu-id="a808b-125">O valor do parâmetro *MediaType* é sempre usado.</span><span class="sxs-lookup"><span data-stu-id="a808b-125">The value for the *mediaType* parameter is always used.</span></span> <span data-ttu-id="a808b-126">Por exemplo, se a consulta composta contiver a condição "MediaType igual a áudio" e o valor do parâmetro *MediaType* for "vídeo", a lista de reprodução resultante conterá apenas itens de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a808b-126">For example, if the compound query contains the condition "MediaType Equals audio" and the value for the *mediaType* parameter is "video", the resulting playlist will contain only video items.</span></span>

## <a name="requirements"></a><span data-ttu-id="a808b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a808b-127">Requirements</span></span>



| <span data-ttu-id="a808b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a808b-128">Requirement</span></span> | <span data-ttu-id="a808b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a808b-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a808b-130">Versão</span><span class="sxs-lookup"><span data-stu-id="a808b-130">Version</span></span><br/> | <span data-ttu-id="a808b-131">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="a808b-131">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="a808b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a808b-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="a808b-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a808b-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a808b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a808b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a808b-135">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="a808b-135">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="a808b-136">**Atributo MediaType**</span><span class="sxs-lookup"><span data-stu-id="a808b-136">**MediaType Attribute**</span></span>](mediatype-attribute.md)
</dt> <dt>

[<span data-ttu-id="a808b-137">**Objeto de consulta**</span><span class="sxs-lookup"><span data-stu-id="a808b-137">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 





