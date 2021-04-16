---
title: Mensagem de ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: O ICM \_ DEScompactar a \_ \_ mensagem obter paleta solicita que o driver de descompactação de vídeo forneça a tabela de cores da estrutura BITMAPINFOHEADER de saída. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_GET_PALETTE
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758608"
---
# <a name="icm_decompress_get_palette-message"></a><span data-ttu-id="2a9ce-105">ICM- \_ compactar \_ \_ mensagem obter paleta</span><span class="sxs-lookup"><span data-stu-id="2a9ce-105">ICM\_DECOMPRESS\_GET\_PALETTE message</span></span>

<span data-ttu-id="2a9ce-106">O **ICM \_ descompactar a mensagem \_ obter \_ paleta** solicita que o driver de descompactação de vídeo forneça a tabela de cores da estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) de saída.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-106">The **ICM\_DECOMPRESS\_GET\_PALETTE** message requests that the video decompression driver supply the color table of the output [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure.</span></span> <span data-ttu-id="2a9ce-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .</span><span class="sxs-lookup"><span data-stu-id="2a9ce-107">You can send this message explicitly or by using the [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="2a9ce-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a9ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a9ce-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="2a9ce-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="2a9ce-110">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="2a9ce-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="2a9ce-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="2a9ce-112">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) para conter a tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-112">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure to contain the color table.</span></span> <span data-ttu-id="2a9ce-113">O espaço reservado para a tabela de cores é sempre pelo menos 256 cores.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-113">The space reserved for the color table is always at least 256 colors.</span></span> <span data-ttu-id="2a9ce-114">Você pode especificar zero para esse parâmetro para retornar apenas o tamanho da tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-114">You can specify zero for this parameter to return only the size of the color table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a9ce-115">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2a9ce-115">Return Value</span></span>

<span data-ttu-id="2a9ce-116">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-116">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a9ce-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a9ce-117">Remarks</span></span>

<span data-ttu-id="2a9ce-118">Se *lpbiOutput* for diferente de zero, o driver definirá o membro **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) como o número de cores na tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-118">If *lpbiOutput* is nonzero, the driver sets the **biClrUsed** member of [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) to the number of colors in the color table.</span></span> <span data-ttu-id="2a9ce-119">O driver preenche o membro **bmiColors** de [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) com as cores reais.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-119">The driver fills the **bmiColors** member of [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) with the actual colors.</span></span>

<span data-ttu-id="2a9ce-120">O driver deve dar suporte a essa mensagem somente se usar uma paleta diferente da especificada no formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a9ce-120">The driver should support this message only if it uses a palette other than the one specified in the input format.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9ce-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a9ce-121">Requirements</span></span>



| <span data-ttu-id="2a9ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a9ce-122">Requirement</span></span> | <span data-ttu-id="2a9ce-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2a9ce-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2a9ce-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a9ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9ce-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a9ce-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2a9ce-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a9ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9ce-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a9ce-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2a9ce-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a9ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a9ce-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a9ce-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a9ce-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a9ce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9ce-131">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a9ce-131">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2a9ce-132">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="2a9ce-132">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

