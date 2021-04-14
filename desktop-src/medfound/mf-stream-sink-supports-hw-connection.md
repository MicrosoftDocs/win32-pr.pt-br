---
description: Indica se um coletor de mídia dá suporte ao fluxo de dados de hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Atributo MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461181"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="2597f-103">O \_ coletor de fluxo MF \_ \_ dá suporte ao \_ atributo de \_ conexão HW</span><span class="sxs-lookup"><span data-stu-id="2597f-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="2597f-104">Indica se um coletor de mídia dá suporte ao fluxo de dados de hardware.</span><span class="sxs-lookup"><span data-stu-id="2597f-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="2597f-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2597f-105">Data type</span></span>

<span data-ttu-id="2597f-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2597f-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2597f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2597f-107">Remarks</span></span>

<span data-ttu-id="2597f-108">Esse atributo é usado quando um coletor de mídia proxies de um dispositivo de hardware e é capaz de receber dados em um barramento de hardware.</span><span class="sxs-lookup"><span data-stu-id="2597f-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="2597f-109">Por exemplo, um decodificador de áudio de hardware pode enviar dados de áudio diretamente para o hardware de renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="2597f-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="2597f-110">Nesse cenário, o decodificador e o coletor ainda são representados no Microsoft Media Foundation por uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) e um coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="2597f-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="2597f-111">No entanto, nenhum fluxo de dados entre esses dois objetos na camada de pipeline, somente na camada de hardware, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="2597f-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![um diagrama que mostra uma origem de proxy de hardware.](images/proxy-mft4.png)

<span data-ttu-id="2597f-113">A conexão entre o MFT e o coletor de mídia é negociada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="2597f-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="2597f-114">O pipeline verifica se o MFT é um proxy de hardware, verificando o atributo de [ \_ \_ \_ \_ atributo URL de hardware de enumeração de MFT](mft-enum-hardware-url-attribute.md) no MFT.</span><span class="sxs-lookup"><span data-stu-id="2597f-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="2597f-115">Para obter detalhes, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="2597f-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="2597f-116">O pipeline Obtém um ponteiro para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) do coletor de fluxo no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="2597f-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="2597f-117">O pipeline usa o ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) para consultar o coletor de \_ fluxo MF que \_ \_ dá suporte ao \_ atributo de conexão HW \_ .</span><span class="sxs-lookup"><span data-stu-id="2597f-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="2597f-118">Se esse atributo estiver presente e for igual a **true**, a fonte de mídia dará suporte a conexões de hardware.</span><span class="sxs-lookup"><span data-stu-id="2597f-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="2597f-119">O pipeline define o atributo de [ \_ atributo de \_ fluxo \_ do MFT conectado](mft-connected-stream-attribute.md) no coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="2597f-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="2597f-120">O valor desse atributo é o ponteiro [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do MFT.</span><span class="sxs-lookup"><span data-stu-id="2597f-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="2597f-121">O pipeline define o [MFT \_ conectado \_ ao \_ \_](mft-connected-to-hw-stream.md) atributo de fluxo de HW como **true** no coletor de fluxo e no MFT.</span><span class="sxs-lookup"><span data-stu-id="2597f-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="2597f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2597f-122">Requirements</span></span>



| <span data-ttu-id="2597f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2597f-123">Requirement</span></span> | <span data-ttu-id="2597f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="2597f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2597f-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2597f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2597f-126">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2597f-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2597f-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2597f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2597f-128">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2597f-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2597f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2597f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2597f-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2597f-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2597f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2597f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2597f-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2597f-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




