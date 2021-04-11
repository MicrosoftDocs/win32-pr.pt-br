---
description: Especifica se os fluxos de áudio em uma apresentação têm uma taxa de bits variável.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: Atributo MF_PD_AUDIO_ISVARIABLEBITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170367"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="80a2b-103">\_ \_ Atributo ISVARIABLEBITRATE de áudio de PD do MF \_</span><span class="sxs-lookup"><span data-stu-id="80a2b-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="80a2b-104">Especifica se os fluxos de áudio em uma apresentação têm uma taxa de bits variável.</span><span class="sxs-lookup"><span data-stu-id="80a2b-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="80a2b-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="80a2b-105">Data type</span></span>

<span data-ttu-id="80a2b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="80a2b-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="80a2b-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="80a2b-107">Get/set</span></span>

<span data-ttu-id="80a2b-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="80a2b-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="80a2b-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="80a2b-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="80a2b-110">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="80a2b-110">Applies To</span></span>

[<span data-ttu-id="80a2b-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="80a2b-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="80a2b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="80a2b-112">Remarks</span></span>

<span data-ttu-id="80a2b-113">Este é um atributo opcional para descritores de apresentação.</span><span class="sxs-lookup"><span data-stu-id="80a2b-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="80a2b-114">Se o atributo for **true** (diferente de zero), a apresentação conterá pelo menos um fluxo de áudio de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="80a2b-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="80a2b-115">Se o atributo for **false**, todos os fluxos de áudio terão uma taxa de bits constante.</span><span class="sxs-lookup"><span data-stu-id="80a2b-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="80a2b-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="80a2b-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="80a2b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80a2b-117">Requirements</span></span>



| <span data-ttu-id="80a2b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a2b-118">Requirement</span></span> | <span data-ttu-id="80a2b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="80a2b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80a2b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80a2b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="80a2b-121">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="80a2b-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="80a2b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80a2b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="80a2b-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="80a2b-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="80a2b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80a2b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="80a2b-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="80a2b-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a2b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="80a2b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a2b-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80a2b-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80a2b-128">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="80a2b-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




