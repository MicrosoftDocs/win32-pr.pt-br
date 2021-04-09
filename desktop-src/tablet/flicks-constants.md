---
description: A seguir estão as constantes de movimentos.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Constantes de movimentos (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090564"
---
# <a name="flicks-constants"></a><span data-ttu-id="88e57-103">Constantes de movimentos</span><span class="sxs-lookup"><span data-stu-id="88e57-103">Flicks Constants</span></span>

<span data-ttu-id="88e57-104">A seguir estão as constantes de movimentos.</span><span class="sxs-lookup"><span data-stu-id="88e57-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="88e57-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="88e57-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="88e57-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="88e57-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="88e57-107"><dt>**Movimento \_ O WM \_ tratou a \_ máscara**</dt> <dt>0x1</dt></span><span class="sxs-lookup"><span data-stu-id="88e57-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="88e57-108">O valor a ser retornado após a manipulação da mensagem de [**\_ mensagem de \_ movimento do WM Tablet**](wm-tablet-flick-message.md) .</span><span class="sxs-lookup"><span data-stu-id="88e57-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="88e57-109">Se **a \_ \_ \_ máscara manipulada do WM em movimento** for retornada, nenhuma ação adicional ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="88e57-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="88e57-110">Caso contrário, o Windows envia notificações de acompanhamento, como o [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), o [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)ou o [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown), dependendo de qual ação está associada ao movimento da caneta.</span><span class="sxs-lookup"><span data-stu-id="88e57-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="88e57-111"><dt>**Número \_ de \_Direções de movimento**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="88e57-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="88e57-112">O número de direções definidas na enumeração [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .</span><span class="sxs-lookup"><span data-stu-id="88e57-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="88e57-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88e57-113">Requirements</span></span>



| <span data-ttu-id="88e57-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e57-114">Requirement</span></span> | <span data-ttu-id="88e57-115">Valor</span><span class="sxs-lookup"><span data-stu-id="88e57-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88e57-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e57-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88e57-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="88e57-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="88e57-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88e57-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88e57-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="88e57-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="88e57-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88e57-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="88e57-121"><dt>Tabflicks. h</dt></span><span class="sxs-lookup"><span data-stu-id="88e57-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e57-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="88e57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e57-123">**Enumeração FLICKDIRECTION**</span><span class="sxs-lookup"><span data-stu-id="88e57-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="88e57-124">**Mensagem de movimento do \_ Tablet do WM \_**</span><span class="sxs-lookup"><span data-stu-id="88e57-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="88e57-125">Gestos de movimentos</span><span class="sxs-lookup"><span data-stu-id="88e57-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="88e57-126">[Respondendo a movimentos de caneta](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="88e57-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

