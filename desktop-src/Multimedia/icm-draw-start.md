---
title: Mensagem de ICM_DRAW_START (VFW. h)
description: A mensagem de início do ICM \_ draw \_ Notifica um driver de renderização para iniciar seu relógio interno durante o tempo dos quadros de desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_START
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369528"
---
# <a name="icm_draw_start-message"></a><span data-ttu-id="b5a10-105">Mensagem de início do ICM \_ draw \_</span><span class="sxs-lookup"><span data-stu-id="b5a10-105">ICM\_DRAW\_START message</span></span>

<span data-ttu-id="b5a10-106">A mensagem de **\_ \_ início do ICM Draw** notifica um driver de renderização para iniciar seu relógio interno durante o tempo dos quadros de desenho.</span><span class="sxs-lookup"><span data-stu-id="b5a10-106">The **ICM\_DRAW\_START** message notifies a rendering driver to start its internal clock for the timing of drawing frames.</span></span> <span data-ttu-id="b5a10-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .</span><span class="sxs-lookup"><span data-stu-id="b5a10-107">You can send this message explicitly or by using the [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) macro.</span></span>


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b5a10-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b5a10-108">Return Value</span></span>

<span data-ttu-id="b5a10-109">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b5a10-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5a10-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5a10-110">Remarks</span></span>

<span data-ttu-id="b5a10-111">Essa mensagem é usada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.</span><span class="sxs-lookup"><span data-stu-id="b5a10-111">This message is used by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="b5a10-112">Quando o driver recebe essa mensagem, ele deve iniciar a renderização de dados na taxa especificada com a mensagem de [**\_ \_ início de empate de ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="b5a10-112">When the driver receives this message, it should start rendering data at the rate specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="b5a10-113">As mensagens de parada do **ICM \_ trace \_ Start** e [**ICM \_ draw \_**](icm-draw-stop.md) não são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="b5a10-113">The **ICM\_DRAW\_START** and [**ICM\_DRAW\_STOP**](icm-draw-stop.md) messages do not nest.</span></span> <span data-ttu-id="b5a10-114">Se o seu driver receber o **início de ICM e \_ \_ Iniciar** antes que a renderização seja interrompida com a **\_ \_ parada de desenho ICM**, ela deverá reiniciar a renderização com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b5a10-114">If your driver receives **ICM\_DRAW\_START** before rendering is stopped with **ICM\_DRAW\_STOP**, it should restart rendering with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5a10-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5a10-115">Requirements</span></span>



| <span data-ttu-id="b5a10-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5a10-116">Requirement</span></span> | <span data-ttu-id="b5a10-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b5a10-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b5a10-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5a10-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b5a10-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5a10-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b5a10-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5a10-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b5a10-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5a10-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b5a10-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b5a10-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5a10-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5a10-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5a10-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5a10-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5a10-125">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="b5a10-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b5a10-126">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="b5a10-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





