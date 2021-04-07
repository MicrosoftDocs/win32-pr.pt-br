---
title: Mensagem de ICM_DRAW_RENDERBUFFER (VFW. h)
description: A \_ mensagem ICM Draw \_ RENDERBUFFER notifica um driver de renderização para desenhar os quadros que foram passados para ele. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_RENDERBUFFER
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918916"
---
# <a name="icm_draw_renderbuffer-message"></a><span data-ttu-id="ce31b-105">\_Mensagem de desenho RENDERBUFFER de ICM \_</span><span class="sxs-lookup"><span data-stu-id="ce31b-105">ICM\_DRAW\_RENDERBUFFER message</span></span>

<span data-ttu-id="ce31b-106">A mensagem **ICM \_ draw \_ RENDERBUFFER** notifica um driver de renderização para desenhar os quadros que foram passados para ele.</span><span class="sxs-lookup"><span data-stu-id="ce31b-106">The **ICM\_DRAW\_RENDERBUFFER** message notifies a rendering driver to draw the frames that have been passed to it.</span></span> <span data-ttu-id="ce31b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ce31b-107">You can send this message explicitly or by using the [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) macro.</span></span>


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ce31b-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ce31b-108">Return Value</span></span>

<span data-ttu-id="ce31b-109">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ce31b-109">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce31b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce31b-110">Remarks</span></span>

<span data-ttu-id="ce31b-111">Use essa mensagem com hardware que executa sua própria descompactação assíncrona, tempo e desenho.</span><span class="sxs-lookup"><span data-stu-id="ce31b-111">Use this message with hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="ce31b-112">Essa mensagem é normalmente usada para executar uma operação de busca quando o driver deve ser especificamente instruído para exibir cada quadro de vídeo passado para ele, em vez de reproduzir uma sequência de quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ce31b-112">This message is typically used to perform a seek operation when the driver must be specifically instructed to display each video frame passed to it rather than playing a sequence of video frames.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce31b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce31b-113">Requirements</span></span>



| <span data-ttu-id="ce31b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce31b-114">Requirement</span></span> | <span data-ttu-id="ce31b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ce31b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ce31b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce31b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce31b-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ce31b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ce31b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce31b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce31b-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ce31b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce31b-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ce31b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce31b-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce31b-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce31b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce31b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce31b-123">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ce31b-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ce31b-124">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="ce31b-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





