---
title: Mensagem de MCIWNDM_SETINACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM SETINACTIVETIMER define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver inativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETINACTIVETIMER
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4504d84b254dfb67616568f5f97bba8e3bc2e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499532"
---
# <a name="mciwndm_setinactivetimer-message"></a><span data-ttu-id="3ac43-105">\_Mensagem MCIWNDM SETINACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="3ac43-105">MCIWNDM\_SETINACTIVETIMER message</span></span>

<span data-ttu-id="3ac43-106">A mensagem **MCIWNDM \_ SETINACTIVETIMER** define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver inativa.</span><span class="sxs-lookup"><span data-stu-id="3ac43-106">The **MCIWNDM\_SETINACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive.</span></span> <span data-ttu-id="3ac43-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="3ac43-107">You can send this message explicitly or by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span>


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="3ac43-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ac43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac43-109"><span id="inactive"></span><span id="INACTIVE"></span>*inativo*</span><span class="sxs-lookup"><span data-stu-id="3ac43-109"><span id="inactive"></span><span id="INACTIVE"></span>*inactive*</span></span>
</dt> <dd>

<span data-ttu-id="3ac43-110">Período de atualização, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3ac43-110">Update period, in milliseconds.</span></span> <span data-ttu-id="3ac43-111">O padrão é 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3ac43-111">The default is 2000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac43-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3ac43-112">Return Value</span></span>

<span data-ttu-id="3ac43-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3ac43-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac43-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac43-114">Requirements</span></span>



| <span data-ttu-id="3ac43-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac43-115">Requirement</span></span> | <span data-ttu-id="3ac43-116">Valor</span><span class="sxs-lookup"><span data-stu-id="3ac43-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3ac43-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ac43-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac43-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ac43-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3ac43-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ac43-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac43-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ac43-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3ac43-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ac43-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac43-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac43-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ac43-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ac43-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac43-124">**MCIWndSetInactiveTimer**</span><span class="sxs-lookup"><span data-stu-id="3ac43-124">**MCIWndSetInactiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





