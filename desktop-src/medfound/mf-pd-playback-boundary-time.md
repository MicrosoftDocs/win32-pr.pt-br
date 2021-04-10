---
description: Armazena o tempo (em unidades de 100 a nanossegundos) em que a apresentação deve começar, em relação ao início da origem da mídia.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Atributo MF_PD_PLAYBACK_BOUNDARY_TIME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011740"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="a430a-103">\_Atributo de \_ \_ tempo limite de reprodução de PD MF \_</span><span class="sxs-lookup"><span data-stu-id="a430a-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="a430a-104">Armazena o tempo (em unidades de 100 a nanossegundos) em que a apresentação deve começar, em relação ao início da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="a430a-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="a430a-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a430a-105">Data type</span></span>

<span data-ttu-id="a430a-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a430a-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="a430a-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="a430a-107">Get/set</span></span>

<span data-ttu-id="a430a-108">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="a430a-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="a430a-109">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="a430a-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a430a-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="a430a-110">Applies to</span></span>

[<span data-ttu-id="a430a-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a430a-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="a430a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a430a-112">Remarks</span></span>

<span data-ttu-id="a430a-113">O \_ atributo de \_ tempo limite de reprodução de PD MF \_ \_ é opcional para fontes de mídia em uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="a430a-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="a430a-114">Esse valor indica a hora de início real da apresentação.</span><span class="sxs-lookup"><span data-stu-id="a430a-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="a430a-115">Considere uma lista de reprodução que inclui fontes de mídia *Element1*, *Element2* e *Element3* em uma sequência.</span><span class="sxs-lookup"><span data-stu-id="a430a-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="a430a-116">15 segundos depois que o *Element1* começa a ser reproduzido, ocorre uma alteração dinâmica de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a430a-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="a430a-117">O novo fluxo deve começar a reproduzir 15 segundos na apresentação.</span><span class="sxs-lookup"><span data-stu-id="a430a-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="a430a-118">No entanto, o quadro-chave mais próximo do tempo de apresentação de 15 segundos é de 12 segundos para o novo fluxo.</span><span class="sxs-lookup"><span data-stu-id="a430a-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="a430a-119">Para iniciar a nova apresentação em 15 segundos, uma marca é necessária para que as amostras decodificadas sejam removidas de 12 segundos para 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="a430a-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="a430a-120">Antes da transição, o evento [MENewPresentation](menewpresentation.md) é gerado pela fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="a430a-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="a430a-121">Isso retorna o descritor de apresentação que contém o atributo de [ID do elemento de reprodução de PD do MF \_ \_ \_ \_](mf-pd-playback-element-id.md) para *Element1*.</span><span class="sxs-lookup"><span data-stu-id="a430a-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="a430a-122">Além disso, ele contém o \_ atributo de tempo limite de reprodução de PD MF \_ \_ \_ que é definido como 15 segundos para indicar a hora em que a transição ocorreu.</span><span class="sxs-lookup"><span data-stu-id="a430a-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="a430a-123">A origem da mídia executa a marca de 15 segundos após a decodificação, o que impede que os quadros de 12 segundos a 15 segundos sejam exibidos.</span><span class="sxs-lookup"><span data-stu-id="a430a-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="a430a-124">Esse valor afeta apenas o tempo de marcação e não afeta como a sessão de mídia ajusta carimbos de data/hora.</span><span class="sxs-lookup"><span data-stu-id="a430a-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="a430a-125">Esse atributo é ignorado, a menos que a origem de mídia indique por meio do atributo de ID do elemento de reprodução de PD do MF que esta apresentação é o mesmo elemento de reprodução que o anterior. [ \_ \_ \_ \_ ](mf-pd-playback-element-id.md)</span><span class="sxs-lookup"><span data-stu-id="a430a-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="a430a-126">O \_ atributo de \_ tempo limite de reprodução de PD MF \_ \_ é semelhante ao atributo [MF \_ TOPONODE \_ MEDIASTART](mf-toponode-mediastart-attribute.md) que é definido no nó de topologia.</span><span class="sxs-lookup"><span data-stu-id="a430a-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="a430a-127">Para aplicativos em execução no Windows Vista, as fontes de mídia que implementam [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) devem usar **MF \_ TOPONODE \_ MEDIASTART** em vez de \_ \_ tempo limite de reprodução do MF PD \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a430a-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="a430a-128">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a430a-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a430a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a430a-129">Requirements</span></span>



| <span data-ttu-id="a430a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a430a-130">Requirement</span></span> | <span data-ttu-id="a430a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a430a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a430a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a430a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a430a-133">Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a430a-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a430a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a430a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a430a-135">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="a430a-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a430a-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a430a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a430a-137"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a430a-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a430a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a430a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a430a-139">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a430a-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a430a-140">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="a430a-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




