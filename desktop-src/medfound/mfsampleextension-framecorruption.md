---
description: Especifica se um quadro de vídeo está corrompido.
ms.assetid: 0218F6F6-6832-445C-B733-6A99E4EA2A3B
title: Atributo MFSampleExtension_FrameCorruption (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d3618e5d847833b539cdfa7f6f99ae784e96c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091355"
---
# <a name="mfsampleextension_framecorruption-attribute"></a><span data-ttu-id="cb2f6-103">\_Atributo MFSampleExtension FrameCorruption</span><span class="sxs-lookup"><span data-stu-id="cb2f6-103">MFSampleExtension\_FrameCorruption attribute</span></span>

<span data-ttu-id="cb2f6-104">Especifica se um quadro de vídeo está corrompido.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-104">Specifies whether a video frame is corrupted.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb2f6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cb2f6-105">Data type</span></span>

<span data-ttu-id="cb2f6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="cb2f6-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="cb2f6-107">Get/set</span></span>

<span data-ttu-id="cb2f6-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="cb2f6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="cb2f6-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="cb2f6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="cb2f6-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="cb2f6-110">Applies to</span></span>

[<span data-ttu-id="cb2f6-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="cb2f6-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="cb2f6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb2f6-112">Remarks</span></span>

<span data-ttu-id="cb2f6-113">Um decodificador de vídeo pode definir esse atributo em seus exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-113">A video decoder can set this attribute on its output samples.</span></span> <span data-ttu-id="cb2f6-114">Se o valor for 1, o decodificador detectou dados corrompidos no quadro.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-114">If the value is 1, the decoder detected data corruption in the frame.</span></span> <span data-ttu-id="cb2f6-115">Se o valor for 0, não haverá corrupção de dados ou nenhum foi detectado.</span><span class="sxs-lookup"><span data-stu-id="cb2f6-115">If the value is 0, there is no data corruption, or none was detected.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb2f6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb2f6-116">Requirements</span></span>



| <span data-ttu-id="cb2f6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb2f6-117">Requirement</span></span> | <span data-ttu-id="cb2f6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cb2f6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cb2f6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb2f6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cb2f6-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cb2f6-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="cb2f6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb2f6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cb2f6-122">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="cb2f6-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="cb2f6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb2f6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb2f6-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb2f6-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb2f6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb2f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb2f6-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb2f6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb2f6-127">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="cb2f6-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb2f6-128">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="cb2f6-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




