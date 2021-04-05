---
title: Mensagem de ICM_GETBUFFERSWANTED (VFW. h)
description: A \_ mensagem ICM GETBUFFERSWANTED consulta um driver para o número de buffers a serem alocados. Você pode enviar essa mensagem explicitamente ou usando a macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- Multimídia do Windows de mensagem ICM_GETBUFFERSWANTED
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918110"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="7af03-105">\_Mensagem GETBUFFERSWANTED de ICM</span><span class="sxs-lookup"><span data-stu-id="7af03-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="7af03-106">A mensagem **ICM \_ GETBUFFERSWANTED** consulta um driver para o número de buffers a serem alocados.</span><span class="sxs-lookup"><span data-stu-id="7af03-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="7af03-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .</span><span class="sxs-lookup"><span data-stu-id="7af03-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="7af03-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7af03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af03-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span><span class="sxs-lookup"><span data-stu-id="7af03-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="7af03-110">Endereço para conter o número de amostras que o driver precisa para renderizar os dados com eficiência.</span><span class="sxs-lookup"><span data-stu-id="7af03-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af03-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7af03-111">Return Value</span></span>

<span data-ttu-id="7af03-112">Retorna ICERR \_ OK se o êxito ou o ICERR \_ não tiver suporte de outra forma.</span><span class="sxs-lookup"><span data-stu-id="7af03-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af03-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7af03-113">Remarks</span></span>

<span data-ttu-id="7af03-114">Essa mensagem é usada por drivers que usam o hardware para renderizar dados e para garantir um intervalo de tempo mínimo causado pela espera pela chegada de buffers.</span><span class="sxs-lookup"><span data-stu-id="7af03-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="7af03-115">Por exemplo, se um driver controla uma placa de descompactação de vídeo que pode conter 10 quadros de vídeo, ele poderia retornar 10 para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="7af03-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="7af03-116">Isso instrui os aplicativos a tentar manter 10 quadros à frente do quadro que ele precisa atualmente.</span><span class="sxs-lookup"><span data-stu-id="7af03-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af03-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7af03-117">Requirements</span></span>



| <span data-ttu-id="7af03-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af03-118">Requirement</span></span> | <span data-ttu-id="7af03-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7af03-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7af03-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7af03-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7af03-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7af03-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7af03-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7af03-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7af03-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7af03-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7af03-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7af03-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7af03-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7af03-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af03-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="7af03-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af03-127">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="7af03-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="7af03-128">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="7af03-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





