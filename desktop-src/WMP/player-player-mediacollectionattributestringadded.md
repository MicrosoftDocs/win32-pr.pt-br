---
title: Evento Player. MediaCollectionAttributeStringAdded
description: O evento MediaCollectionAttributeStringAdded ocorre quando um valor de atributo é adicionado à biblioteca. | Evento Player. MediaCollectionAttributeStringAdded
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Evento MediaCollectionAttributeStringAdded do Windows Media Player
- Evento MediaCollectionAttributeStringAdded Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaCollectionAttributeStringAdded
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796193"
---
# <a name="playermediacollectionattributestringadded-event"></a><span data-ttu-id="29145-107">Evento Player. MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="29145-107">Player.MediaCollectionAttributeStringAdded event</span></span>

<span data-ttu-id="29145-108">O evento **MediaCollectionAttributeStringAdded** ocorre quando um valor de atributo é adicionado à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="29145-108">The **MediaCollectionAttributeStringAdded** event occurs when an attribute value is added to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="29145-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29145-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="29145-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29145-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29145-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="29145-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="29145-112">**Cadeia de caracteres** que especifica o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="29145-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="29145-113">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="29145-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="29145-114">*bstrAttribVal*</span><span class="sxs-lookup"><span data-stu-id="29145-114">*bstrAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="29145-115">**Cadeia de caracteres** que especifica o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="29145-115">**String** specifying the value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29145-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29145-116">Return value</span></span>

<span data-ttu-id="29145-117">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="29145-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29145-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="29145-118">Remarks</span></span>

<span data-ttu-id="29145-119">Quando um item de mídia é adicionado à biblioteca, seus metadados são adicionados ao objeto **mediacollection** e esse evento é acionado para cada atributo adicionado.</span><span class="sxs-lookup"><span data-stu-id="29145-119">When a media item is added to the library its metadata is added to the **MediaCollection** object and this event is fired for each attribute added.</span></span>

<span data-ttu-id="29145-120">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="29145-120">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="29145-121">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="29145-121">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="29145-122">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="29145-122">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="29145-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29145-123">Requirements</span></span>



| <span data-ttu-id="29145-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="29145-124">Requirement</span></span> | <span data-ttu-id="29145-125">Valor</span><span class="sxs-lookup"><span data-stu-id="29145-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29145-126">Versão</span><span class="sxs-lookup"><span data-stu-id="29145-126">Version</span></span><br/> | <span data-ttu-id="29145-127">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="29145-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="29145-128">DLL</span><span class="sxs-lookup"><span data-stu-id="29145-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="29145-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29145-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29145-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="29145-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29145-131">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="29145-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="29145-132">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="29145-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="29145-133">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="29145-133">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





