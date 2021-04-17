---
description: Especifica os deslocamentos para os limites de carga em um quadro para exemplos protegidos.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Atributo MFSampleExtension_PacketCrossOffsets (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808353"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a><span data-ttu-id="1f56d-103">\_Atributo MFSampleExtension PacketCrossOffsets</span><span class="sxs-lookup"><span data-stu-id="1f56d-103">MFSampleExtension\_PacketCrossOffsets attribute</span></span>

<span data-ttu-id="1f56d-104">Especifica os deslocamentos para os limites de carga em um quadro para exemplos protegidos.</span><span class="sxs-lookup"><span data-stu-id="1f56d-104">Specifies the offsets to the payload boundaries in a frame for protected samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f56d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1f56d-105">Data type</span></span>

<span data-ttu-id="1f56d-106">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="1f56d-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="1f56d-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="1f56d-107">Get/set</span></span>

<span data-ttu-id="1f56d-108">Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="1f56d-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="1f56d-109">Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="1f56d-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1f56d-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="1f56d-110">Applies to</span></span>

[<span data-ttu-id="1f56d-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="1f56d-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="1f56d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f56d-112">Remarks</span></span>

<span data-ttu-id="1f56d-113">Esse atributo se aplica a amostras de mídia protegidas pelo Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="1f56d-113">This attribute applies to media samples protected by Windows Media Digital Rights Management (DRM).</span></span> <span data-ttu-id="1f56d-114">O valor do atributo é uma matriz de **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="1f56d-114">The value of the attribute is an array of **DWORD** s.</span></span> <span data-ttu-id="1f56d-115">Cada entrada na matriz é o deslocamento de um limite de carga, em relação ao início do quadro.</span><span class="sxs-lookup"><span data-stu-id="1f56d-115">Each entry in the array is the offset of a payload boundary, relative to the start of the frame.</span></span> <span data-ttu-id="1f56d-116">Um aplicativo pode usar esses valores ao descriptografar e reconstruir os quadros.</span><span class="sxs-lookup"><span data-stu-id="1f56d-116">An application can use these values when decrypting and reconstructing the frames.</span></span>

<span data-ttu-id="1f56d-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1f56d-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f56d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f56d-118">Requirements</span></span>



| <span data-ttu-id="1f56d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f56d-119">Requirement</span></span> | <span data-ttu-id="1f56d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1f56d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f56d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f56d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1f56d-122">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="1f56d-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="1f56d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f56d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1f56d-124">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1f56d-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1f56d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f56d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f56d-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f56d-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f56d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f56d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f56d-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f56d-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f56d-129">Divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="1f56d-129">ASF Splitter</span></span>](asf-splitter.md)
</dt> <dt>

[<span data-ttu-id="1f56d-130">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="1f56d-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f56d-131">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="1f56d-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




