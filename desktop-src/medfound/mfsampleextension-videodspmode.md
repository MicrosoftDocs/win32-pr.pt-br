---
description: Indica se a estabilização de vídeo foi aplicada a um quadro de vídeo.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Atributo MFSampleExtension_VideoDSPMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772660"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="e2c19-103">\_Atributo MFSampleExtension VideoDSPMode</span><span class="sxs-lookup"><span data-stu-id="e2c19-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="e2c19-104">Indica se a estabilização de vídeo foi aplicada a um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2c19-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2c19-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e2c19-105">Data type</span></span>

<span data-ttu-id="e2c19-106">**MFVideoDSPMode** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e2c19-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e2c19-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="e2c19-107">Get/set</span></span>

<span data-ttu-id="e2c19-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e2c19-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e2c19-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e2c19-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e2c19-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="e2c19-110">Applies to</span></span>

[<span data-ttu-id="e2c19-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="e2c19-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="e2c19-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2c19-112">Remarks</span></span>

<span data-ttu-id="e2c19-113">O [**estabilização de vídeo MFT**](video-stabilization-mft.md) define esse atributo nos exemplos de saída que ele produz.</span><span class="sxs-lookup"><span data-stu-id="e2c19-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="e2c19-114">O valor do atributo é um valor de enumeração [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) .</span><span class="sxs-lookup"><span data-stu-id="e2c19-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="e2c19-115">Se o valor for **MFVideoDSPMode \_ estabilização**, isso significa que a MFT aplicou a estabilização de imagem ao quadro.</span><span class="sxs-lookup"><span data-stu-id="e2c19-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c19-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2c19-116">Requirements</span></span>



| <span data-ttu-id="e2c19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2c19-117">Requirement</span></span> | <span data-ttu-id="e2c19-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e2c19-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c19-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2c19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c19-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2c19-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="e2c19-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2c19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c19-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2c19-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2c19-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2c19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c19-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c19-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c19-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2c19-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c19-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2c19-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2c19-127">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="e2c19-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="e2c19-128">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="e2c19-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="e2c19-129">**Estabilização de Vídeo MFT**</span><span class="sxs-lookup"><span data-stu-id="e2c19-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




