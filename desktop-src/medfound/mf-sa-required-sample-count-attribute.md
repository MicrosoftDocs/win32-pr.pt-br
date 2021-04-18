---
description: Indica o número de buffers descompactados que o coletor de mídia do EVR (processador de vídeo avançado) exige para desentrelaçamento.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Atributo MF_SA_REQUIRED_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764184"
---
# <a name="mf_sa_required_sample_count-attribute"></a><span data-ttu-id="e03c6-103">\_Atributo de \_ \_ contagem de amostra necessário \_ do MF SA</span><span class="sxs-lookup"><span data-stu-id="e03c6-103">MF\_SA\_REQUIRED\_SAMPLE\_COUNT attribute</span></span>

<span data-ttu-id="e03c6-104">Indica o número de buffers descompactados que o coletor de mídia do EVR (processador de vídeo avançado) exige para desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="e03c6-104">Indicates the number of uncompressed buffers that the enhanced video renderer (EVR) media sink requires for deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="e03c6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e03c6-105">Data type</span></span>

<span data-ttu-id="e03c6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e03c6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e03c6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e03c6-107">Remarks</span></span>

<span data-ttu-id="e03c6-108">Esse é um atributo de nível de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e03c6-108">This is a stream-level attribute.</span></span> <span data-ttu-id="e03c6-109">Para obter o atributo do EVR, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e03c6-109">To get the attribute from the EVR, do the following:</span></span>

1.  <span data-ttu-id="e03c6-110">Chame [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) para obter o coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e03c6-110">Call [**IMFMediaSink::GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) to get the stream sink.</span></span>
2.  <span data-ttu-id="e03c6-111">Consulte o coletor de fluxo para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="e03c6-111">Query the stream sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>
3.  <span data-ttu-id="e03c6-112">Chamar [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e03c6-112">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e03c6-113">Internamente, o mixer fornece esse atributo para o EVR.</span><span class="sxs-lookup"><span data-stu-id="e03c6-113">Internally, the mixer provides this attribute to the EVR.</span></span> <span data-ttu-id="e03c6-114">Para obter o atributo do mixer, chame [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="e03c6-114">To get the attribute from the mixer, call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).</span></span>

<span data-ttu-id="e03c6-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e03c6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e03c6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e03c6-116">Requirements</span></span>



| <span data-ttu-id="e03c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e03c6-117">Requirement</span></span> | <span data-ttu-id="e03c6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e03c6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e03c6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e03c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e03c6-120">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="e03c6-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="e03c6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e03c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e03c6-122">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e03c6-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e03c6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e03c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e03c6-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e03c6-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e03c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e03c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e03c6-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e03c6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e03c6-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="e03c6-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e03c6-128">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="e03c6-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e03c6-129">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e03c6-129">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




