---
description: Taxa de erros de dados, em erros de bit por segundo, para um tipo de mídia de vídeo.
ms.assetid: 90433ff4-a563-4751-86d9-caac0cc58194
title: Atributo MF_MT_AVG_BIT_ERROR_RATE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21eb33d1bc1636dd047dbd56ce6b7ad3a683f356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165020"
---
# <a name="mf_mt_avg_bit_error_rate-attribute"></a><span data-ttu-id="db4c8-103">\_Atributo de \_ \_ taxa de \_ erros de bits \_ do MF MT</span><span class="sxs-lookup"><span data-stu-id="db4c8-103">MF\_MT\_AVG\_BIT\_ERROR\_RATE attribute</span></span>

<span data-ttu-id="db4c8-104">Taxa de erros de dados, em erros de bit por segundo, para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="db4c8-104">Data error rate, in bit errors per second, for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="db4c8-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="db4c8-105">Data type</span></span>

<span data-ttu-id="db4c8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="db4c8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="db4c8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="db4c8-107">Remarks</span></span>

<span data-ttu-id="db4c8-108">Esse atributo corresponde ao membro **dwBitErrorRate** das estruturas [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="db4c8-108">This attribute corresponds to the **dwBitErrorRate** member of the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structures.</span></span>

<span data-ttu-id="db4c8-109">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="db4c8-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="db4c8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db4c8-110">Requirements</span></span>



| <span data-ttu-id="db4c8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="db4c8-111">Requirement</span></span> | <span data-ttu-id="db4c8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="db4c8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db4c8-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db4c8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="db4c8-114">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="db4c8-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="db4c8-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db4c8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="db4c8-116">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="db4c8-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="db4c8-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db4c8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="db4c8-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db4c8-118"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db4c8-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="db4c8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db4c8-120">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db4c8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db4c8-121">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="db4c8-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="db4c8-122">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="db4c8-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="db4c8-123">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="db4c8-123">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="db4c8-124">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="db4c8-124">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
