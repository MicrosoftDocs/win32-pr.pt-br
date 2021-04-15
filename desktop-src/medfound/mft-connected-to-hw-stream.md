---
description: Especifica se uma Media Foundation de transformação baseada em hardware (MFT) está conectada a outra MFT baseada em hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Atributo MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753879"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="6b1e9-103">MFT \_ conectado \_ ao \_ atributo de fluxo de HW \_</span><span class="sxs-lookup"><span data-stu-id="6b1e9-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="6b1e9-104">Especifica se uma Media Foundation de transformação baseada em hardware (MFT) está conectada a outra MFT baseada em hardware.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="6b1e9-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6b1e9-105">Data type</span></span>

<span data-ttu-id="6b1e9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6b1e9-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="6b1e9-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="6b1e9-107">Get/set</span></span>

<span data-ttu-id="6b1e9-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="6b1e9-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="6b1e9-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="6b1e9-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b1e9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b1e9-110">Remarks</span></span>

<span data-ttu-id="6b1e9-111">Normalmente, os aplicativos não usam esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="6b1e9-112">Esse atributo é usado com MFTs com base em hardware.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="6b1e9-113">Quando dois MFTs de hardware são conectados em uma topologia, o carregador de topologia define esse atributo como **true** nos seguintes objetos:</span><span class="sxs-lookup"><span data-stu-id="6b1e9-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="6b1e9-114">O fluxo de saída do MFT de upstream</span><span class="sxs-lookup"><span data-stu-id="6b1e9-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="6b1e9-115">O fluxo de entrada do MFT downstream</span><span class="sxs-lookup"><span data-stu-id="6b1e9-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="6b1e9-116">Para obter o repositório de atributos para o fluxo de saída, o carregador de topologia chama [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) no MFT upstream.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="6b1e9-117">Para obter o repositório de atributos para o fluxo de entrada, o carregador de topologia chama [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) no MFT downstream.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="6b1e9-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6b1e9-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1e9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b1e9-119">Requirements</span></span>



| <span data-ttu-id="6b1e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b1e9-120">Requirement</span></span> | <span data-ttu-id="6b1e9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6b1e9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1e9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b1e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6b1e9-123">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6b1e9-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6b1e9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b1e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6b1e9-125">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="6b1e9-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6b1e9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b1e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b1e9-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1e9-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b1e9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b1e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1e9-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6b1e9-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6b1e9-130">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="6b1e9-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="6b1e9-131">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="6b1e9-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




