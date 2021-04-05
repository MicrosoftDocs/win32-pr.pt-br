---
title: Mensagem de MCIWNDM_SETACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM SETACTIVETIMER define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver ativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETACTIVETIMER
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085900"
---
# <a name="mciwndm_setactivetimer-message"></a><span data-ttu-id="819c3-105">\_Mensagem MCIWNDM SETACTIVETIMER</span><span class="sxs-lookup"><span data-stu-id="819c3-105">MCIWNDM\_SETACTIVETIMER message</span></span>

<span data-ttu-id="819c3-106">A mensagem **MCIWNDM \_ SETACTIVETIMER** define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="819c3-106">The **MCIWNDM\_SETACTIVETIMER** message sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active.</span></span> <span data-ttu-id="819c3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="819c3-107">You can send this message explicitly or by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span>


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="819c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="819c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="819c3-109"><span id="active"></span><span id="ACTIVE"></span>*activo*</span><span class="sxs-lookup"><span data-stu-id="819c3-109"><span id="active"></span><span id="ACTIVE"></span>*active*</span></span>
</dt> <dd>

<span data-ttu-id="819c3-110">Período de atualização, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="819c3-110">Update period, in milliseconds.</span></span> <span data-ttu-id="819c3-111">O padrão é 500 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="819c3-111">The default is 500 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="819c3-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="819c3-112">Return Value</span></span>

<span data-ttu-id="819c3-113">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="819c3-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="819c3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="819c3-114">Requirements</span></span>



| <span data-ttu-id="819c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="819c3-115">Requirement</span></span> | <span data-ttu-id="819c3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="819c3-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="819c3-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="819c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="819c3-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="819c3-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="819c3-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="819c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="819c3-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="819c3-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="819c3-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="819c3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="819c3-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="819c3-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="819c3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="819c3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819c3-124">**MCIWndSetActiveTimer**</span><span class="sxs-lookup"><span data-stu-id="819c3-124">**MCIWndSetActiveTimer**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





