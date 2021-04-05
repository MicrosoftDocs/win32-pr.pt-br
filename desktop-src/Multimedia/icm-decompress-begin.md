---
title: Mensagem de ICM_DECOMPRESS_BEGIN (VFW. h)
description: A mensagem de início do ICM \_ DEScompactar \_ Notifica um driver de descompactação de vídeo para se preparar para descompactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS_BEGIN
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086141"
---
# <a name="icm_decompress_begin-message"></a><span data-ttu-id="a33cf-105">Mensagem de início do ICM \_ DEScompactar \_</span><span class="sxs-lookup"><span data-stu-id="a33cf-105">ICM\_DECOMPRESS\_BEGIN message</span></span>

<span data-ttu-id="a33cf-106">A mensagem de **início do ICM \_ descompactar \_** notifica um driver de descompactação de vídeo para se preparar para descompactar dados.</span><span class="sxs-lookup"><span data-stu-id="a33cf-106">The **ICM\_DECOMPRESS\_BEGIN** message notifies a video decompression driver to prepare to decompress data.</span></span> <span data-ttu-id="a33cf-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="a33cf-107">You can send this message explicitly or by using the [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) macro.</span></span>


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="a33cf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a33cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a33cf-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="a33cf-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="a33cf-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="a33cf-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="a33cf-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="a33cf-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="a33cf-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="a33cf-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a33cf-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a33cf-113">Return Value</span></span>

<span data-ttu-id="a33cf-114">Retornará ICERR \_ OK se a descompactação especificada for suportada ou ICERR \_ BADFORMAT do contrário.</span><span class="sxs-lookup"><span data-stu-id="a33cf-114">Returns ICERR\_OK if the specified decompression is supported or ICERR\_BADFORMAT otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33cf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a33cf-115">Remarks</span></span>

<span data-ttu-id="a33cf-116">Quando o driver recebe essa mensagem, ele deve alocar buffers e realizar operações demoradas para que possa processar com eficiência as mensagens do [**ICM \_**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="a33cf-116">When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process [**ICM\_DECOMPRESS**](icm-decompress.md) messages efficiently.</span></span>

<span data-ttu-id="a33cf-117">Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem [**ICM \_ draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="a33cf-117">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="a33cf-118">As mensagens de [**\_ \_ término**](icm-decompress-end.md) do **ICM \_ Descompacte \_ begin** e ICM não são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="a33cf-118">The **ICM\_DECOMPRESS\_BEGIN** and [**ICM\_DECOMPRESS\_END**](icm-decompress-end.md) messages do not nest.</span></span> <span data-ttu-id="a33cf-119">Se o driver receber **a \_ descompactação ICM \_ começar** antes que a descompactação seja interrompida com o **\_ \_ ponto de descompactação ICM**, ela deverá reiniciar a descompactação com novos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a33cf-119">If your driver receives **ICM\_DECOMPRESS\_BEGIN** before decompression is stopped with **ICM\_DECOMPRESS\_END**, it should restart decompression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33cf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33cf-120">Requirements</span></span>



| <span data-ttu-id="a33cf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33cf-121">Requirement</span></span> | <span data-ttu-id="a33cf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a33cf-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a33cf-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a33cf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a33cf-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a33cf-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a33cf-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a33cf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a33cf-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a33cf-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a33cf-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a33cf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a33cf-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a33cf-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a33cf-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a33cf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33cf-130">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="a33cf-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="a33cf-131">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="a33cf-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

