---
title: Mensagem de ICM_DRAW_STOP (VFW. h)
description: A \_ mensagem de parada de desenho ICM \_ Notifica um driver de renderização para interromper seu relógio interno durante o período de desenho de quadros. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_STOP
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454989"
---
# <a name="icm_draw_stop-message"></a><span data-ttu-id="026a2-105">Mensagem de parada de \_ desenho ICM \_</span><span class="sxs-lookup"><span data-stu-id="026a2-105">ICM\_DRAW\_STOP message</span></span>

<span data-ttu-id="026a2-106">A mensagem de **\_ \_ parada de desenho ICM** notifica um driver de renderização para interromper seu relógio interno durante o período de desenho de quadros.</span><span class="sxs-lookup"><span data-stu-id="026a2-106">The **ICM\_DRAW\_STOP** message notifies a rendering driver to stop its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="026a2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .</span><span class="sxs-lookup"><span data-stu-id="026a2-107">You can send this message explicitly or by using the [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) macro.</span></span>


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="026a2-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="026a2-108">Return Value</span></span>

<span data-ttu-id="026a2-109">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="026a2-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="026a2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="026a2-110">Remarks</span></span>

<span data-ttu-id="026a2-111">Essa mensagem é usada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.</span><span class="sxs-lookup"><span data-stu-id="026a2-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="026a2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="026a2-112">Requirements</span></span>



| <span data-ttu-id="026a2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="026a2-113">Requirement</span></span> | <span data-ttu-id="026a2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="026a2-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="026a2-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="026a2-115">Minimum supported client</span></span><br/> | <span data-ttu-id="026a2-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="026a2-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="026a2-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="026a2-117">Minimum supported server</span></span><br/> | <span data-ttu-id="026a2-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="026a2-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="026a2-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="026a2-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="026a2-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="026a2-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="026a2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="026a2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="026a2-122">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="026a2-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="026a2-123">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="026a2-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





