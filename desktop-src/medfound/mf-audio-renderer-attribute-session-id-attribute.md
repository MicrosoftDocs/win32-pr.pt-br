---
description: Especifica a classe de política de áudio para o processador de áudio.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829233"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="f8f40-103">\_Atributo de \_ \_ ID de sessão de atributo de processador \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="f8f40-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="f8f40-104">Especifica a classe de política de áudio para o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f8f40-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="f8f40-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f8f40-105">Data type</span></span>

<span data-ttu-id="f8f40-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f8f40-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f40-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8f40-107">Remarks</span></span>

<span data-ttu-id="f8f40-108">Esse atributo associa o processador de áudio a uma classe de política de áudio.</span><span class="sxs-lookup"><span data-stu-id="f8f40-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="f8f40-109">Cada classe de política tem seu próprio controle de volume e de política.</span><span class="sxs-lookup"><span data-stu-id="f8f40-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="f8f40-110">Se esse atributo não for definido, o novo SAR ingressará na sessão de áudio padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f8f40-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="f8f40-111">Para obter mais informações, consulte [**IAudioClient:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) na documentação da API de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="f8f40-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="f8f40-112">Você pode usar esse atributo para configurar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f8f40-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="f8f40-113">O uso depende de qual função você chama para criar o processador de áudio:</span><span class="sxs-lookup"><span data-stu-id="f8f40-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="f8f40-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="f8f40-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="f8f40-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="f8f40-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="f8f40-116">Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="f8f40-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="f8f40-117">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f8f40-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8f40-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8f40-118">Requirements</span></span>



| <span data-ttu-id="f8f40-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8f40-119">Requirement</span></span> | <span data-ttu-id="f8f40-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f8f40-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f8f40-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8f40-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f8f40-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8f40-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f8f40-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8f40-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f8f40-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8f40-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f8f40-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8f40-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8f40-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8f40-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8f40-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8f40-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8f40-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f8f40-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8f40-129">Atributos do processador de áudio</span><span class="sxs-lookup"><span data-stu-id="f8f40-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="f8f40-130">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="f8f40-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="f8f40-131">**IMFAttributes:: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="f8f40-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="f8f40-132">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="f8f40-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
