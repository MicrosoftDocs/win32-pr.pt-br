---
title: Mensagem de ICM_DECOMPRESSEX (VFW. h)
description: A \_ mensagem ICM DECOMPRESSEX notifica um driver de compactação de vídeo para descompactar um quadro de dados diretamente na tela, descompactar para um DIB de cabeça para baixo ou descompactar imagens descritas com retângulos de origem e de destino.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009637"
---
# <a name="icm_decompressex-message"></a><span data-ttu-id="54197-104">\_Mensagem DECOMPRESSEX de ICM</span><span class="sxs-lookup"><span data-stu-id="54197-104">ICM\_DECOMPRESSEX message</span></span>

<span data-ttu-id="54197-105">A mensagem **ICM \_ DECOMPRESSEX** notifica um driver de compactação de vídeo para descompactar um quadro de dados diretamente na tela, descompactar para um DIB de cabeça para baixo ou descompactar imagens descritas com retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="54197-105">The **ICM\_DECOMPRESSEX** message notifies a video compression driver to decompress a frame of data directly to the screen, decompress to an upside-down DIB, or decompress images described with source and destination rectangles.</span></span>


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="54197-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54197-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54197-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="54197-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="54197-108">Ponteiro para uma estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .</span><span class="sxs-lookup"><span data-stu-id="54197-108">Pointer to an [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54197-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="54197-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="54197-110">Tamanho, em bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="54197-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54197-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="54197-111">Return Value</span></span>

<span data-ttu-id="54197-112">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="54197-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="54197-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="54197-113">Remarks</span></span>

<span data-ttu-id="54197-114">Essa mensagem é semelhante à [**\_ descompactação de ICM**](icm-decompress.md) , exceto pelo fato de que ela usa a estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) para definir suas informações de descompactação.</span><span class="sxs-lookup"><span data-stu-id="54197-114">This message is similar to [**ICM\_DECOMPRESS**](icm-decompress.md) except that it uses the [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure to define its decompression information.</span></span>

<span data-ttu-id="54197-115">Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem [**ICM \_ draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="54197-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="54197-116">O driver retornará um erro se essa mensagem for recebida antes da mensagem de [**\_ \_ início de DECOMPRESSEX do ICM**](icm-decompressex-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="54197-116">The driver returns an error if this message is received before the [**ICM\_DECOMPRESSEX\_BEGIN**](icm-decompressex-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="54197-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54197-117">Requirements</span></span>



| <span data-ttu-id="54197-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54197-118">Requirement</span></span> | <span data-ttu-id="54197-119">Valor</span><span class="sxs-lookup"><span data-stu-id="54197-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="54197-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54197-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54197-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54197-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="54197-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54197-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54197-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="54197-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="54197-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="54197-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54197-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="54197-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54197-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="54197-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54197-127">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="54197-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="54197-128">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="54197-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





