---
title: Mensagem de ICM_COMPRESS_END (VFW. h)
description: A \_ mensagem de final de compactação ICM \_ Notifica um driver de compactação de vídeo para encerrar a compactação e liberar recursos alocados para compactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressEnd.
ms.assetid: 5d4b5962-c4f0-44eb-a3a9-36026f167a5a
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_END
topic_type:
- apiref
api_name:
- ICM_COMPRESS_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320cc99ed4223b7919b85d2b39e15d4d9b76aa90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454910"
---
# <a name="icm_compress_end-message"></a><span data-ttu-id="c3ea5-105">\_Mensagem de final de compactação ICM \_</span><span class="sxs-lookup"><span data-stu-id="c3ea5-105">ICM\_COMPRESS\_END message</span></span>

<span data-ttu-id="c3ea5-106">A mensagem de **\_ \_ final de compactação ICM** notifica um driver de compactação de vídeo para encerrar a compactação e liberar recursos alocados para compactação.</span><span class="sxs-lookup"><span data-stu-id="c3ea5-106">The **ICM\_COMPRESS\_END** message notifies a video compression driver to end compression and free resources allocated for compression.</span></span> <span data-ttu-id="c3ea5-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) .</span><span class="sxs-lookup"><span data-stu-id="c3ea5-107">You can send this message explicitly or by using the [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) macro.</span></span>


```C++
ICM_COMPRESS_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="c3ea5-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c3ea5-108">Return Value</span></span>

<span data-ttu-id="c3ea5-109">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="c3ea5-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3ea5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3ea5-110">Remarks</span></span>

<span data-ttu-id="c3ea5-111">VCM salva as configurações da mensagem de [**\_ \_ início de compactação ICM**](icm-compress-begin.md) mais recente.</span><span class="sxs-lookup"><span data-stu-id="c3ea5-111">VCM saves the settings of the most recent [**ICM\_COMPRESS\_BEGIN**](icm-compress-begin.md) message.</span></span> <span data-ttu-id="c3ea5-112">**ICM \_ COMPACTar \_ begin** e **ICM \_ compactar \_ fim** não aninhar.</span><span class="sxs-lookup"><span data-stu-id="c3ea5-112">**ICM\_COMPRESS\_BEGIN** and **ICM\_COMPRESS\_END** do not nest.</span></span> <span data-ttu-id="c3ea5-113">Se o driver receber **a \_ compactação de ICM, \_ comece** antes que a compactação seja interrompida com a **\_ \_ extremidade de compactação ICM**, ela deverá reiniciar a compactação com novos parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3ea5-113">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ea5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ea5-114">Requirements</span></span>



| <span data-ttu-id="c3ea5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ea5-115">Requirement</span></span> | <span data-ttu-id="c3ea5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3ea5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c3ea5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3ea5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ea5-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3ea5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c3ea5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3ea5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ea5-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c3ea5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c3ea5-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c3ea5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3ea5-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ea5-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ea5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3ea5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ea5-124">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="c3ea5-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="c3ea5-125">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="c3ea5-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





