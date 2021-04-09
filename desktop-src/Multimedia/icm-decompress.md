---
title: Mensagem de ICM_DECOMPRESS (VFW. h)
description: A \_ mensagem de DEScompactação ICM notifica um driver de descompactação de vídeo para descompactar um quadro de dados em um buffer definido pelo aplicativo.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- Multimídia do Windows de mensagem ICM_DECOMPRESS
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009638"
---
# <a name="icm_decompress-message"></a><span data-ttu-id="bfa99-104">\_Mensagem de DEScompactação ICM</span><span class="sxs-lookup"><span data-stu-id="bfa99-104">ICM\_DECOMPRESS message</span></span>

<span data-ttu-id="bfa99-105">A mensagem de **\_ descompactação ICM** notifica um driver de descompactação de vídeo para descompactar um quadro de dados em um buffer definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa99-105">The **ICM\_DECOMPRESS** message notifies a video decompression driver to decompress a frame of data into an application-defined buffer.</span></span>


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a><span data-ttu-id="bfa99-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfa99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa99-107"><span id="icd"></span><span id="ICD"></span>*ICD*</span><span class="sxs-lookup"><span data-stu-id="bfa99-107"><span id="icd"></span><span id="ICD"></span>*icd*</span></span>
</dt> <dd>

<span data-ttu-id="bfa99-108">Ponteiro para uma estrutura [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .</span><span class="sxs-lookup"><span data-stu-id="bfa99-108">Pointer to an [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bfa99-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfa99-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="bfa99-110">Tamanho, em bytes, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span><span class="sxs-lookup"><span data-stu-id="bfa99-110">Size, in bytes, of [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa99-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bfa99-111">Return Value</span></span>

<span data-ttu-id="bfa99-112">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="bfa99-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfa99-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfa99-113">Remarks</span></span>

<span data-ttu-id="bfa99-114">Se você quiser que o driver descompacte os dados diretamente na tela, envie a mensagem [**ICM \_ draw**](icm-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa99-114">If you want the driver to decompress data directly to the screen, send the [**ICM\_DRAW**](icm-draw.md) message.</span></span>

<span data-ttu-id="bfa99-115">O driver retornará um erro se essa mensagem for recebida antes da mensagem de [**início do ICM \_ descompactar \_**](icm-decompress-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa99-115">The driver returns an error if this message is received before the [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa99-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfa99-116">Requirements</span></span>



| <span data-ttu-id="bfa99-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfa99-117">Requirement</span></span> | <span data-ttu-id="bfa99-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bfa99-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bfa99-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfa99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa99-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bfa99-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bfa99-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfa99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa99-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bfa99-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bfa99-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bfa99-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa99-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa99-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa99-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bfa99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa99-126">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="bfa99-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="bfa99-127">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="bfa99-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





