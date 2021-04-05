---
title: WM_TOUCHHITTESTING mensagem
description: Enviado a uma janela em um toque para determinar o destino de toque mais provável.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- Mensagens de entrada e notificações de WM_TOUCHHITTESTING mensagem
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085848"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="d18f8-104">WM_TOUCHHITTESTING mensagem</span><span class="sxs-lookup"><span data-stu-id="d18f8-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="d18f8-105">Enviado a uma janela em um toque para determinar o destino de toque mais provável.</span><span class="sxs-lookup"><span data-stu-id="d18f8-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="d18f8-106">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="d18f8-106">\[!Important\]</span></span>  
> <span data-ttu-id="d18f8-107">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="d18f8-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="d18f8-108">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="d18f8-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="d18f8-109">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="d18f8-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="d18f8-110">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d18f8-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="d18f8-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d18f8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d18f8-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d18f8-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d18f8-113">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d18f8-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="d18f8-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d18f8-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d18f8-115">Ponteiro para a estrutura de [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) que contém os dados da área de contato de toque.</span><span class="sxs-lookup"><span data-stu-id="d18f8-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d18f8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d18f8-116">Return value</span></span>

<span data-ttu-id="d18f8-117">Se um ou mais elementos estiverem dentro da área de contato de toque, um aplicativo deverá retornar o resultado de [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span><span class="sxs-lookup"><span data-stu-id="d18f8-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="d18f8-118">Se nenhum elemento estiver dentro da área de contato de toque, um aplicativo deverá definir o valor de **Score** em [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) para [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) e chamar [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) para obter o valor de retorno de LRESULT.</span><span class="sxs-lookup"><span data-stu-id="d18f8-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="d18f8-119">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="d18f8-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="d18f8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d18f8-120">Remarks</span></span>

<span data-ttu-id="d18f8-121">Essa mensagem é enviada ao Windows que se registra através da função [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="d18f8-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d18f8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d18f8-122">Requirements</span></span>



| <span data-ttu-id="d18f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18f8-123">Requirement</span></span> | <span data-ttu-id="d18f8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d18f8-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18f8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d18f8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d18f8-126">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d18f8-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d18f8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d18f8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d18f8-128">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d18f8-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d18f8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d18f8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d18f8-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d18f8-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18f8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d18f8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18f8-132">Mensagens</span><span class="sxs-lookup"><span data-stu-id="d18f8-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="d18f8-133">**Pontuações de teste de colisão de toque**</span><span class="sxs-lookup"><span data-stu-id="d18f8-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

