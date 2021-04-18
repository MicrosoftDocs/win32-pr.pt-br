---
description: Contém sinalizadores para configurar o processador de áudio.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760298"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="f8a4d-103">\_Atributo de \_ sinalizadores de atributo de processamento de áudio MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="f8a4d-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="f8a4d-104">Contém sinalizadores para configurar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="f8a4d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f8a4d-105">Data type</span></span>

<span data-ttu-id="f8a4d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f8a4d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f8a4d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8a4d-107">Remarks</span></span>

<span data-ttu-id="f8a4d-108">O valor desse atributo é uma operação bit a bit **ou** dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="f8a4d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a4d-109">Value</span></span>                                                   | <span data-ttu-id="f8a4d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8a4d-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a4d-111">**\_sinalizadores de atributo do processador de áudio MF \_ \_ \_ \_ CROSSPROCESS**</span><span class="sxs-lookup"><span data-stu-id="f8a4d-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="f8a4d-112">O processador de áudio usa uma sessão de áudio de processo cruzado.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="f8a4d-113">Esse sinalizador permite que os renderizadores de áudio em vários processos compartilhem a mesma sessão de áudio, juntamente com os controles de política e de volume associados.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="f8a4d-114">Se esse sinalizador não for definido, a sessão de áudio não poderá ser compartilhada por renderizadores de áudio em outros processos.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="f8a4d-115">**\_sinalizadores de atributo do processador de áudio MF \_ \_ \_ \_ nopersist**</span><span class="sxs-lookup"><span data-stu-id="f8a4d-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="f8a4d-116">A API de sessão de áudio do Windows (WASAPI) não manterá as propriedades desta sessão de áudio, como o volume da sessão.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="f8a4d-117">Se esse sinalizador não for definido, WASAPI manterá as propriedades de sessão de áudio.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="f8a4d-118">Você pode usar esse atributo para configurar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="f8a4d-119">O uso depende de qual função você chama para criar o processador de áudio:</span><span class="sxs-lookup"><span data-stu-id="f8a4d-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="f8a4d-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="f8a4d-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="f8a4d-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="f8a4d-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="f8a4d-122">Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="f8a4d-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="f8a4d-123">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f8a4d-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a4d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8a4d-124">Requirements</span></span>



| <span data-ttu-id="f8a4d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8a4d-125">Requirement</span></span> | <span data-ttu-id="f8a4d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f8a4d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a4d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a4d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a4d-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8a4d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8a4d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8a4d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a4d-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8a4d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8a4d-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8a4d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8a4d-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a4d-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a4d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8a4d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a4d-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8a4d-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8a4d-135">Atributos do processador de áudio</span><span class="sxs-lookup"><span data-stu-id="f8a4d-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8a4d-136">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f8a4d-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f8a4d-137">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="f8a4d-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f8a4d-138">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="f8a4d-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




