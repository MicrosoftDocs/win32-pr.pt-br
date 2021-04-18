---
title: WM_POINTERDEVICECHANGE mensagem
description: Enviado a uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ele. Esta mensagem contém informações sobre o dimensionamento do modo de exibição.
ms.assetid: 9ED01D4C-58B4-4A21-B510-784281F9A909
keywords:
- Mensagens de entrada e notificações de WM_POINTERDEVICECHANGE mensagem
topic_type:
- apiref
api_name:
- WM_POINTERDEVICECHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 38f570059f374f64e393e960a8458e605983d6c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794016"
---
# <a name="wm_pointerdevicechange-message"></a><span data-ttu-id="66083-105">WM_POINTERDEVICECHANGE mensagem</span><span class="sxs-lookup"><span data-stu-id="66083-105">WM_POINTERDEVICECHANGE message</span></span>

<span data-ttu-id="66083-106">Enviado a uma janela quando há uma alteração nas configurações de um monitor que tem um digitalizador anexado a ele.</span><span class="sxs-lookup"><span data-stu-id="66083-106">Sent to a window when there is a change in the settings of a monitor that has a digitizer attached to it.</span></span> <span data-ttu-id="66083-107">Esta mensagem contém informações sobre o dimensionamento do modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="66083-107">This message contains information regarding the scaling of the display mode.</span></span>

> <span data-ttu-id="66083-108">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="66083-108">\[!Important\]</span></span>  
> <span data-ttu-id="66083-109">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="66083-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="66083-110">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="66083-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="66083-111">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="66083-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="66083-112">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="66083-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICECHANGE       0X238
```



## <a name="parameters"></a><span data-ttu-id="66083-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66083-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66083-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66083-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66083-115">Contém um valor das [**constantes de alteração de dispositivo ponteiro**](pointer-device-change-constants.md).</span><span class="sxs-lookup"><span data-stu-id="66083-115">Contains a value from [**Pointer Device Change Constants**](pointer-device-change-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="66083-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66083-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66083-117">Obter informações adicionais específicas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="66083-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66083-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66083-118">Return value</span></span>

<span data-ttu-id="66083-119">Se o aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="66083-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="66083-120">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="66083-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="66083-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66083-121">Requirements</span></span>



| <span data-ttu-id="66083-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66083-122">Requirement</span></span> | <span data-ttu-id="66083-123">Valor</span><span class="sxs-lookup"><span data-stu-id="66083-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66083-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66083-124">Minimum supported client</span></span><br/> | <span data-ttu-id="66083-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="66083-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="66083-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="66083-126">Minimum supported server</span></span><br/> | <span data-ttu-id="66083-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="66083-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66083-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66083-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="66083-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66083-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66083-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="66083-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66083-131">Mensagens</span><span class="sxs-lookup"><span data-stu-id="66083-131">Messages</span></span>](messages.md)
</dt> </dl>

 

