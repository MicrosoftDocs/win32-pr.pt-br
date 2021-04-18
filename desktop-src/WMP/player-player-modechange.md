---
title: Evento Player. ModeChange
description: O evento ModeChange ocorre quando um modo do Windows Media Player é alterado. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Evento ModeChange do Windows Media Player
- Evento ModeChange Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760578"
---
# <a name="playermodechange-event"></a><span data-ttu-id="3393f-107">Evento Player. ModeChange</span><span class="sxs-lookup"><span data-stu-id="3393f-107">Player.ModeChange event</span></span>

<span data-ttu-id="3393f-108">O evento **ModeChange** ocorre quando um modo do Windows Media Player é alterado.</span><span class="sxs-lookup"><span data-stu-id="3393f-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3393f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3393f-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="3393f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3393f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3393f-111">*ModeName*</span><span class="sxs-lookup"><span data-stu-id="3393f-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="3393f-112">**Cadeia de caracteres** que indica o modo que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3393f-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="3393f-113">Contém um dos seguintes valores.</span><span class="sxs-lookup"><span data-stu-id="3393f-113">Contains one of the following values.</span></span>



| <span data-ttu-id="3393f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3393f-114">Value</span></span>   | <span data-ttu-id="3393f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3393f-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="3393f-116">ordem aleatória</span><span class="sxs-lookup"><span data-stu-id="3393f-116">shuffle</span></span> | <span data-ttu-id="3393f-117">As faixas são reproduzidas em ordem aleatória.</span><span class="sxs-lookup"><span data-stu-id="3393f-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="3393f-118">loop</span><span class="sxs-lookup"><span data-stu-id="3393f-118">loop</span></span>    | <span data-ttu-id="3393f-119">A sequência inteira de faixas é reproduzida repetidamente.</span><span class="sxs-lookup"><span data-stu-id="3393f-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3393f-120">*NewValue*</span><span class="sxs-lookup"><span data-stu-id="3393f-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="3393f-121">**Booliano** que indica o novo estado do modo especificado.</span><span class="sxs-lookup"><span data-stu-id="3393f-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3393f-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3393f-122">Return value</span></span>

<span data-ttu-id="3393f-123">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3393f-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3393f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3393f-124">Remarks</span></span>

<span data-ttu-id="3393f-125">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="3393f-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="3393f-126">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="3393f-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="3393f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3393f-127">Requirements</span></span>



| <span data-ttu-id="3393f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3393f-128">Requirement</span></span> | <span data-ttu-id="3393f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3393f-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3393f-130">Versão</span><span class="sxs-lookup"><span data-stu-id="3393f-130">Version</span></span><br/> | <span data-ttu-id="3393f-131">Windows Media Player versão 7,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3393f-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3393f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3393f-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="3393f-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3393f-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3393f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3393f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3393f-135">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="3393f-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="3393f-136">**Settings. GetMode**</span><span class="sxs-lookup"><span data-stu-id="3393f-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="3393f-137">**Settings. setmode**</span><span class="sxs-lookup"><span data-stu-id="3393f-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





