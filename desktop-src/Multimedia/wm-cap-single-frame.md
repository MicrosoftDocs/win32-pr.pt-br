---
title: Mensagem de WM_CAP_SINGLE_FRAME (VFW. h)
description: A mensagem do quadro do WM \_ Cap \_ \_ anexa um único quadro a um arquivo de captura que foi aberto usando a \_ mensagem de abertura do quadro do WM Cap \_ \_ \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- Multimídia do Windows de mensagem WM_CAP_SINGLE_FRAME
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086362"
---
# <a name="wm_cap_single_frame-message"></a><span data-ttu-id="de0c7-105">\_Mensagem de \_ \_ quadro único do WM Cap</span><span class="sxs-lookup"><span data-stu-id="de0c7-105">WM\_CAP\_SINGLE\_FRAME message</span></span>

<span data-ttu-id="de0c7-106">A mensagem do **\_ \_ \_ quadro do WM Cap** anexa um único quadro a um arquivo de captura que foi aberto usando a mensagem de [**\_ \_ \_ \_ abertura do quadro do WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="de0c7-106">The **WM\_CAP\_SINGLE\_FRAME** message appends a single frame to a capture file that was opened using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="de0c7-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .</span><span class="sxs-lookup"><span data-stu-id="de0c7-107">You can send this message explicitly or by using the [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="de0c7-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="de0c7-108">Return Value</span></span>

<span data-ttu-id="de0c7-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="de0c7-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="de0c7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de0c7-110">Requirements</span></span>



| <span data-ttu-id="de0c7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="de0c7-111">Requirement</span></span> | <span data-ttu-id="de0c7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="de0c7-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="de0c7-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de0c7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="de0c7-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de0c7-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="de0c7-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de0c7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="de0c7-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de0c7-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="de0c7-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="de0c7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="de0c7-118"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="de0c7-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0c7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="de0c7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0c7-120">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="de0c7-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="de0c7-121">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="de0c7-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





