---
title: WM_POINTERDEVICEOUTOFRANGE mensagem
description: Enviado a uma janela quando um dispositivo ponteiro tiver desem parte o intervalo de um digitalizador de entrada. Esta mensagem contém informações sobre o dispositivo e sua proximidade.
ms.assetid: 6BC667C1-6D9A-4E69-BAC6-761A1859F09E
keywords:
- Mensagens de entrada e notificações de WM_POINTERDEVICEOUTOFRANGE mensagem
topic_type:
- apiref
api_name:
- WM_POINTERDEVICEOUTOFRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: c222d9a35cae89838d7b6e1d99dcecd11f85b54d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085418"
---
# <a name="wm_pointerdeviceoutofrange-message"></a><span data-ttu-id="dae1b-105">WM_POINTERDEVICEOUTOFRANGE mensagem</span><span class="sxs-lookup"><span data-stu-id="dae1b-105">WM_POINTERDEVICEOUTOFRANGE message</span></span>

<span data-ttu-id="dae1b-106">Enviado a uma janela quando um dispositivo ponteiro tiver desem parte o intervalo de um digitalizador de entrada.</span><span class="sxs-lookup"><span data-stu-id="dae1b-106">Sent to a window when a pointer device has departed the range of an input digitizer.</span></span> <span data-ttu-id="dae1b-107">Esta mensagem contém informações sobre o dispositivo e sua proximidade.</span><span class="sxs-lookup"><span data-stu-id="dae1b-107">This message contains information regarding the device and its proximity.</span></span>

> <span data-ttu-id="dae1b-108">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="dae1b-108">\[!Important\]</span></span>  
> <span data-ttu-id="dae1b-109">Os aplicativos da área de trabalho devem ter reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="dae1b-109">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="dae1b-110">Se seu aplicativo não tiver reconhecimento de DPI, as coordenadas de tela contidas nas mensagens de ponteiro e estruturas relacionadas poderão parecer imprecisas devido à virtualização de DPI.</span><span class="sxs-lookup"><span data-stu-id="dae1b-110">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="dae1b-111">A virtualização de DPI fornece suporte de dimensionamento automático para aplicativos que não têm reconhecimento de DPI e está ativo por padrão (os usuários podem desativá-lo).</span><span class="sxs-lookup"><span data-stu-id="dae1b-111">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="dae1b-112">Para obter mais informações, consulte [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dae1b-112">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERDEVICEOUTOFRANGE       0X23A
```



## <a name="parameters"></a><span data-ttu-id="dae1b-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dae1b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae1b-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dae1b-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dae1b-115">Obter informações adicionais específicas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="dae1b-115">Additional message-specific information.</span></span>

</dd> <dt>

<span data-ttu-id="dae1b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dae1b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dae1b-117">Obter informações adicionais específicas de mensagem.</span><span class="sxs-lookup"><span data-stu-id="dae1b-117">Additional message-specific information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae1b-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dae1b-118">Return value</span></span>

<span data-ttu-id="dae1b-119">Se o aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="dae1b-119">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="dae1b-120">Se o aplicativo não processar essa mensagem, ele deverá chamar [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="dae1b-120">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="requirements"></a><span data-ttu-id="dae1b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae1b-121">Requirements</span></span>



| <span data-ttu-id="dae1b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae1b-122">Requirement</span></span> | <span data-ttu-id="dae1b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dae1b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae1b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dae1b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dae1b-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dae1b-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="dae1b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dae1b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dae1b-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dae1b-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dae1b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dae1b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dae1b-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dae1b-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae1b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae1b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae1b-131">Mensagens</span><span class="sxs-lookup"><span data-stu-id="dae1b-131">Messages</span></span>](messages.md)
</dt> </dl>

 

