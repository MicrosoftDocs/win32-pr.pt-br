---
title: Evento Player. PositionChange
description: O evento PositionChange ocorre quando a posição atual do item de mídia é alterada.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Evento PositionChange do Windows Media Player
- Evento PositionChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento PositionChange
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797643"
---
# <a name="playerpositionchange-event"></a><span data-ttu-id="926a7-106">Evento Player. PositionChange</span><span class="sxs-lookup"><span data-stu-id="926a7-106">Player.PositionChange event</span></span>

<span data-ttu-id="926a7-107">O evento **PositionChange** ocorre quando a posição atual do item de mídia é alterada.</span><span class="sxs-lookup"><span data-stu-id="926a7-107">The **PositionChange** event occurs when the current position of the media item has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="926a7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="926a7-108">Syntax</span></span>


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a><span data-ttu-id="926a7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="926a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="926a7-110">*oldPosition*</span><span class="sxs-lookup"><span data-stu-id="926a7-110">*oldPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="926a7-111">Número (**duplo**) especificando a posição antiga.</span><span class="sxs-lookup"><span data-stu-id="926a7-111">Number (**double**) specifying the old position.</span></span>

</dd> <dt>

<span data-ttu-id="926a7-112">*newPosition*</span><span class="sxs-lookup"><span data-stu-id="926a7-112">*newPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="926a7-113">**Número** (**duplo**) especificando a nova posição.</span><span class="sxs-lookup"><span data-stu-id="926a7-113">**Number** (**double**) specifying the new position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="926a7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="926a7-114">Return value</span></span>

<span data-ttu-id="926a7-115">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="926a7-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="926a7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="926a7-116">Remarks</span></span>

<span data-ttu-id="926a7-117">Esse evento não é gerado rotineiramente durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="926a7-117">This event is not raised routinely during playback.</span></span> <span data-ttu-id="926a7-118">Isso ocorre apenas quando algo altera ativamente a posição atual do item de mídia em execução, como o usuário que move o identificador de busca ou o código que especifica um valor para *controles*. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="926a7-118">It only occurs when something actively changes the current position of the playing media item, such as the user moving the seek handle or code specifying a value for *Controls*.**currentPosition**.</span></span>

<span data-ttu-id="926a7-119">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="926a7-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="926a7-120">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="926a7-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="926a7-121">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="926a7-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="926a7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="926a7-122">Requirements</span></span>



| <span data-ttu-id="926a7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="926a7-123">Requirement</span></span> | <span data-ttu-id="926a7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="926a7-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="926a7-125">Versão</span><span class="sxs-lookup"><span data-stu-id="926a7-125">Version</span></span><br/> | <span data-ttu-id="926a7-126">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="926a7-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="926a7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="926a7-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="926a7-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="926a7-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926a7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="926a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926a7-130">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="926a7-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





