---
description: Especifica o identificador para o dispositivo de ponto de extremidade de áudio.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Atributo MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296568"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="ecf35-103">\_Atributo de \_ ID do \_ ponto de extremidade do atributo de processamento \_ de áudio \_ MF</span><span class="sxs-lookup"><span data-stu-id="ecf35-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="ecf35-104">Especifica o identificador para o dispositivo de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="ecf35-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="ecf35-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ecf35-105">Data type</span></span>

<span data-ttu-id="ecf35-106">Cadeia de caracteres largos</span><span class="sxs-lookup"><span data-stu-id="ecf35-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf35-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecf35-107">Remarks</span></span>

<span data-ttu-id="ecf35-108">Você pode usar esse atributo para configurar o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="ecf35-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="ecf35-109">O uso depende de qual função você chama para criar o processador de áudio:</span><span class="sxs-lookup"><span data-stu-id="ecf35-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="ecf35-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): defina esse atributo usando o ponteiro de interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) especificado no parâmetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="ecf35-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="ecf35-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): defina esse atributo usando o ponteiro de interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recuperado no parâmetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="ecf35-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="ecf35-112">Defina o atributo antes de chamar [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="ecf35-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="ecf35-113">Um dispositivo de ponto de extremidade de áudio é um dispositivo de hardware que está em uma extremidade de um caminho de dados de áudio, como um fone de ouvido ou um palestrante.</span><span class="sxs-lookup"><span data-stu-id="ecf35-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="ecf35-114">Para obter o identificador de ponto de extremidade de áudio, use as seguintes APIs de áudio principal:</span><span class="sxs-lookup"><span data-stu-id="ecf35-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="ecf35-115">Use a interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) para enumerar os dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="ecf35-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="ecf35-116">Chame [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter o identificador para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ecf35-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="ecf35-117">Para obter mais informações, consulte a documentação da API de [áudio principal](../coreaudio/core-audio-apis-in-windows-vista.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf35-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="ecf35-118">Se esse atributo não for definido, o processador de áudio usará o dispositivo de ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="ecf35-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="ecf35-119">Se esse atributo estiver definido, não defina o atributo [**de \_ função de \_ ponto de extremidade do atributo de processamento \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf35-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="ecf35-120">Se ambos os atributos forem definidos, ocorrerá uma falha quando o processador de áudio for criado.</span><span class="sxs-lookup"><span data-stu-id="ecf35-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="ecf35-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ecf35-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf35-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecf35-122">Requirements</span></span>



| <span data-ttu-id="ecf35-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf35-123">Requirement</span></span> | <span data-ttu-id="ecf35-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ecf35-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf35-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecf35-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf35-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecf35-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ecf35-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ecf35-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf35-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ecf35-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ecf35-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ecf35-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf35-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf35-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf35-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecf35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf35-132">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ecf35-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecf35-133">Atributos do processador de áudio</span><span class="sxs-lookup"><span data-stu-id="ecf35-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecf35-134">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="ecf35-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="ecf35-135">**IMFAttributes:: SetString**</span><span class="sxs-lookup"><span data-stu-id="ecf35-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="ecf35-136">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="ecf35-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
