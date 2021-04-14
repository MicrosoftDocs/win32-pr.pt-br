---
title: Mensagem de ICM_DECOMPRESSEX_END (VFW. h)
description: A \_ mensagem ICM DECOMPRESSEX \_ end notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressExEnd.
ms.assetid: 7ed63a4e-bb17-43a3-b593-25c4a51be942
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX_END
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e96f6a069e9ed2c9c52dc2f07f1ab4c5210ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499662"
---
# <a name="icm_decompressex_end-message"></a><span data-ttu-id="5bba8-105">Mensagem de final do ICM \_ DECOMPRESSEX \_</span><span class="sxs-lookup"><span data-stu-id="5bba8-105">ICM\_DECOMPRESSEX\_END message</span></span>

<span data-ttu-id="5bba8-106">A mensagem **ICM \_ DECOMPRESSEX \_ end** notifica um driver de descompactação de vídeo para encerrar a descompactação e liberar recursos alocados para descompactação.</span><span class="sxs-lookup"><span data-stu-id="5bba8-106">The **ICM\_DECOMPRESSEX\_END** message notifies a video decompression driver to end decompression and free resources allocated for decompression.</span></span> <span data-ttu-id="5bba8-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) .</span><span class="sxs-lookup"><span data-stu-id="5bba8-107">You can send this message explicitly or by using the [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) macro.</span></span>


```C++
ICM_DECOMPRESSEX_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="5bba8-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5bba8-108">Return Value</span></span>

<span data-ttu-id="5bba8-109">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="5bba8-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bba8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bba8-110">Remarks</span></span>

<span data-ttu-id="5bba8-111">O driver libera todos os recursos alocados para a mensagem de [**\_ \_ início do ICM DECOMPRESSEX**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="5bba8-111">The driver frees any resources allocated for the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

<span data-ttu-id="5bba8-112">[**ICM \_ DECOMPRESSEX \_ begin**](icm-decompressex-begin.md) e **ICM \_ DECOMPRESSEX \_ end** não são aninhados.</span><span class="sxs-lookup"><span data-stu-id="5bba8-112">[**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) and **ICM\_DECOMPRESSEX\_END** do not nest.</span></span> <span data-ttu-id="5bba8-113">Se o driver receber o **ICM \_ DECOMPRESSEX \_ begin** antes da descompactação ser interrompida com o **ICM \_ DECOMPRESSEX \_ end**, ele deverá reiniciar a descompactação com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5bba8-113">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bba8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bba8-114">Requirements</span></span>



| <span data-ttu-id="5bba8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bba8-115">Requirement</span></span> | <span data-ttu-id="5bba8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5bba8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5bba8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bba8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5bba8-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5bba8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5bba8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bba8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5bba8-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5bba8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5bba8-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5bba8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bba8-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bba8-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bba8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bba8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bba8-124">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="5bba8-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5bba8-125">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="5bba8-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





