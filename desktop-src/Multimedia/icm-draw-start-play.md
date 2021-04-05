---
title: Mensagem de ICM_DRAW_START_PLAY (VFW. h)
description: A \_ mensagem de \_ início de inicialização ICM \_ fornece as horas de início e de término de uma operação de reprodução para um driver de renderização. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_START_PLAY
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085448"
---
# <a name="icm_draw_start_play-message"></a><span data-ttu-id="d7d6d-105">\_Iniciar a \_ mensagem de início de \_ execução do ICM</span><span class="sxs-lookup"><span data-stu-id="d7d6d-105">ICM\_DRAW\_START\_PLAY message</span></span>

<span data-ttu-id="d7d6d-106">A mensagem de **\_ início de \_ inicialização \_ ICM** fornece as horas de início e de término de uma operação de reprodução para um driver de renderização.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-106">The **ICM\_DRAW\_START\_PLAY** message provides the start and end times of a play operation to a rendering driver.</span></span> <span data-ttu-id="d7d6d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .</span><span class="sxs-lookup"><span data-stu-id="d7d6d-107">You can send this message explicitly or by using the [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) macro.</span></span>


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a><span data-ttu-id="d7d6d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7d6d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d6d-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span><span class="sxs-lookup"><span data-stu-id="d7d6d-109"><span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*</span></span>
</dt> <dd>

<span data-ttu-id="d7d6d-110">Hora de início.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-110">Start time.</span></span>

</dd> <dt>

<span data-ttu-id="d7d6d-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span><span class="sxs-lookup"><span data-stu-id="d7d6d-111"><span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*</span></span>
</dt> <dd>

<span data-ttu-id="d7d6d-112">Hora de término.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-112">End time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d6d-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d7d6d-113">Return Value</span></span>

<span data-ttu-id="d7d6d-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d6d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7d6d-115">Remarks</span></span>

<span data-ttu-id="d7d6d-116">Essa mensagem precede todos os dados de quadro enviados ao driver de renderização.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-116">This message precedes any frame data sent to the rendering driver.</span></span>

<span data-ttu-id="d7d6d-117">As unidades para *lFrom* e *lTo* são especificadas com a mensagem de [**\_ \_ início de empate de ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d6d-117">Units for *lFrom* and *lTo* are specified with the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span> <span data-ttu-id="d7d6d-118">Para dados de vídeo, normalmente é um número de quadro.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-118">For video data this is normally a frame number.</span></span> <span data-ttu-id="d7d6d-119">Para obter mais informações sobre a taxa de reprodução, consulte os membros **dwRate** e **DwScale** da estrutura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .</span><span class="sxs-lookup"><span data-stu-id="d7d6d-119">For more information about the playback rate, see the **dwRate** and **dwScale** members of the [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) structure.</span></span>

<span data-ttu-id="d7d6d-120">Se a hora de término for menor que a hora de início, a direção da reprodução será invertida.</span><span class="sxs-lookup"><span data-stu-id="d7d6d-120">If the end time is less than the start time, the playback direction is reversed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d6d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7d6d-121">Requirements</span></span>



| <span data-ttu-id="d7d6d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7d6d-122">Requirement</span></span> | <span data-ttu-id="d7d6d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d7d6d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7d6d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7d6d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d6d-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7d6d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d7d6d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7d6d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d6d-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7d6d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d7d6d-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d7d6d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7d6d-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d6d-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d6d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7d6d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d6d-131">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="d7d6d-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="d7d6d-132">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="d7d6d-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





