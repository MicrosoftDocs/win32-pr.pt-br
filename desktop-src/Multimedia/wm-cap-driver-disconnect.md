---
title: Mensagem de WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: A \_ mensagem de desconexão do driver do WM Cap \_ \_ desconecta um driver de captura de uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_DISCONNECT
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918323"
---
# <a name="wm_cap_driver_disconnect-message"></a><span data-ttu-id="2f431-105">\_Mensagem de \_ \_ desconexão do driver do WM Cap</span><span class="sxs-lookup"><span data-stu-id="2f431-105">WM\_CAP\_DRIVER\_DISCONNECT message</span></span>

<span data-ttu-id="2f431-106">A mensagem de **\_ \_ \_ desconexão do driver do WM Cap desconecta** um driver de captura de uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="2f431-106">The **WM\_CAP\_DRIVER\_DISCONNECT** message disconnects a capture driver from a capture window.</span></span> <span data-ttu-id="2f431-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .</span><span class="sxs-lookup"><span data-stu-id="2f431-107">You can send this message explicitly or by using the [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) macro.</span></span>


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="2f431-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2f431-108">Return Value</span></span>

<span data-ttu-id="2f431-109">Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="2f431-109">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f431-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f431-110">Requirements</span></span>



| <span data-ttu-id="2f431-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f431-111">Requirement</span></span> | <span data-ttu-id="2f431-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2f431-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2f431-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f431-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2f431-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f431-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2f431-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f431-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2f431-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f431-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2f431-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f431-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f431-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f431-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f431-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f431-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f431-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2f431-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2f431-121">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="2f431-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





