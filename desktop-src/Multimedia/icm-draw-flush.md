---
title: Mensagem de ICM_DRAW_FLUSH (VFW. h)
description: A \_ mensagem de liberação de desenho ICM \_ Notifica um driver de renderização para renderizar o conteúdo de quaisquer buffers de imagem que estão aguardando para serem desenhados. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_FLUSH
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758751"
---
# <a name="icm_draw_flush-message"></a><span data-ttu-id="950b3-105">Mensagem de liberação de \_ desenho ICM \_</span><span class="sxs-lookup"><span data-stu-id="950b3-105">ICM\_DRAW\_FLUSH message</span></span>

<span data-ttu-id="950b3-106">A mensagem de **\_ \_ liberação de desenho ICM** notifica um driver de renderização para renderizar o conteúdo de quaisquer buffers de imagem que estão aguardando para serem desenhados.</span><span class="sxs-lookup"><span data-stu-id="950b3-106">The **ICM\_DRAW\_FLUSH** message notifies a rendering driver to render the contents of any image buffers that are waiting to be drawn.</span></span> <span data-ttu-id="950b3-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .</span><span class="sxs-lookup"><span data-stu-id="950b3-107">You can send this message explicitly or by using the [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) macro.</span></span>


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="950b3-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="950b3-108">Return Value</span></span>

<span data-ttu-id="950b3-109">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="950b3-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="950b3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="950b3-110">Remarks</span></span>

<span data-ttu-id="950b3-111">Essa mensagem é usada somente por hardware que executa sua própria descompactação assíncrona, tempo e desenho.</span><span class="sxs-lookup"><span data-stu-id="950b3-111">This message is used only by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="950b3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="950b3-112">Requirements</span></span>



| <span data-ttu-id="950b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="950b3-113">Requirement</span></span> | <span data-ttu-id="950b3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="950b3-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="950b3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="950b3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="950b3-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="950b3-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="950b3-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="950b3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="950b3-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="950b3-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="950b3-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="950b3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="950b3-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="950b3-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="950b3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="950b3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950b3-122">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="950b3-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="950b3-123">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="950b3-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





