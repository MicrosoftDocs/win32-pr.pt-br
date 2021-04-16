---
title: Método mediacollection. getByAttributeAndMediaType
description: O método getByAttributeAndMediaType recupera um objeto playlist contendo objetos de mídia com o tipo de mídia e o atributo especificados.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- método getByAttributeAndMediaType Windows Media Player
- método getByAttributeAndMediaType Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751123"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="1d16c-106">Método mediacollection. getByAttributeAndMediaType</span><span class="sxs-lookup"><span data-stu-id="1d16c-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="1d16c-107">O método **getByAttributeAndMediaType** recupera um objeto **playlist** contendo objetos de **mídia** com o tipo de mídia e o atributo especificados.</span><span class="sxs-lookup"><span data-stu-id="1d16c-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d16c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d16c-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="1d16c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d16c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d16c-110">*atributo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d16c-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d16c-111">**Cadeia de caracteres** que contém o atributo.</span><span class="sxs-lookup"><span data-stu-id="1d16c-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="1d16c-112">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1d16c-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d16c-113">**Cadeia de caracteres** que contém o valor.</span><span class="sxs-lookup"><span data-stu-id="1d16c-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="1d16c-114">*MediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d16c-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d16c-115">**Cadeia de caracteres** que contém o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1d16c-115">**String** containing the media type.</span></span> <span data-ttu-id="1d16c-116">Deve conter um dos seguintes valores: "áudio", "vídeo", "foto", "playlist" ou "outros".</span><span class="sxs-lookup"><span data-stu-id="1d16c-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d16c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d16c-117">Return value</span></span>

<span data-ttu-id="1d16c-118">Esse método retorna um objeto **playlist**</span><span class="sxs-lookup"><span data-stu-id="1d16c-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="1d16c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d16c-119">Requirements</span></span>



| <span data-ttu-id="1d16c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d16c-120">Requirement</span></span> | <span data-ttu-id="1d16c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1d16c-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d16c-122">Versão</span><span class="sxs-lookup"><span data-stu-id="1d16c-122">Version</span></span><br/> | <span data-ttu-id="1d16c-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1d16c-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="1d16c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1d16c-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d16c-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d16c-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d16c-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d16c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d16c-127">**Referência de atributo**</span><span class="sxs-lookup"><span data-stu-id="1d16c-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="1d16c-128">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="1d16c-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="1d16c-129">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="1d16c-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





