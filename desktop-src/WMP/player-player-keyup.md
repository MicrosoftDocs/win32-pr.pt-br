---
title: Evento Player. KeyUp
description: O evento KeyUp ocorre quando uma chave é liberada. | Evento Player. KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Evento KeyUp Windows Media Player
- Evento KeyUp Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779987"
---
# <a name="playerkeyup-event"></a><span data-ttu-id="12c51-107">Evento Player. KeyUp</span><span class="sxs-lookup"><span data-stu-id="12c51-107">Player.KeyUp event</span></span>

<span data-ttu-id="12c51-108">O evento **KeyUp** ocorre quando uma chave é liberada.</span><span class="sxs-lookup"><span data-stu-id="12c51-108">The **KeyUp** event occurs when a key is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="12c51-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12c51-109">Syntax</span></span>


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a><span data-ttu-id="12c51-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12c51-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12c51-111">*nKeyCode*</span><span class="sxs-lookup"><span data-stu-id="12c51-111">*nKeyCode*</span></span> 
</dt> <dd>

<span data-ttu-id="12c51-112">**Número** (**int**) que especifica qual chave física é pressionada.</span><span class="sxs-lookup"><span data-stu-id="12c51-112">**Number** (**int**) specifying which physical key is pressed.</span></span> <span data-ttu-id="12c51-113">Para obter os valores possíveis, consulte [evento Player. KeyDown](player-player-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="12c51-113">For possible values, see [Player.KeyDown Event](player-player-keydown.md).</span></span>

</dd> <dt>

<span data-ttu-id="12c51-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="12c51-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="12c51-115">**Número** (**int**) especificando um campo de bits com os menos significativos que correspondem à tecla Shift (bit 0), a tecla Ctrl (bit 1) e a tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="12c51-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="12c51-116">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="12c51-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="12c51-117">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="12c51-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="12c51-118">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="12c51-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12c51-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12c51-119">Return value</span></span>

<span data-ttu-id="12c51-120">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="12c51-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12c51-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="12c51-121">Remarks</span></span>

<span data-ttu-id="12c51-122">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="12c51-122">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="12c51-123">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="12c51-123">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="12c51-124">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="12c51-124">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="12c51-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12c51-125">Requirements</span></span>



| <span data-ttu-id="12c51-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c51-126">Requirement</span></span> | <span data-ttu-id="12c51-127">Valor</span><span class="sxs-lookup"><span data-stu-id="12c51-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12c51-128">Versão</span><span class="sxs-lookup"><span data-stu-id="12c51-128">Version</span></span><br/> | <span data-ttu-id="12c51-129">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="12c51-129">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="12c51-130">DLL</span><span class="sxs-lookup"><span data-stu-id="12c51-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="12c51-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12c51-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c51-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="12c51-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c51-133">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="12c51-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





