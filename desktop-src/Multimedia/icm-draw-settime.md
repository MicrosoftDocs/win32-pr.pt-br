---
title: Mensagem de ICM_DRAW_SETTIME (VFW. h)
description: O ICM \_ desenha \_ setTime fornece informações de sincronização para um driver de renderização que manipula a temporização de quadros de desenho.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_SETTIME
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824324"
---
# <a name="icm_draw_settime-message"></a><span data-ttu-id="6a803-104">\_ \_ Mensagem setTime do ICM Draw</span><span class="sxs-lookup"><span data-stu-id="6a803-104">ICM\_DRAW\_SETTIME message</span></span>

<span data-ttu-id="6a803-105">O **ICM \_ desenha \_ setTime** fornece informações de sincronização para um driver de renderização que manipula a temporização de quadros de desenho.</span><span class="sxs-lookup"><span data-stu-id="6a803-105">The **ICM\_DRAW\_SETTIME** provides synchronization information to a rendering driver that handles the timing of drawing frames.</span></span> <span data-ttu-id="6a803-106">As informações de sincronização são o número de exemplo do quadro a ser desenhado.</span><span class="sxs-lookup"><span data-stu-id="6a803-106">The synchronization information is the sample number of the frame to draw.</span></span> <span data-ttu-id="6a803-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .</span><span class="sxs-lookup"><span data-stu-id="6a803-107">You can send this message explicitly or by using the [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) macro.</span></span>


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="6a803-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a803-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a803-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span><span class="sxs-lookup"><span data-stu-id="6a803-109"><span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*</span></span>
</dt> <dd>

<span data-ttu-id="6a803-110">Número de exemplo do quadro a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="6a803-110">Sample number of the frame to render.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a803-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6a803-111">Return Value</span></span>

<span data-ttu-id="6a803-112">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="6a803-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a803-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a803-113">Remarks</span></span>

<span data-ttu-id="6a803-114">Normalmente, o driver compara o valor especificado com o número de quadro associado à hora de seu relógio interno e tenta sincronizar os dois se a diferença for significativa.</span><span class="sxs-lookup"><span data-stu-id="6a803-114">Typically, the driver compares the specified value with the frame number associated with the time of its internal clock and attempts to synchronize the two if the difference is significant.</span></span>

<span data-ttu-id="6a803-115">Use essa mensagem quando o hardware executar sua própria descompactação assíncrona, tempo e desenho, e o hardware depender de um sinal de sincronização externo (o hardware não está sendo usado como o mestre de sincronização).</span><span class="sxs-lookup"><span data-stu-id="6a803-115">Use this message when the hardware performs its own asynchronous decompression, timing, and drawing, and the hardware relies on an external synchronization signal (the hardware is not being used as the synchronization master).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a803-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a803-116">Requirements</span></span>



| <span data-ttu-id="6a803-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a803-117">Requirement</span></span> | <span data-ttu-id="6a803-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6a803-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6a803-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a803-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6a803-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a803-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6a803-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a803-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6a803-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6a803-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6a803-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6a803-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a803-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a803-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a803-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a803-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a803-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="6a803-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="6a803-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="6a803-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





