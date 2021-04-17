---
description: Especifica a categoria de fluxo de áudio para o processador de áudio de streaming (SAR).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813009"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="dad6d-103">\_Atributo de \_ \_ categoria de fluxo do atributo de processamento de \_ áudio MF \_</span><span class="sxs-lookup"><span data-stu-id="dad6d-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="dad6d-104">Especifica a categoria de fluxo de áudio para o [processador de áudio de streaming](streaming-audio-renderer.md) (SAR).</span><span class="sxs-lookup"><span data-stu-id="dad6d-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="dad6d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dad6d-105">Data type</span></span>

<span data-ttu-id="dad6d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="dad6d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="dad6d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="dad6d-107">Remarks</span></span>

<span data-ttu-id="dad6d-108">Você pode usar esse atributo para configurar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="dad6d-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="dad6d-109">O uso depende de qual função você chama para criar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="dad6d-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="dad6d-110">Função</span><span class="sxs-lookup"><span data-stu-id="dad6d-110">Function</span></span>                                                               | <span data-ttu-id="dad6d-111">Como definir o atributo</span><span class="sxs-lookup"><span data-stu-id="dad6d-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dad6d-112">**MFCreateAudioRenderer**</span><span class="sxs-lookup"><span data-stu-id="dad6d-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="dad6d-113">Use o ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="dad6d-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="dad6d-114">**MFCreateAudioRendererActivate**</span><span class="sxs-lookup"><span data-stu-id="dad6d-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="dad6d-115">Use o ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retornado no parâmetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="dad6d-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="dad6d-116">Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="dad6d-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="dad6d-117">O valor do atributo é um membro da enumeração de [**\_ \_ categoria de fluxo de áudio**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .</span><span class="sxs-lookup"><span data-stu-id="dad6d-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="dad6d-118">O serviço de áudio usa a categoria de fluxo para determinar as políticas de áudio quando vários aplicativos tocam áudio ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="dad6d-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad6d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dad6d-119">Requirements</span></span>



| <span data-ttu-id="dad6d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dad6d-120">Requirement</span></span> | <span data-ttu-id="dad6d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="dad6d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dad6d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad6d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dad6d-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dad6d-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dad6d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dad6d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dad6d-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dad6d-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="dad6d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dad6d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dad6d-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dad6d-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dad6d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="dad6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad6d-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dad6d-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
