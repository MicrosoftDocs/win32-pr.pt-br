---
title: Mensagem de ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: A \_ mensagem de formato Get DEScompactar o ICM \_ \_ solicita o formato de saída dos dados descompactados de um driver de descompactação de vídeo. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressGetFormat.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_GET_FORMAT
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009640"
---
# <a name="icm_decompress_get_format-message"></a><span data-ttu-id="f4da4-105">\_ \_ Extrair \_ mensagem de formato do ICM</span><span class="sxs-lookup"><span data-stu-id="f4da4-105">ICM\_DECOMPRESS\_GET\_FORMAT message</span></span>

<span data-ttu-id="f4da4-106">A mensagem de **\_ \_ \_ formato Get descompactar o ICM** solicita o formato de saída dos dados descompactados de um driver de descompactação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f4da4-106">The **ICM\_DECOMPRESS\_GET\_FORMAT** message requests the output format of the decompressed data from a video decompression driver.</span></span> <span data-ttu-id="f4da4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .</span><span class="sxs-lookup"><span data-stu-id="f4da4-107">You can send this message explicitly or by using the [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) macro.</span></span>


```C++
ICM_DECOMPRESS_GET_FORMAT 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="f4da4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4da4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4da4-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="f4da4-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="f4da4-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="f4da4-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="f4da4-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="f4da4-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="f4da4-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) para conter o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="f4da4-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure to contain the output format.</span></span> <span data-ttu-id="f4da4-113">Você pode especificar zero para solicitar apenas o tamanho do formato de saída, como na macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .</span><span class="sxs-lookup"><span data-stu-id="f4da4-113">You can specify zero to request only the size of the output format, as in the [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) macro.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4da4-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f4da4-114">Return Value</span></span>

<span data-ttu-id="f4da4-115">Se *lpbiOutput* for zero, retornará o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="f4da4-115">If *lpbiOutput* is zero, returns the size of the structure.</span></span>

<span data-ttu-id="f4da4-116">Se *lpbiOutput* for diferente de zero, retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="f4da4-116">If *lpbiOutput* is nonzero, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4da4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4da4-117">Remarks</span></span>

<span data-ttu-id="f4da4-118">Se *lpbiOutput* for diferente de zero, o driver deverá preencher a estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) com o formato de saída padrão correspondente ao formato de entrada especificado para *lpbiInput*.</span><span class="sxs-lookup"><span data-stu-id="f4da4-118">If *lpbiOutput* is nonzero, the driver should fill the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure with the default output format corresponding to the input format specified for *lpbiInput*.</span></span> <span data-ttu-id="f4da4-119">Se o compressor puder produzir vários formatos, o formato padrão deverá ser o que preserva a maior quantidade de informações.</span><span class="sxs-lookup"><span data-stu-id="f4da4-119">If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4da4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4da4-120">Requirements</span></span>



| <span data-ttu-id="f4da4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4da4-121">Requirement</span></span> | <span data-ttu-id="f4da4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f4da4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4da4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4da4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f4da4-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4da4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f4da4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4da4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f4da4-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f4da4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4da4-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f4da4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4da4-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4da4-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4da4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4da4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4da4-130">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="f4da4-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="f4da4-131">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="f4da4-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

