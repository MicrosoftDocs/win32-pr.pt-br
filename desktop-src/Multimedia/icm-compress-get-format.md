---
title: Mensagem de ICM_COMPRESS_GET_FORMAT (VFW. h)
description: A \_ mensagem ICM Compact \_ Get \_ Format solicita o formato de saída dos dados compactados de um driver de compactação de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_GET_FORMAT
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096ceafa382bdbae5e4efe16975b3518735e773
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455730"
---
# <a name="icm_compress_get_format-message"></a><span data-ttu-id="53c6c-105">\_Mensagem de \_ formato de obtenção do ICM Compact \_</span><span class="sxs-lookup"><span data-stu-id="53c6c-105">ICM\_COMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="53c6c-106">A mensagem **ICM \_ Compact \_ Get \_ Format** solicita o formato de saída dos dados compactados de um driver de compactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="53c6c-106">The **ICM\_COMPRESS\_GET\_FORMAT** message requests the output format of the compressed data from a video compression driver.</span></span> <span data-ttu-id="53c6c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="53c6c-107">You can send this message explicitly or by using the [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) macro.</span></span>


```C++
ICM_COMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="53c6c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53c6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c6c-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="53c6c-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="53c6c-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="53c6c-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="53c6c-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="53c6c-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="53c6c-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) para conter o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="53c6c-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="53c6c-113">Você pode especificar zero para esse parâmetro para solicitar apenas o tamanho do formato de saída, como na macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="53c6c-113">You can specify zero for this parameter to request only the size of the output format, as in the [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c6c-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="53c6c-114">Return Value</span></span>

<span data-ttu-id="53c6c-115">Se *lpbiOutput* for zero, retornará o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="53c6c-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="53c6c-116">Se *lpbiOutput* for diferente de zero, retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="53c6c-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="53c6c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="53c6c-117">Remarks</span></span>

<span data-ttu-id="53c6c-118">Se *lpbiOutput* for diferente de zero, o driver deverá preencher a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) com o formato de saída padrão correspondente ao formato de entrada especificado para *lpbiInput*.</span><span class="sxs-lookup"><span data-stu-id="53c6c-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="53c6c-119">Se o compressor puder produzir vários formatos, o formato padrão deverá ser o que preserva a maior quantidade de informações.</span><span class="sxs-lookup"><span data-stu-id="53c6c-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="53c6c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53c6c-120">Requirements</span></span>



| <span data-ttu-id="53c6c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c6c-121">Requirement</span></span> | <span data-ttu-id="53c6c-122">Valor</span><span class="sxs-lookup"><span data-stu-id="53c6c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="53c6c-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53c6c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="53c6c-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53c6c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="53c6c-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53c6c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="53c6c-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53c6c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="53c6c-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="53c6c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c6c-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="53c6c-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53c6c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="53c6c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c6c-130">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="53c6c-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="53c6c-131">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="53c6c-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

