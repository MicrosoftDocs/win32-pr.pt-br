---
title: Evento Player. Click
description: O evento de clique ocorre quando o usuário clica em um botão do mouse.
ms.assetid: c2d5fab9-9b53-4d0c-a001-8cbf4430e713
keywords:
- Clique em evento Windows Media Player
- Clique em evento Windows Media Player, classe Player
- Classe de Player Windows Media Player, evento de clique
topic_type:
- apiref
api_name:
- Player.Click
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8389460d59018b221749719d32edbaa89943808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810878"
---
# <a name="playerclick-event"></a><span data-ttu-id="1cc42-106">Evento Player. Click</span><span class="sxs-lookup"><span data-stu-id="1cc42-106">Player.Click event</span></span>

<span data-ttu-id="1cc42-107">O evento de **clique** ocorre quando o usuário clica em um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="1cc42-107">The **Click** event occurs when the user clicks a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc42-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cc42-108">Syntax</span></span>


```JScript
Player.Click(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="1cc42-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cc42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc42-110">*Nnovo*</span><span class="sxs-lookup"><span data-stu-id="1cc42-110">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc42-111">**Número** (**int**) que especifica um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="1cc42-111">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="1cc42-112">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1cc42-112">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1cc42-113">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="1cc42-113">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="1cc42-114">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="1cc42-114">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc42-115">**Número** (**int**) especificando um campo de bits com os menos significativos que correspondem à tecla Shift (bit 0), a tecla Ctrl (bit 1) e a tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="1cc42-115">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="1cc42-116">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1cc42-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="1cc42-117">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="1cc42-117">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="1cc42-118">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="1cc42-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="1cc42-119">*Efeito*</span><span class="sxs-lookup"><span data-stu-id="1cc42-119">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc42-120">**Número** (**longo**) que especifica a coordenada x do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="1cc42-120">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="1cc42-121">*SAR*</span><span class="sxs-lookup"><span data-stu-id="1cc42-121">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="1cc42-122">**Número** (**longo**) que especifica a coordenada y do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="1cc42-122">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc42-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cc42-123">Return value</span></span>

<span data-ttu-id="1cc42-124">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1cc42-124">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc42-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cc42-125">Remarks</span></span>

<span data-ttu-id="1cc42-126">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="1cc42-126">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="1cc42-127">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="1cc42-127">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="1cc42-128">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="1cc42-128">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc42-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc42-129">Requirements</span></span>



| <span data-ttu-id="1cc42-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc42-130">Requirement</span></span> | <span data-ttu-id="1cc42-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1cc42-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc42-132">Versão</span><span class="sxs-lookup"><span data-stu-id="1cc42-132">Version</span></span><br/> | <span data-ttu-id="1cc42-133">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1cc42-133">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1cc42-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1cc42-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="1cc42-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cc42-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc42-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cc42-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc42-137">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="1cc42-137">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





