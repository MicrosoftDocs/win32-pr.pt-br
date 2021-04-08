---
description: Especifica a função de ponto de extremidade de áudio para o processador de áudio.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922075"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="3a284-103">\_Atributo de \_ função de \_ ponto de extremidade de atributo de processamento \_ de áudio \_ MF</span><span class="sxs-lookup"><span data-stu-id="3a284-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="3a284-104">Especifica a função de ponto de extremidade de áudio para o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="3a284-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="3a284-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3a284-105">Data type</span></span>

<span data-ttu-id="3a284-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3a284-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3a284-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a284-107">Remarks</span></span>

<span data-ttu-id="3a284-108">Você pode usar esse atributo para configurar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="3a284-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="3a284-109">O uso depende de qual função você chama para criar o processador de áudio:</span><span class="sxs-lookup"><span data-stu-id="3a284-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="3a284-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="3a284-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="3a284-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="3a284-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="3a284-112">Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="3a284-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="3a284-113">Um dispositivo de ponto de extremidade de áudio é um dispositivo de hardware que está em uma extremidade de um caminho de dados de áudio, como um fone de ouvido ou um palestrante.</span><span class="sxs-lookup"><span data-stu-id="3a284-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="3a284-114">Se esse atributo for definido, o processador de áudio usará o dispositivo de áudio padrão para a função especificada.</span><span class="sxs-lookup"><span data-stu-id="3a284-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="3a284-115">O valor desse atributo é um membro da enumeração **ERole** , que é definida no arquivo de cabeçalho mmdeviceapi. h.</span><span class="sxs-lookup"><span data-stu-id="3a284-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="3a284-116">Para obter mais informações, consulte a documentação da API de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="3a284-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="3a284-117">Se esse atributo não for definido, o processador de áudio usará o dispositivo de ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="3a284-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="3a284-118">Se esse atributo estiver definido, não defina o atributo [**de \_ ID do \_ ponto de extremidade do atributo de processador \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="3a284-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="3a284-119">Se ambos os atributos forem definidos, ocorrerá uma falha quando o processador de áudio for criado.</span><span class="sxs-lookup"><span data-stu-id="3a284-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="3a284-120">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3a284-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a284-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a284-121">Requirements</span></span>



| <span data-ttu-id="3a284-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a284-122">Requirement</span></span> | <span data-ttu-id="3a284-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3a284-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3a284-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a284-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a284-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a284-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a284-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a284-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a284-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a284-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3a284-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a284-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a284-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a284-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a284-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a284-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a284-131">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3a284-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a284-132">Atributos do processador de áudio</span><span class="sxs-lookup"><span data-stu-id="3a284-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a284-133">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3a284-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3a284-134">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="3a284-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3a284-135">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="3a284-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




