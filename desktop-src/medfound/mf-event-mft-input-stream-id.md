---
description: Especifica um fluxo de entrada em uma Media Foundation transformação (MFT).
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: Atributo MF_EVENT_MFT_INPUT_STREAM_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d3966c33dc563fc9e38ad367cc675ba6616c03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164649"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a><span data-ttu-id="18c18-103">\_Atributo de \_ \_ ID do fluxo de entrada do MFT do \_ evento MF \_</span><span class="sxs-lookup"><span data-stu-id="18c18-103">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID attribute</span></span>

<span data-ttu-id="18c18-104">Especifica um fluxo de entrada em uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="18c18-104">Specifies an input stream on a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="18c18-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="18c18-105">Data type</span></span>

<span data-ttu-id="18c18-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="18c18-106">**UINT32**</span></span>

<span data-ttu-id="18c18-107">O valor é um identificador de fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="18c18-107">The value is an input stream identifier.</span></span>

## <a name="getset"></a><span data-ttu-id="18c18-108">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="18c18-108">Get/set</span></span>

<span data-ttu-id="18c18-109">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="18c18-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="18c18-110">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="18c18-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="18c18-111">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="18c18-111">Applies to</span></span>

[<span data-ttu-id="18c18-112">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="18c18-112">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="18c18-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="18c18-113">Remarks</span></span>

<span data-ttu-id="18c18-114">Esse atributo é usado com os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="18c18-114">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="18c18-115">METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="18c18-115">METransformDrainComplete</span></span>](metransformdraincomplete.md)
-   [<span data-ttu-id="18c18-116">METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="18c18-116">METransformNeedInput</span></span>](metransformneedinput.md)

<span data-ttu-id="18c18-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="18c18-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18c18-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18c18-118">Requirements</span></span>



| <span data-ttu-id="18c18-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="18c18-119">Requirement</span></span> | <span data-ttu-id="18c18-120">Valor</span><span class="sxs-lookup"><span data-stu-id="18c18-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18c18-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18c18-121">Minimum supported client</span></span><br/> | <span data-ttu-id="18c18-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="18c18-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="18c18-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18c18-123">Minimum supported server</span></span><br/> | <span data-ttu-id="18c18-124">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="18c18-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="18c18-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18c18-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="18c18-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="18c18-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18c18-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="18c18-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18c18-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18c18-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18c18-129">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="18c18-129">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="18c18-130">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="18c18-130">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




