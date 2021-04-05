---
title: Mensagem de ICM_DECOMPRESSEX_BEGIN (VFW. h)
description: A \_ mensagem ICM DECOMPRESSEX \_ begin notifica um driver de compactação de vídeo para se preparar para descompactar dados.
ms.assetid: 35298274-91b5-4df0-b4b0-4a71d6a49990
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESSEX_BEGIN
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ea082c91d48a9964348b762ce13631cd80af30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645013"
---
# <a name="icm_decompressex_begin-message"></a><span data-ttu-id="09633-104">\_Iniciar mensagem de DECOMPRESSEX de ICM \_</span><span class="sxs-lookup"><span data-stu-id="09633-104">ICM\_DECOMPRESSEX\_BEGIN message</span></span>

<span data-ttu-id="09633-105">A mensagem **ICM \_ DECOMPRESSEX \_ begin** notifica um driver de compactação de vídeo para se preparar para descompactar dados.</span><span class="sxs-lookup"><span data-stu-id="09633-105">The **ICM\_DECOMPRESSEX\_BEGIN** message notifies a video compression driver to prepare to decompress data.</span></span>


```C++
ICM_DECOMPRESSEX_BEGIN 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a><span data-ttu-id="09633-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09633-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09633-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span><span class="sxs-lookup"><span data-stu-id="09633-107"><span id="icdex"></span><span id="ICDEX"></span>*icdex*</span></span>
</dt> <dd>

<span data-ttu-id="09633-108">Ponteiro para uma estrutura [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) que contém os formatos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="09633-108">Pointer to a [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) structure containing the input and output formats.</span></span>

</dd> <dt>

<span data-ttu-id="09633-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="09633-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="09633-110">Tamanho, em bytes, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span><span class="sxs-lookup"><span data-stu-id="09633-110">Size, in bytes, of [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09633-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="09633-111">Return Value</span></span>

<span data-ttu-id="09633-112">Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.</span><span class="sxs-lookup"><span data-stu-id="09633-112">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="09633-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="09633-113">Remarks</span></span>

<span data-ttu-id="09633-114">Quando o driver recebe essa mensagem, ele deve alocar buffers e realizar operações demoradas para que possa processar mensagens [**\_ DECOMPRESSEX de ICM**](icm-decompressex.md) com eficiência.</span><span class="sxs-lookup"><span data-stu-id="09633-114">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESSEX**](icm-decompressex.md) messages efficiently.</span></span>

<span data-ttu-id="09633-115">Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem de [**\_ \_ início de desenho ICM**](icm-draw-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="09633-115">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message.</span></span>

<span data-ttu-id="09633-116">As mensagens **ICM \_ DECOMPRESSEX \_ begin** e [**ICM \_ DECOMPRESSEX \_ end**](icm-decompressex-end.md) não são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="09633-116">The **ICM\_DECOMPRESSEX\_BEGIN** and [**ICM\_DECOMPRESSEX\_END**](icm-decompressex-end.md) messages do not nest.</span></span> <span data-ttu-id="09633-117">Se o driver receber o **ICM \_ DECOMPRESSEX \_ begin** antes da descompactação ser interrompida com o **ICM \_ DECOMPRESSEX \_ end**, ele deverá reiniciar a descompactação com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="09633-117">If your driver receives **ICM\_DECOMPRESSEX\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESSEX\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="09633-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09633-118">Requirements</span></span>



| <span data-ttu-id="09633-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="09633-119">Requirement</span></span> | <span data-ttu-id="09633-120">Valor</span><span class="sxs-lookup"><span data-stu-id="09633-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="09633-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09633-121">Minimum supported client</span></span><br/> | <span data-ttu-id="09633-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09633-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="09633-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09633-123">Minimum supported server</span></span><br/> | <span data-ttu-id="09633-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09633-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="09633-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="09633-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="09633-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="09633-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09633-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="09633-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09633-128">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="09633-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="09633-129">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="09633-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





