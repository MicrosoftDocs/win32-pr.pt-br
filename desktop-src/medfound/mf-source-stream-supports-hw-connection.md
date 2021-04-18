---
description: Indica se uma fonte de mídia dá suporte ao fluxo de dados de hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Atributo MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807950"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="e3d59-103">O \_ fluxo de origem MF \_ \_ dá suporte ao \_ atributo de \_ conexão HW</span><span class="sxs-lookup"><span data-stu-id="e3d59-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="e3d59-104">Indica se uma fonte de mídia dá suporte ao fluxo de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="e3d59-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="e3d59-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e3d59-105">Data type</span></span>

<span data-ttu-id="e3d59-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="e3d59-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e3d59-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3d59-107">Remarks</span></span>

<span data-ttu-id="e3d59-108">Esse atributo é usado quando um proxy de origem de mídia um dispositivo de hardware e é capaz de transferir dados downstream em um barramento de hardware, sem enviar dados para a CPU.</span><span class="sxs-lookup"><span data-stu-id="e3d59-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="e3d59-109">Por exemplo, uma webcam pode entregar o vídeo codificado por H. 264 diretamente a um decodificador de hardware integrado.</span><span class="sxs-lookup"><span data-stu-id="e3d59-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="e3d59-110">Nesse cenário, a origem e o decodificador ainda são representados no Microsoft Media Foundation por um objeto de [origem de mídia](media-sources.md) e uma [Media Foundation transformação](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="e3d59-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="e3d59-111">No entanto, nenhum fluxo de dados entre esses dois objetos na camada de pipeline, somente na camada de hardware, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3d59-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![um diagrama que mostra uma origem de proxy de hardware.](images/proxy-mft3.png)

<span data-ttu-id="e3d59-113">A conexão entre a origem de mídia e a MFT é negociada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="e3d59-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="e3d59-114">O pipeline consulta a origem de mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="e3d59-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="e3d59-115">(Essa interface é opcional para que as fontes de mídia ofereçam suporte.)</span><span class="sxs-lookup"><span data-stu-id="e3d59-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="e3d59-116">O pipeline chama [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="e3d59-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="e3d59-117">As consultas de pipeline para o \_ fluxo de origem MF \_ \_ dão suporte ao \_ atributo de \_ conexão HW.</span><span class="sxs-lookup"><span data-stu-id="e3d59-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="e3d59-118">Se o atributo estiver presente e for igual a **true**, a fonte de mídia dará suporte a conexões de hardware.</span><span class="sxs-lookup"><span data-stu-id="e3d59-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="e3d59-119">O pipeline verifica se o MFT também é um proxy de hardware, verificando o atributo de [ \_ \_ \_ \_ atributo URL de hardware de enumeração de MFT](mft-enum-hardware-url-attribute.md) no MFT.</span><span class="sxs-lookup"><span data-stu-id="e3d59-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="e3d59-120">Para obter detalhes, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="e3d59-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="e3d59-121">O pipeline define o atributo de [ \_ atributo de \_ fluxo \_ do MFT conectado](mft-connected-stream-attribute.md) na MFT.</span><span class="sxs-lookup"><span data-stu-id="e3d59-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="e3d59-122">O valor desse atributo é o ponteiro [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtido da origem de mídia na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="e3d59-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="e3d59-123">O pipeline define o [MFT \_ conectado \_ ao \_ \_](mft-connected-to-hw-stream.md) atributo de fluxo de HW como **true** na origem da mídia e no MFT.</span><span class="sxs-lookup"><span data-stu-id="e3d59-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d59-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3d59-124">Requirements</span></span>



| <span data-ttu-id="e3d59-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3d59-125">Requirement</span></span> | <span data-ttu-id="e3d59-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e3d59-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d59-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3d59-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d59-128">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e3d59-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e3d59-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3d59-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d59-130">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e3d59-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e3d59-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3d59-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d59-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d59-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3d59-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3d59-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d59-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3d59-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e3d59-135">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="e3d59-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




