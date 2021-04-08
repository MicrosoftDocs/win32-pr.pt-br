---
title: Mensagem de ICM_DRAW_STOP_PLAY (VFW. h)
description: A \_ mensagem de parar reprodução do ICM Draw \_ \_ Notifica um driver de renderização quando uma operação de reprodução é concluída. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_STOP_PLAY
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086513"
---
# <a name="icm_draw_stop_play-message"></a><span data-ttu-id="96c95-105">\_Mensagem de \_ parada de \_ execução do ICM Draw</span><span class="sxs-lookup"><span data-stu-id="96c95-105">ICM\_DRAW\_STOP\_PLAY message</span></span>

<span data-ttu-id="96c95-106">A mensagem de **\_ \_ parar \_ reprodução do ICM Draw** notifica um driver de renderização quando uma operação de reprodução é concluída.</span><span class="sxs-lookup"><span data-stu-id="96c95-106">The **ICM\_DRAW\_STOP\_PLAY** message notifies a rendering driver when a play operation is complete.</span></span> <span data-ttu-id="96c95-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .</span><span class="sxs-lookup"><span data-stu-id="96c95-107">You can send this message explicitly or by using the [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) macro.</span></span>


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="96c95-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96c95-108">Return Value</span></span>

<span data-ttu-id="96c95-109">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="96c95-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96c95-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="96c95-110">Remarks</span></span>

<span data-ttu-id="96c95-111">Use esta mensagem quando a operação de reprodução for concluída.</span><span class="sxs-lookup"><span data-stu-id="96c95-111">Use this message when the play operation is complete.</span></span> <span data-ttu-id="96c95-112">Use a mensagem de [**\_ \_ parada de desenho ICM**](icm-draw-stop.md) para encerrar o tempo.</span><span class="sxs-lookup"><span data-stu-id="96c95-112">Use the [**ICM\_DRAW\_STOP**](icm-draw-stop.md) message to end timing.</span></span>

## <a name="requirements"></a><span data-ttu-id="96c95-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c95-113">Requirements</span></span>



| <span data-ttu-id="96c95-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c95-114">Requirement</span></span> | <span data-ttu-id="96c95-115">Valor</span><span class="sxs-lookup"><span data-stu-id="96c95-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96c95-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c95-116">Minimum supported client</span></span><br/> | <span data-ttu-id="96c95-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96c95-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="96c95-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96c95-118">Minimum supported server</span></span><br/> | <span data-ttu-id="96c95-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96c95-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96c95-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96c95-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c95-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c95-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c95-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="96c95-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c95-123">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="96c95-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="96c95-124">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="96c95-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





