---
title: Mensagem de MCIWNDM_SETOWNER (VFW. h)
description: A \_ mensagem MCIWNDM SetOwner define a janela para receber mensagens de notificação associadas à janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetOwner.
ms.assetid: c2d0f9d5-bf60-4036-a613-65ba1ed83110
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETOWNER
topic_type:
- apiref
api_name:
- MCIWNDM_SETOWNER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3989632e83a65cda5e805bd91da3f502ca387d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085902"
---
# <a name="mciwndm_setowner-message"></a><span data-ttu-id="ba747-105">Mensagem do MCIWNDM \_ SETowner</span><span class="sxs-lookup"><span data-stu-id="ba747-105">MCIWNDM\_SETOWNER message</span></span>

<span data-ttu-id="ba747-106">A mensagem **MCIWNDM \_ SetOwner** define a janela para receber mensagens de notificação associadas à janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ba747-106">The **MCIWNDM\_SETOWNER** message sets the window to receive notification messages associated with the MCIWnd window.</span></span> <span data-ttu-id="ba747-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) .</span><span class="sxs-lookup"><span data-stu-id="ba747-107">You can send this message explicitly or by using the [**MCIWndSetOwner**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner) macro.</span></span>


```C++
MCIWNDM_SETOWNER 
wParam = (WPARAM) hwndP; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="ba747-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba747-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba747-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span><span class="sxs-lookup"><span data-stu-id="ba747-109"><span id="hwndP"></span><span id="hwndp"></span><span id="HWNDP"></span>*hwndP*</span></span>
</dt> <dd>

<span data-ttu-id="ba747-110">Manipule a janela para receber as mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="ba747-110">Handle to the window to receive the notification messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba747-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ba747-111">Return Value</span></span>

<span data-ttu-id="ba747-112">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="ba747-112">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba747-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba747-113">Requirements</span></span>



| <span data-ttu-id="ba747-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba747-114">Requirement</span></span> | <span data-ttu-id="ba747-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ba747-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ba747-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba747-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba747-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba747-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ba747-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba747-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba747-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ba747-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ba747-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ba747-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba747-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba747-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba747-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba747-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba747-123">**MCIWndSetOwner**</span><span class="sxs-lookup"><span data-stu-id="ba747-123">**MCIWndSetOwner**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetowner)
</dt> </dl>

 

 





