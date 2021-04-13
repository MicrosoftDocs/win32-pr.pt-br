---
title: Constantes da janela de teste de colisão de toque
description: Indica como as mensagens para teste de clique de toque são processadas pelo Windows que são registradas por meio da função RegisterTouchHitTestingWindow.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369803"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="a6588-103">Constantes da janela de teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="a6588-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="a6588-104">Indica como as mensagens para teste de clique de toque são processadas pelo Windows que são registradas por meio da função [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="a6588-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="a6588-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="a6588-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="a6588-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6588-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="a6588-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a6588-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a6588-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) mensagens não são enviadas para a janela de destino, mas são enviadas para janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="a6588-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="a6588-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a6588-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="a6588-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) mensagens são enviadas para a janela de destino.</span><span class="sxs-lookup"><span data-stu-id="a6588-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="a6588-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="a6588-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="a6588-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) mensagens não são enviadas para a janela de destino ou janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="a6588-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="a6588-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6588-113">Requirements</span></span>



| <span data-ttu-id="a6588-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6588-114">Requirement</span></span> | <span data-ttu-id="a6588-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a6588-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6588-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6588-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a6588-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a6588-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a6588-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6588-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a6588-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a6588-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6588-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6588-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6588-121"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6588-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6588-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6588-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6588-123">Constantes</span><span class="sxs-lookup"><span data-stu-id="a6588-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="a6588-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="a6588-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

