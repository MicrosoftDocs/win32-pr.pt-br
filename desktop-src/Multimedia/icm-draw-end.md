---
title: Mensagem de ICM_DRAW_END (VFW. h)
description: A mensagem de final do ICM \_ draw \_ Notifica um driver de renderização para descompactar a imagem atual na tela e liberar recursos alocados para descompactação e desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_END
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644765"
---
# <a name="icm_draw_end-message"></a><span data-ttu-id="3a08f-105">Mensagem de final de \_ desenho ICM \_</span><span class="sxs-lookup"><span data-stu-id="3a08f-105">ICM\_DRAW\_END message</span></span>

<span data-ttu-id="3a08f-106">A mensagem de **\_ \_ final do ICM Draw** notifica um driver de renderização para descompactar a imagem atual na tela e liberar recursos alocados para descompactação e desenho.</span><span class="sxs-lookup"><span data-stu-id="3a08f-106">The **ICM\_DRAW\_END** message notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing.</span></span> <span data-ttu-id="3a08f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .</span><span class="sxs-lookup"><span data-stu-id="3a08f-107">You can send this message explicitly or by using the [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) macro.</span></span>


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="3a08f-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3a08f-108">Return Value</span></span>

<span data-ttu-id="3a08f-109">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3a08f-109">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a08f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a08f-110">Remarks</span></span>

<span data-ttu-id="3a08f-111">As mensagens de final [**ICM \_ draw \_ begin**](icm-draw-begin.md) e **ICM \_ draw \_** não são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="3a08f-111">The [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) and **ICM\_DRAW\_END** messages do not nest.</span></span> <span data-ttu-id="3a08f-112">Se o driver receber o **início de ICM e \_ \_ começar** antes que a descompactação seja interrompida com a **\_ \_ extremidade de desenho ICM**, ela deverá reiniciar a descompactação com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3a08f-112">If your driver receives **ICM\_DRAW\_BEGIN** before decompression is stopped with **ICM\_DRAW\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a08f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a08f-113">Requirements</span></span>



| <span data-ttu-id="3a08f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a08f-114">Requirement</span></span> | <span data-ttu-id="3a08f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3a08f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3a08f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a08f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3a08f-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a08f-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3a08f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a08f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3a08f-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a08f-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3a08f-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a08f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a08f-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a08f-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a08f-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3a08f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a08f-123">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="3a08f-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="3a08f-124">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="3a08f-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





