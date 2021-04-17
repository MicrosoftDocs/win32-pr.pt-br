---
description: Contém o identificador do elemento playlist na apresentação.
ms.assetid: 355818cf-1e00-46ad-9ce1-ab3a178164f9
title: Atributo MF_PD_PLAYBACK_ELEMENT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 744a1d164c71cbd7eb8bb47ef12be68d47b8351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754422"
---
# <a name="mf_pd_playback_element_id-attribute"></a><span data-ttu-id="0e507-103">\_Atributo de \_ ID do elemento de reprodução de PD MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="0e507-103">MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute</span></span>

<span data-ttu-id="0e507-104">Contém o identificador do elemento playlist na apresentação.</span><span class="sxs-lookup"><span data-stu-id="0e507-104">Contains the identifier of the playlist element in the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="0e507-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0e507-105">Data type</span></span>

<span data-ttu-id="0e507-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0e507-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0e507-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="0e507-107">Get/set</span></span>

<span data-ttu-id="0e507-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0e507-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0e507-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0e507-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="0e507-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="0e507-110">Applies to</span></span>

[<span data-ttu-id="0e507-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0e507-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="0e507-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e507-112">Remarks</span></span>

<span data-ttu-id="0e507-113">As fontes de mídia que entregam listas de reprodução podem, opcionalmente, definir esse atributo nos descritores de apresentação.</span><span class="sxs-lookup"><span data-stu-id="0e507-113">Media sources that deliver playlists can optionally set this attribute on their presentation descriptors.</span></span>

<span data-ttu-id="0e507-114">Quando uma fonte de mídia fornece uma lista de reprodução, ela envia um evento [MENewPresentation](menewpresentation.md) para cada elemento da playlist após o primeiro.</span><span class="sxs-lookup"><span data-stu-id="0e507-114">When a media source delivers a playlist, it sends a [MENewPresentation](menewpresentation.md) event for each playlist element after the first.</span></span> <span data-ttu-id="0e507-115">Esse evento contém um descritor de apresentação para o novo elemento playlist.</span><span class="sxs-lookup"><span data-stu-id="0e507-115">This event contains a presentation descriptor for the new playlist element.</span></span> <span data-ttu-id="0e507-116">A origem da mídia pode atribuir identificadores aos elementos, definindo o \_ atributo de ID do elemento de reprodução de PD MF \_ \_ \_ em cada descritor de apresentação, incluindo aquele criado por [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="0e507-116">The media source can assign identifiers to the elements by setting the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute on each presentation descriptor, including the one created by [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>

<span data-ttu-id="0e507-117">Uma origem de mídia também pode enviar o evento [MENewPresentation](menewpresentation.md) devido a um comutador de fluxo dinâmico ou uma alteração no número de fluxos.</span><span class="sxs-lookup"><span data-stu-id="0e507-117">A media source might also send the [MENewPresentation](menewpresentation.md) event because of a dynamic stream switch or a change in the number of streams.</span></span> <span data-ttu-id="0e507-118">Nessa situação, o valor da ID do \_ elemento MF PD \_ playback \_ \_ deve permanecer o mesmo em ambas as apresentações, para indicar que as duas apresentações representam o mesmo elemento de playlist.</span><span class="sxs-lookup"><span data-stu-id="0e507-118">In that situation, the value of MF\_PD\_PLAYBACK\_ELEMENT\_ID should remain the same across both presentations, to indicate that both presentations represent the same playlist element.</span></span> <span data-ttu-id="0e507-119">Se duas apresentações consecutivas tiverem o mesmo valor para esse atributo, o pipeline de Microsoft Media Foundation espera que os carimbos de data/hora permaneçam contínuos na transição.</span><span class="sxs-lookup"><span data-stu-id="0e507-119">If two consecutive presentations have the same value for this attribute, the Microsoft Media Foundation pipeline expects the time stamps to remain continuous across the transition.</span></span> <span data-ttu-id="0e507-120">Portanto, a origem da mídia não deve usar o atributo de [ \_ \_ \_ \_ início real da origem do evento MF](mf-event-source-actual-start-attribute.md) quando ela faz a transição para a próxima apresentação.</span><span class="sxs-lookup"><span data-stu-id="0e507-120">Therefore, the media source must not use the [MF\_EVENT\_SOURCE\_ACTUAL\_START](mf-event-source-actual-start-attribute.md) attribute when it transitions to the next presentation.</span></span>

<span data-ttu-id="0e507-121">As fontes de mídia que implementam [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devem usar o atributo [ \_ \_ \_ ElementID da sequência MF TOPONODE](mf-toponode-sequence-elementid-attribute.md) em vez do atributo de ID do elemento de reprodução de PD do MF \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0e507-121">Media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use the [MF\_TOPONODE\_SEQUENCE\_ELEMENTID](mf-toponode-sequence-elementid-attribute.md) attribute rather than the MF\_PD\_PLAYBACK\_ELEMENT\_ID attribute.</span></span>

<span data-ttu-id="0e507-122">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0e507-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e507-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e507-123">Requirements</span></span>



| <span data-ttu-id="0e507-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e507-124">Requirement</span></span> | <span data-ttu-id="0e507-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0e507-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e507-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e507-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e507-127">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0e507-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="0e507-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e507-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e507-129">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="0e507-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="0e507-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e507-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e507-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e507-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e507-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e507-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e507-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0e507-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0e507-134">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="0e507-134">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




