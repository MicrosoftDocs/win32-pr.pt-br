---
title: Mensagem de ICM_DECOMPRESS_END (VFW. h)
description: A \_ mensagem de término de DEScompactação ICM \_ Notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressEnd.
ms.assetid: 16ce2424-9606-455f-afbd-84326457538e
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_END
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e25155755b6bfbb893905e6facad890dbf98f175
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645017"
---
# <a name="icm_decompress_end-message"></a><span data-ttu-id="8fde9-105">\_Mensagem de final de DEScompactação ICM \_</span><span class="sxs-lookup"><span data-stu-id="8fde9-105">ICM\_DECOMPRESS\_END message</span></span>

<span data-ttu-id="8fde9-106">A mensagem de **\_ \_ término de descompactação ICM** notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação.</span><span class="sxs-lookup"><span data-stu-id="8fde9-106">The **ICM\_DECOMPRESS\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="8fde9-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) .</span><span class="sxs-lookup"><span data-stu-id="8fde9-107">You can send this message explicitly or by using the [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend) macro.</span></span>


```C++
ICM_DECOMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="8fde9-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="8fde9-108">Return Value</span></span>

<span data-ttu-id="8fde9-109">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8fde9-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fde9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fde9-110">Remarks</span></span>

<span data-ttu-id="8fde9-111">O driver deve liberar todos os recursos alocados para a mensagem de [**\_ \_ início de descompactação do ICM**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="8fde9-111">The driver should free any resources allocated for the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="8fde9-112">[**ICM \_ Descompactar \_ início**](icm-decompress-begin.md) e **\_ descompactação \_ de ICM** não aninhe.</span><span class="sxs-lookup"><span data-stu-id="8fde9-112">[**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) and **ICM\_DECOMPRESS\_END** do not nest.</span></span> <span data-ttu-id="8fde9-113">Se o driver receber **a \_ descompactação ICM \_ começar** antes que a descompactação seja interrompida com o **\_ \_ ponto de descompactação ICM**, ela deverá reiniciar a descompactação com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8fde9-113">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fde9-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fde9-114">Requirements</span></span>



| <span data-ttu-id="8fde9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fde9-115">Requirement</span></span> | <span data-ttu-id="8fde9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8fde9-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8fde9-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fde9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8fde9-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fde9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8fde9-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fde9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8fde9-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fde9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8fde9-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8fde9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fde9-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fde9-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fde9-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8fde9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fde9-124">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="8fde9-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8fde9-125">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="8fde9-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





