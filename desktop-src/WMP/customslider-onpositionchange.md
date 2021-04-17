---
title: CUSTOMSLIDER.onPositionChange
description: O manipulador de eventos onPositionChange manipula um evento que ocorre quando a posição do controle deslizante é alterada como resultado do usuário clicar ou arrastar. | CUSTOMSLIDER.onPositionChange
ms.assetid: d8fe99a2-69ff-4e75-8d7d-506bcb2f75bf
keywords:
- CUSTOMSLIDER. onPositionChange Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3d5547d66ca6dc1b770242301bd95ed010a8d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780016"
---
# <a name="customslideronpositionchange"></a><span data-ttu-id="cf654-105">CUSTOMSLIDER.onPositionChange</span><span class="sxs-lookup"><span data-stu-id="cf654-105">CUSTOMSLIDER.onPositionChange</span></span>

<span data-ttu-id="cf654-106">O manipulador de eventos **onPositionChange** manipula um evento que ocorre quando a posição do controle deslizante é alterada como resultado do usuário clicar ou arrastar.</span><span class="sxs-lookup"><span data-stu-id="cf654-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="cf654-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf654-107">Remarks</span></span>

<span data-ttu-id="cf654-108">Se a posição do controle deslizante personalizado for alterada como resultado do atributo de **valor** que está sendo modificado no script, esse evento não será acionado.</span><span class="sxs-lookup"><span data-stu-id="cf654-108">If the position of the custom slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="cf654-109">Para acomodar essa possibilidade, implemente o valor do manipulador de eventos **\_ onChange** .</span><span class="sxs-lookup"><span data-stu-id="cf654-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf654-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf654-110">Requirements</span></span>



| <span data-ttu-id="cf654-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf654-111">Requirement</span></span> | <span data-ttu-id="cf654-112">Valor</span><span class="sxs-lookup"><span data-stu-id="cf654-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cf654-113">Versão</span><span class="sxs-lookup"><span data-stu-id="cf654-113">Version</span></span><br/> | <span data-ttu-id="cf654-114">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cf654-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf654-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf654-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf654-116">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="cf654-116">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





