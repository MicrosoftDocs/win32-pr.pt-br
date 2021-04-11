---
title: Mensagem de ICM_COMPRESS_BEGIN (VFW. h)
description: A \_ mensagem de início de compactação ICM \_ Notifica um driver de compactação de vídeo para se preparar para compactar dados. Você pode enviar essa mensagem explicitamente ou usando a macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- Multimídia do Windows de mensagem ICM_COMPRESS_BEGIN
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009748"
---
# <a name="icm_compress_begin-message"></a><span data-ttu-id="5229e-105">\_Mensagem de início de compactação ICM \_</span><span class="sxs-lookup"><span data-stu-id="5229e-105">ICM\_COMPRESS\_BEGIN message</span></span>

<span data-ttu-id="5229e-106">A mensagem de **\_ \_ início de compactação ICM** notifica um driver de compactação de vídeo para se preparar para compactar dados.</span><span class="sxs-lookup"><span data-stu-id="5229e-106">The **ICM\_COMPRESS\_BEGIN** message notifies a video compression driver to prepare to compress data.</span></span> <span data-ttu-id="5229e-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .</span><span class="sxs-lookup"><span data-stu-id="5229e-107">You can send this message explicitly or by using the [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) macro.</span></span>


```C++
ICM_COMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a><span data-ttu-id="5229e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5229e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5229e-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span><span class="sxs-lookup"><span data-stu-id="5229e-109"><span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*</span></span>
</dt> <dd>

<span data-ttu-id="5229e-110">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="5229e-110">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the input format.</span></span>

</dd> <dt>

<span data-ttu-id="5229e-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span><span class="sxs-lookup"><span data-stu-id="5229e-111"><span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*</span></span>
</dt> <dd>

<span data-ttu-id="5229e-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="5229e-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure containing the output format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5229e-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="5229e-113">Return Value</span></span>

<span data-ttu-id="5229e-114">Retornará ICERR \_ OK se o driver der suporte à compactação especificada ou ICERR \_ BADFORMAT se não houver suporte para o formato de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="5229e-114">Returns ICERR\_OK if the driver supports the specified compression or ICERR\_BADFORMAT if the input or output format is not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="5229e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5229e-115">Remarks</span></span>

<span data-ttu-id="5229e-116">O driver deve alocar e inicializar qualquer tabela ou memória necessária para compactar os formatos de dados quando ele recebe a mensagem [**ICM \_ compress**](icm-compress.md) .</span><span class="sxs-lookup"><span data-stu-id="5229e-116">The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the [**ICM\_COMPRESS**](icm-compress.md) message.</span></span>

<span data-ttu-id="5229e-117">VCM salva as configurações da mensagem de **\_ \_ início de compactação ICM** mais recente.</span><span class="sxs-lookup"><span data-stu-id="5229e-117">VCM saves the settings of the most recent **ICM\_COMPRESS\_BEGIN** message.</span></span> <span data-ttu-id="5229e-118">As mensagens de término do **ICM \_ compacte \_ begin** e [**ICM \_ compress \_**](icm-compress-end.md) não são aninhadas.</span><span class="sxs-lookup"><span data-stu-id="5229e-118">The **ICM\_COMPRESS\_BEGIN** and [**ICM\_COMPRESS\_END**](icm-compress-end.md) messages do not nest.</span></span> <span data-ttu-id="5229e-119">Se o driver receber **a \_ compactação de ICM, \_ comece** antes que a compactação seja interrompida com a **\_ \_ extremidade de compactação ICM**, ela deverá reiniciar a compactação com novos parâmetros</span><span class="sxs-lookup"><span data-stu-id="5229e-119">If your driver receives **ICM\_COMPRESS\_BEGIN** before compression is stopped with **ICM\_COMPRESS\_END**, it should restart compression with new parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="5229e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5229e-120">Requirements</span></span>



| <span data-ttu-id="5229e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5229e-121">Requirement</span></span> | <span data-ttu-id="5229e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5229e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5229e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5229e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5229e-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5229e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5229e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5229e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5229e-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5229e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5229e-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5229e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5229e-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="5229e-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5229e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5229e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5229e-130">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="5229e-130">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="5229e-131">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="5229e-131">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

