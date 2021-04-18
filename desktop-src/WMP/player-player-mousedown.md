---
title: Evento Player. MouseDown
description: O evento MouseDown ocorre quando o usuário pressiona um botão do mouse. | Evento Player. MouseDown
ms.assetid: cc2fd2ca-c974-4683-98ca-2202c4d5b240
keywords:
- Evento MouseDown do Windows Media Player
- Evento MouseDown Windows Media Player, classe Player
- Classe de jogador Windows Media Player, evento MouseDown
topic_type:
- apiref
api_name:
- Player.MouseDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29eb0c8aa5f6731f94d0e4c3b4ff967cb7819f42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764151"
---
# <a name="playermousedown-event"></a><span data-ttu-id="c53da-107">Evento Player. MouseDown</span><span class="sxs-lookup"><span data-stu-id="c53da-107">Player.MouseDown event</span></span>

<span data-ttu-id="c53da-108">O evento **MouseDown** ocorre quando o usuário pressiona um botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="c53da-108">The **MouseDown** event occurs when the user presses a mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="c53da-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c53da-109">Syntax</span></span>


```JScript
Player.MouseDown(
  nButton,
  nShiftState,
  fX,
  fY
)
```



## <a name="parameters"></a><span data-ttu-id="c53da-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c53da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c53da-111">*Nnovo*</span><span class="sxs-lookup"><span data-stu-id="c53da-111">*nButton*</span></span> 
</dt> <dd>

<span data-ttu-id="c53da-112">**Número** (**int**) que especifica um campo de bits que corresponde ao botão esquerdo (bit 0), ao botão direito (bit 1) e ao botão do meio (bit 2).</span><span class="sxs-lookup"><span data-stu-id="c53da-112">**Number** (**int**) specifying a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="c53da-113">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c53da-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="c53da-114">Apenas um dos bits é definido, indicando o botão que causou o evento.</span><span class="sxs-lookup"><span data-stu-id="c53da-114">Only one of the bits is set, indicating the button that caused the event.</span></span>

</dd> <dt>

<span data-ttu-id="c53da-115">*nShiftState*</span><span class="sxs-lookup"><span data-stu-id="c53da-115">*nShiftState*</span></span> 
</dt> <dd>

<span data-ttu-id="c53da-116">**Número** (**int**) especificando um campo de bits com os menos significativos que correspondem à tecla Shift (bit 0), a tecla Ctrl (bit 1) e a tecla Alt (bit 2).</span><span class="sxs-lookup"><span data-stu-id="c53da-116">**Number** (**int**) specifying a bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="c53da-117">Esses bits correspondem aos valores 1, 2 e 4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c53da-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="c53da-118">O argumento Shift indica o estado dessas chaves.</span><span class="sxs-lookup"><span data-stu-id="c53da-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="c53da-119">Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.</span><span class="sxs-lookup"><span data-stu-id="c53da-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span>

</dd> <dt>

<span data-ttu-id="c53da-120">*Efeito*</span><span class="sxs-lookup"><span data-stu-id="c53da-120">*fX*</span></span> 
</dt> <dd>

<span data-ttu-id="c53da-121">**Número** (**longo**) que especifica a coordenada x do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="c53da-121">**Number** (**long**) specifying the x coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> <dt>

<span data-ttu-id="c53da-122">*SAR*</span><span class="sxs-lookup"><span data-stu-id="c53da-122">*fY*</span></span> 
</dt> <dd>

<span data-ttu-id="c53da-123">**Número** (**longo**) que especifica a coordenada y do ponteiro do mouse em relação ao canto superior esquerdo do controle.</span><span class="sxs-lookup"><span data-stu-id="c53da-123">**Number** (**long**) specifying the y coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c53da-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c53da-124">Return value</span></span>

<span data-ttu-id="c53da-125">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c53da-125">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c53da-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c53da-126">Remarks</span></span>

<span data-ttu-id="c53da-127">O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido.</span><span class="sxs-lookup"><span data-stu-id="c53da-127">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="c53da-128">Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.</span><span class="sxs-lookup"><span data-stu-id="c53da-128">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="c53da-129">**Windows Media Player 10 Mobile:** Não há suporte para esse evento.</span><span class="sxs-lookup"><span data-stu-id="c53da-129">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="c53da-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c53da-130">Requirements</span></span>



| <span data-ttu-id="c53da-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c53da-131">Requirement</span></span> | <span data-ttu-id="c53da-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c53da-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c53da-133">Versão</span><span class="sxs-lookup"><span data-stu-id="c53da-133">Version</span></span><br/> | <span data-ttu-id="c53da-134">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c53da-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c53da-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c53da-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="c53da-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c53da-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c53da-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c53da-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c53da-138">**Objeto de jogador**</span><span class="sxs-lookup"><span data-stu-id="c53da-138">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





