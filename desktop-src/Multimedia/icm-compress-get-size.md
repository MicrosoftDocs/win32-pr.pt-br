---
title: Mensagem de ICM_COMPRESS_GET_SIZE (VFW. h)
description: A \_ mensagem ICM Compact \_ Get de \_ tamanho solicita que o driver de compactação de vídeo forneça o tamanho máximo de um quadro de dados quando compactados no formato de saída especificado. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_GET_SIZE
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918955"
---
# <a name="icm_compress_get_size-message"></a><span data-ttu-id="37b2b-105">ICM \_ compactar \_ mensagem de obtenção de \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="37b2b-105">ICM\_COMPRESS\_GET\_SIZE message</span></span>

<span data-ttu-id="37b2b-106">A mensagem **ICM \_ Compact Get de \_ \_ tamanho** solicita que o driver de compactação de vídeo forneça o tamanho máximo de um quadro de dados quando compactados no formato de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="37b2b-106">The **ICM\_COMPRESS\_GET\_SIZE** message requests that the video compression driver supply the maximum size of one frame of data when compressed into the specified output format.</span></span> <span data-ttu-id="37b2b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .</span><span class="sxs-lookup"><span data-stu-id="37b2b-107">You can send this message explicitly or by using the [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) macro.</span></span>


```C++
ICM_COMPRESS_GET_SIZE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="37b2b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37b2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b2b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="37b2b-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="37b2b-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="37b2b-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="37b2b-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="37b2b-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="37b2b-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="37b2b-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b2b-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="37b2b-113">Return Value</span></span>

<span data-ttu-id="37b2b-114">Retorna o número máximo de bytes que um único quadro compactado pode ocupar.</span><span class="sxs-lookup"><span data-stu-id="37b2b-114">Returns the maximum number of bytes a single compressed frame can occupy.</span></span>

## <a name="remarks"></a><span data-ttu-id="37b2b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="37b2b-115">Remarks</span></span>

<span data-ttu-id="37b2b-116">Normalmente, os aplicativos enviam essa mensagem para determinar o tamanho de um buffer a ser alocado para o quadro compactado.</span><span class="sxs-lookup"><span data-stu-id="37b2b-116">Typically, applications send this message to determine how large a buffer to allocate for the compressed frame.</span></span>

<span data-ttu-id="37b2b-117">O driver deve calcular o tamanho do maior quadro possível com base nos formatos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="37b2b-117">The driver should calculate the size of the largest possible frame based on the input and output formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b2b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37b2b-118">Requirements</span></span>



| <span data-ttu-id="37b2b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="37b2b-119">Requirement</span></span> | <span data-ttu-id="37b2b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="37b2b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="37b2b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37b2b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="37b2b-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="37b2b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="37b2b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37b2b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="37b2b-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="37b2b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="37b2b-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="37b2b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="37b2b-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="37b2b-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b2b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="37b2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b2b-128">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="37b2b-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="37b2b-129">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="37b2b-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

