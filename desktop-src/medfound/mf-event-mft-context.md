---
description: Contém um valor definido pelo chamador para um evento METransformMarker.
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: Atributo MF_EVENT_MFT_CONTEXT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61e8920c119da151df1215e8de8ce0d526220e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010718"
---
# <a name="mf_event_mft_context-attribute"></a><span data-ttu-id="a1dd6-103">\_Atributo de \_ contexto de MFT do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="a1dd6-103">MF\_EVENT\_MFT\_CONTEXT attribute</span></span>

<span data-ttu-id="a1dd6-104">Contém um valor definido pelo chamador para um evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dd6-104">Contains a caller-defined value for an [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="data-type"></a><span data-ttu-id="a1dd6-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a1dd6-105">Data type</span></span>

<span data-ttu-id="a1dd6-106">**ULONG \_ PTR** armazenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="a1dd6-106">**ULONG\_PTR** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="a1dd6-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="a1dd6-107">Get/set</span></span>

<span data-ttu-id="a1dd6-108">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="a1dd6-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="a1dd6-109">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="a1dd6-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a1dd6-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="a1dd6-110">Applies to</span></span>

[<span data-ttu-id="a1dd6-111">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="a1dd6-111">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a><span data-ttu-id="a1dd6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1dd6-112">Remarks</span></span>

<span data-ttu-id="a1dd6-113">Esse atributo é usado com o evento [METransformMarker](metransformmarker.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dd6-113">This attribute is used with the [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="a1dd6-114">O valor do atributo é obtido do parâmetro *ulParam* do método [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) .</span><span class="sxs-lookup"><span data-stu-id="a1dd6-114">The value of the attribute is taken from the *ulParam* parameter of the [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) method.</span></span>

<span data-ttu-id="a1dd6-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a1dd6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1dd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1dd6-116">Requirements</span></span>



| <span data-ttu-id="a1dd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1dd6-117">Requirement</span></span> | <span data-ttu-id="a1dd6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a1dd6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1dd6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1dd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a1dd6-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a1dd6-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a1dd6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1dd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a1dd6-122">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="a1dd6-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a1dd6-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1dd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1dd6-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1dd6-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1dd6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1dd6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1dd6-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a1dd6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1dd6-127">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="a1dd6-127">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="a1dd6-128">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="a1dd6-128">Event Attributes</span></span>](event-attributes.md)
</dt> </dl>

 

 




