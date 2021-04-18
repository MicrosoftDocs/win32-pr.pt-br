---
title: Evento Player. MediaCollectionAttributeStringChanged
description: O evento MediaCollectionAttributeStringChanged ocorre quando um valor de atributo na biblioteca é alterado. | Evento Player. MediaCollectionAttributeStringChanged
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Evento MediaCollectionAttributeStringChanged do Windows Media Player
- Evento MediaCollectionAttributeStringChanged Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MediaCollectionAttributeStringChanged
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814024"
---
# <a name="playermediacollectionattributestringchanged-event"></a><span data-ttu-id="9251e-107">Evento Player. MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="9251e-107">Player.MediaCollectionAttributeStringChanged event</span></span>

<span data-ttu-id="9251e-108">O evento **MediaCollectionAttributeStringChanged** ocorre quando um valor de atributo na biblioteca é alterado.</span><span class="sxs-lookup"><span data-stu-id="9251e-108">The **MediaCollectionAttributeStringChanged** event occurs when an attribute value in the library is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9251e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9251e-109">Syntax</span></span>


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a><span data-ttu-id="9251e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9251e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9251e-111">*bstrAttribName*</span><span class="sxs-lookup"><span data-stu-id="9251e-111">*bstrAttribName*</span></span> 
</dt> <dd>

<span data-ttu-id="9251e-112">**Cadeia de caracteres** que especifica o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="9251e-112">**String** specifying the name of the attribute.</span></span> <span data-ttu-id="9251e-113">Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [referência de atributo](attribute-reference.md)do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9251e-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="9251e-114">*bstrOldAttribVal*</span><span class="sxs-lookup"><span data-stu-id="9251e-114">*bstrOldAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9251e-115">**Cadeia de caracteres** que especifica o valor antigo do atributo.</span><span class="sxs-lookup"><span data-stu-id="9251e-115">**String** specifying the old value of the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="9251e-116">*bstrNewAttribVal*</span><span class="sxs-lookup"><span data-stu-id="9251e-116">*bstrNewAttribVal*</span></span> 
</dt> <dd>

<span data-ttu-id="9251e-117">**Cadeia de caracteres** que especifica o novo valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="9251e-117">**String** specifying the new value of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9251e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9251e-118">Return value</span></span>

<span data-ttu-id="9251e-119">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9251e-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9251e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9251e-120">Remarks</span></span>

<span data-ttu-id="9251e-121">Quando um usuário modifica os metadados da biblioteca, o objeto **mediacollection** é atualizado e esse evento é acionado para cada atributo alterado.</span><span class="sxs-lookup"><span data-stu-id="9251e-121">When a user modifies library metadata, the **MediaCollection** object is updated and this event fires for each attribute changed.</span></span>

<span data-ttu-id="9251e-122">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="9251e-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="9251e-123">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="9251e-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="9251e-124">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="9251e-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="9251e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9251e-125">Requirements</span></span>



| <span data-ttu-id="9251e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9251e-126">Requirement</span></span> | <span data-ttu-id="9251e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9251e-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9251e-128">Versão</span><span class="sxs-lookup"><span data-stu-id="9251e-128">Version</span></span><br/> | <span data-ttu-id="9251e-129">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9251e-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="9251e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9251e-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="9251e-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9251e-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9251e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9251e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9251e-133">**Objeto mediacollection**</span><span class="sxs-lookup"><span data-stu-id="9251e-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="9251e-134">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="9251e-134">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="9251e-135">**Player. mediacollection**</span><span class="sxs-lookup"><span data-stu-id="9251e-135">**Player.mediaCollection**</span></span>](player-mediacollection.md)
</dt> </dl>

 

 





