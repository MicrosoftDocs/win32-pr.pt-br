---
description: Contém um ponteiro para os atributos de fluxo do fluxo conectado em um MFT (Media Foundation baseado em hardware).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Atributo MFT_CONNECTED_STREAM_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827811"
---
# <a name="mft_connected_stream_attribute-attribute"></a><span data-ttu-id="0b61a-103">\_Atributo de \_ atributo de fluxo conectado ao MFT \_</span><span class="sxs-lookup"><span data-stu-id="0b61a-103">MFT\_CONNECTED\_STREAM\_ATTRIBUTE attribute</span></span>

<span data-ttu-id="0b61a-104">Contém um ponteiro para os atributos de fluxo do fluxo conectado em um MFT (Media Foundation baseado em hardware).</span><span class="sxs-lookup"><span data-stu-id="0b61a-104">Contains a pointer to the stream attributes of the connected stream on a hardware-based Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="0b61a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0b61a-105">Data type</span></span>

<span data-ttu-id="0b61a-106">**IMFAttributes \** _ armazenado como _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="0b61a-106">**IMFAttributes\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="0b61a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0b61a-107">Get/set</span></span>

<span data-ttu-id="0b61a-108">Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="0b61a-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="0b61a-109">Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="0b61a-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b61a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b61a-110">Remarks</span></span>

<span data-ttu-id="0b61a-111">Normalmente, os aplicativos não usam esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0b61a-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="0b61a-112">Esse atributo é usado para MFTs que atuam como proxies para um dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="0b61a-112">This attribute is used for MFTs that act as proxies to a hardware device.</span></span> <span data-ttu-id="0b61a-113">Para obter detalhes, consulte [hardware MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="0b61a-113">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>

<span data-ttu-id="0b61a-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0b61a-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b61a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b61a-115">Requirements</span></span>



| <span data-ttu-id="0b61a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b61a-116">Requirement</span></span> | <span data-ttu-id="0b61a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0b61a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b61a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b61a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0b61a-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b61a-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0b61a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b61a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0b61a-121">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0b61a-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="0b61a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b61a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b61a-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b61a-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b61a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b61a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b61a-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b61a-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b61a-126">MFT \_ conectado \_ ao \_ fluxo de HW \_</span><span class="sxs-lookup"><span data-stu-id="0b61a-126">MFT\_CONNECTED\_TO\_HW\_STREAM</span></span>](mft-connected-to-hw-stream.md)
</dt> <dt>

[<span data-ttu-id="0b61a-127">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="0b61a-127">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="0b61a-128">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="0b61a-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




