---
description: O SAR (processamento de áudio de streaming) é um coletor de mídia que renderiza áudio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Processador de streaming de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c5b55f197d5e9770c6f1be55f680c7f9136f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759802"
---
# <a name="streaming-audio-renderer"></a><span data-ttu-id="1a060-103">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="1a060-103">Streaming Audio Renderer</span></span>

<span data-ttu-id="1a060-104">O SAR (processamento de áudio de streaming) é um coletor de mídia que renderiza áudio.</span><span class="sxs-lookup"><span data-stu-id="1a060-104">The streaming audio renderer (SAR) is a media sink that renders audio.</span></span> <span data-ttu-id="1a060-105">Cada instância do SAR renderiza um fluxo de áudio único.</span><span class="sxs-lookup"><span data-stu-id="1a060-105">Each instance of the SAR renders a single audio stream.</span></span> <span data-ttu-id="1a060-106">Para renderizar vários fluxos, use várias instâncias do SAR.</span><span class="sxs-lookup"><span data-stu-id="1a060-106">To render multiple streams, use multiple instances of the SAR.</span></span>

<span data-ttu-id="1a060-107">Para criar o SAR, chame uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="1a060-107">To create the SAR, call either of the following functions:</span></span>

-   <span data-ttu-id="1a060-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span><span class="sxs-lookup"><span data-stu-id="1a060-108">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer).</span></span> <span data-ttu-id="1a060-109">Retorna um ponteiro para o SAR.</span><span class="sxs-lookup"><span data-stu-id="1a060-109">Returns a pointer to the SAR.</span></span>
-   <span data-ttu-id="1a060-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span><span class="sxs-lookup"><span data-stu-id="1a060-110">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate).</span></span> <span data-ttu-id="1a060-111">Retorna um ponteiro para um objeto de ativação, que pode ser usado para criar o SAR.</span><span class="sxs-lookup"><span data-stu-id="1a060-111">Returns a pointer to an activation object, which can be used to create the SAR.</span></span>

<span data-ttu-id="1a060-112">A segunda função, que retorna um objeto de ativação, é necessária se você estiver executando conteúdo protegido, pois o objeto de ativação deve ser serializado para o processo protegido.</span><span class="sxs-lookup"><span data-stu-id="1a060-112">The second function, which returns an activation object, is required if you are playing protected content, because the activation object must be serialized to the protected process.</span></span> <span data-ttu-id="1a060-113">Para limpar conteúdo, você pode usar qualquer uma das funções.</span><span class="sxs-lookup"><span data-stu-id="1a060-113">For clear content, you can use either function.</span></span>

<span data-ttu-id="1a060-114">O SAR pode receber áudio descompactado no formato de ponto flutuante PCM ou IEEE.</span><span class="sxs-lookup"><span data-stu-id="1a060-114">The SAR can receive uncompressed audio in either PCM or IEEE floating-point format.</span></span> <span data-ttu-id="1a060-115">Se a taxa de reprodução for mais rápida ou mais lenta que 1 ×, o SAR ajustará automaticamente o timbre.</span><span class="sxs-lookup"><span data-stu-id="1a060-115">If the playback rate is faster or slower than 1×, the SAR automatically adjusts the pitch.</span></span>

## <a name="configuring-the-audio-renderer"></a><span data-ttu-id="1a060-116">Configurando o processador de áudio</span><span class="sxs-lookup"><span data-stu-id="1a060-116">Configuring the Audio Renderer</span></span>

<span data-ttu-id="1a060-117">O SAR dá suporte a vários atributos de configuração.</span><span class="sxs-lookup"><span data-stu-id="1a060-117">The SAR supports several configuration attributes.</span></span> <span data-ttu-id="1a060-118">O mecanismo para definir esses atributos depende de qual função você chama para criar o SAR.</span><span class="sxs-lookup"><span data-stu-id="1a060-118">The mechanism for setting these attributes depends on which function you call to create the SAR.</span></span> <span data-ttu-id="1a060-119">Se você usar a função [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1a060-119">If you use the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function, do the following:</span></span>

1.  <span data-ttu-id="1a060-120">Crie um novo repositório de atributos chamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span><span class="sxs-lookup"><span data-stu-id="1a060-120">Create a new attribute store by calling [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).</span></span>
2.  <span data-ttu-id="1a060-121">Adicione os atributos ao repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="1a060-121">Add the attributes to the attribute store.</span></span>
3.  <span data-ttu-id="1a060-122">Passe o repositório de atributos para a função [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) no parâmetro *pAudioAttributes* .</span><span class="sxs-lookup"><span data-stu-id="1a060-122">Pass the attribute store to the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function in the *pAudioAttributes* parameter.</span></span>

<span data-ttu-id="1a060-123">Se você usar a função [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , a função retornará um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) no parâmetro *ppActivate* .</span><span class="sxs-lookup"><span data-stu-id="1a060-123">If you use the [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) function, the function returns a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface in the *ppActivate* parameter.</span></span> <span data-ttu-id="1a060-124">Use esse ponteiro para adicionar os atributos.</span><span class="sxs-lookup"><span data-stu-id="1a060-124">Use this pointer to add the attributes.</span></span>

<span data-ttu-id="1a060-125">Para obter uma lista de atributos de configuração, consulte [atributos do processador de áudio](audio-renderer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1a060-125">For a list of configuration attributes, see [Audio Renderer Attributes](audio-renderer-attributes.md).</span></span>

## <a name="selecting-the-audio-endpoint-device"></a><span data-ttu-id="1a060-126">Selecionando o dispositivo de ponto de extremidade de áudio</span><span class="sxs-lookup"><span data-stu-id="1a060-126">Selecting the Audio Endpoint Device</span></span>

<span data-ttu-id="1a060-127">Um *dispositivo de ponto de extremidade de áudio* é um dispositivo de hardware que renderiza ou captura áudio.</span><span class="sxs-lookup"><span data-stu-id="1a060-127">An *audio endpoint device* is a hardware device that either renders or captures audio.</span></span> <span data-ttu-id="1a060-128">Os exemplos incluem alto-falantes, fones de ouvido, microfones e CD players.</span><span class="sxs-lookup"><span data-stu-id="1a060-128">Examples include speakers, headphones, microphones, and CD players.</span></span> <span data-ttu-id="1a060-129">O SAR sempre usa um dispositivo de renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="1a060-129">The SAR always uses an audio rendering device.</span></span> <span data-ttu-id="1a060-130">Há duas maneiras de selecionar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a060-130">There are two ways to select the device.</span></span>

<span data-ttu-id="1a060-131">A primeira abordagem é enumerar os dispositivos de renderização de áudio no sistema, usando a interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .</span><span class="sxs-lookup"><span data-stu-id="1a060-131">The first approach is to enumerate the audio rendering devices on the system, using the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface.</span></span> <span data-ttu-id="1a060-132">Essa interface está documentada na documentação da API de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="1a060-132">This interface is documented in the core audio API documentation.</span></span>

1.  <span data-ttu-id="1a060-133">Crie o objeto enumerador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a060-133">Create the device enumerator object.</span></span>
2.  <span data-ttu-id="1a060-134">Use o enumerador de dispositivo para enumerar dispositivos de renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="1a060-134">Use the device enumerator to enumerate audio rendering devices.</span></span> <span data-ttu-id="1a060-135">Cada dispositivo é representado por um ponteiro para a interface [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .</span><span class="sxs-lookup"><span data-stu-id="1a060-135">Each device is represented by a pointer to the [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) interface.</span></span>
3.  <span data-ttu-id="1a060-136">Selecione um dispositivo, com base nas propriedades do dispositivo ou na seleção do usuário.</span><span class="sxs-lookup"><span data-stu-id="1a060-136">Select a device, based on the device properties or the user's selection.</span></span>
4.  <span data-ttu-id="1a060-137">Chame [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter o identificador do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1a060-137">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the device identifier.</span></span>
5.  <span data-ttu-id="1a060-138">Defina o identificador do dispositivo como o valor do [**atributo \_ ID do \_ ponto de extremidade do atributo do processador \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1a060-138">Set the device identifier as the value of the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span>

<span data-ttu-id="1a060-139">Em vez de enumerar dispositivos, você pode especificar o dispositivo de áudio por sua *função*.</span><span class="sxs-lookup"><span data-stu-id="1a060-139">Rather than enumerate devices, you can specify the audio device by its *role*.</span></span> <span data-ttu-id="1a060-140">Uma função de áudio identifica uma categoria geral de uso.</span><span class="sxs-lookup"><span data-stu-id="1a060-140">An audio role identifies a general category of usage.</span></span> <span data-ttu-id="1a060-141">Por exemplo, a função de *console* é definida para jogos e notificações do sistema, enquanto a função de *multimídia* é definida para música e filmes.</span><span class="sxs-lookup"><span data-stu-id="1a060-141">For example, the *console* role is defined for games and system notifications, while the *multimedia* role is defined for music and movies.</span></span> <span data-ttu-id="1a060-142">Cada função tem um dispositivo de renderização de áudio atribuído a ele e o usuário pode alterar essas atribuições.</span><span class="sxs-lookup"><span data-stu-id="1a060-142">Each role has one audio rendering device assigned to it, and the user can change these assignments.</span></span> <span data-ttu-id="1a060-143">Se você especificar uma função de dispositivo, o SAR usará qualquer dispositivo de áudio atribuído para essa função.</span><span class="sxs-lookup"><span data-stu-id="1a060-143">If you specify a device role, the SAR uses whatever audio device has been assigned for that role.</span></span> <span data-ttu-id="1a060-144">Para especificar a função de dispositivo, defina o atributo de [**\_ função de ponto de \_ extremidade do atributo de processamento \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1a060-144">To specify the device role, set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span>

<span data-ttu-id="1a060-145">Os dois atributos listados nesta seção são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="1a060-145">The two attributes listed in this section are mutually exclusive.</span></span> <span data-ttu-id="1a060-146">Se você não definir nenhum deles, o SAR usará o dispositivo de áudio atribuído à função **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="1a060-146">If you do not set either of them, the SAR uses the audio device that is assigned to the **eConsole** role.</span></span>

<span data-ttu-id="1a060-147">O código a seguir enumera os dispositivos de renderização de áudio e atribui o primeiro dispositivo na lista para o SAR.</span><span class="sxs-lookup"><span data-stu-id="1a060-147">The following code enumerates the audio rendering devices and assigns the first device in the list to the SAR.</span></span> <span data-ttu-id="1a060-148">Este exemplo usa a função [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) para criar o SAR.</span><span class="sxs-lookup"><span data-stu-id="1a060-148">This example uses the [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) function to create the SAR.</span></span>


```C++
#include <mmdeviceapi.h>

HRESULT hr = S_OK;

IMMDeviceEnumerator *pEnum = NULL;      // Audio device enumerator.
IMMDeviceCollection *pDevices = NULL;   // Audio device collection.
IMMDevice *pDevice = NULL;              // An audio device.
IMFAttributes *pAttributes = NULL;      // Attribute store.
IMFMediaSink *pSink = NULL;             // Streaming audio renderer (SAR)

LPWSTR wstrID = NULL;                   // Device ID.

// Create the device enumerator.
hr = CoCreateInstance(
    __uuidof(MMDeviceEnumerator), 
    NULL,
    CLSCTX_ALL, 
    __uuidof(IMMDeviceEnumerator), 
    (void**)&pEnum
    );

// Enumerate the rendering devices.
if (SUCCEEDED(hr))
{
    hr = pEnum->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pDevices);
}

// Get ID of the first device in the list.
if (SUCCEEDED(hr))
{
    hr = pDevices->Item(0, &pDevice);
}

if (SUCCEEDED(hr))
{
    hr = pDevice->GetId(&wstrID);
}

// Create an attribute store and set the device ID attribute.
if (SUCCEEDED(hr))
{
    hr = MFCreateAttributes(&pAttributes, 2);
}

if (SUCCEEDED(hr))
{
    hr = pAttributes->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

// Create the audio renderer.
if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRenderer(pAttributes, &pSink);    
}

SAFE_RELEASE(pEnum);
SAFE_RELEASE(pDevices);
SAFE_RELEASE(pDevice); 
SAFE_RELEASE(pAttributes);
CoTaskMemFree(wstrID);
```



<span data-ttu-id="1a060-149">Para criar o objeto de ativação para o SAR, altere o código que aparece após a chamada para [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1a060-149">To create the activation object for the SAR, change the code that appears after the call to [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to the following:</span></span>


```C++
IMFActivate *pActivate = NULL;          // Activation object.

if (SUCCEEDED(hr))
{
    hr = MFCreateAudioRendererActivate(&pActivate);    
}

if (SUCCEEDED(hr))
{
    hr = pActivate->SetString(
        MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID, 
        wstrID
        );
}

SAFE_RELEASE(pActivate);
```



## <a name="selecting-the-audio-session"></a><span data-ttu-id="1a060-150">Selecionando a sessão de áudio</span><span class="sxs-lookup"><span data-stu-id="1a060-150">Selecting the Audio Session</span></span>

<span data-ttu-id="1a060-151">Uma sessão de áudio é um grupo de fluxos de áudio relacionados que um aplicativo pode gerenciar coletivamente.</span><span class="sxs-lookup"><span data-stu-id="1a060-151">An audio session is a group of related audio streams that an application can manage collectively.</span></span> <span data-ttu-id="1a060-152">O aplicativo pode controlar o nível de volume e o estado de mudo de cada sessão.</span><span class="sxs-lookup"><span data-stu-id="1a060-152">The application can control the volume level and mute state of each session.</span></span> <span data-ttu-id="1a060-153">As sessões são identificadas por GUID.</span><span class="sxs-lookup"><span data-stu-id="1a060-153">Sessions are identified by GUID.</span></span> <span data-ttu-id="1a060-154">Para especificar a sessão de áudio para o SAR, use o atributo de [ID de sessão de atributo do \_ processador de áudio \_ \_ \_ \_ MF](mf-audio-renderer-attribute-session-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1a060-154">To specify the audio session for the SAR, use the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID](mf-audio-renderer-attribute-session-id-attribute.md) attribute.</span></span> <span data-ttu-id="1a060-155">Se você não definir esse atributo, o SAR ingressará na sessão padrão para esse processo, identificado pelo **GUID \_ NULL**.</span><span class="sxs-lookup"><span data-stu-id="1a060-155">If you do not set this attribute, the SAR joins the default session for that process, identified by **GUID\_NULL**.</span></span>

<span data-ttu-id="1a060-156">Por padrão, uma sessão de áudio é específica do processo, o que significa que ela contém somente fluxos do processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="1a060-156">By default, an audio session is process-specific, meaning it contains only streams from the calling process.</span></span> <span data-ttu-id="1a060-157">Para ingressar em uma sessão de processo cruzado, defina o atributo de [sinalizadores de atributo do \_ processador de áudio \_ \_ \_ MF](mf-audio-renderer-attribute-flags-attribute.md) com o valor **MF \_ Audio processador de o \_ \_ atributo \_ flags \_ CROSSPROCESS**.</span><span class="sxs-lookup"><span data-stu-id="1a060-157">To join a cross-process session, set the [MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS](mf-audio-renderer-attribute-flags-attribute.md) attribute with the value **MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**.</span></span>

<span data-ttu-id="1a060-158">Depois de criar o SAR, você usa a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) para unir a sessão a um grupo de sessões, todas controladas pelo mesmo controle de volume no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="1a060-158">After you create the SAR, you use the [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) interface to join the session to a group of sessions, all of which are controlled by the same volume control in the control panel.</span></span> <span data-ttu-id="1a060-159">Você também pode usar essa interface para definir o nome de exibição e o ícone que aparecem no controle de volume.</span><span class="sxs-lookup"><span data-stu-id="1a060-159">You can also use this interface to set the display name and the icon that appear in the volume control.</span></span>

## <a name="controlling-volume-levels"></a><span data-ttu-id="1a060-160">Controlando os níveis de volume</span><span class="sxs-lookup"><span data-stu-id="1a060-160">Controlling Volume Levels</span></span>

<span data-ttu-id="1a060-161">Para controlar o nível de volume mestre de todos os fluxos na sessão de áudio do SAR, use a interface [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) .</span><span class="sxs-lookup"><span data-stu-id="1a060-161">To control the master volume level of all the streams in the SAR's audio session, use the [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) interface.</span></span> <span data-ttu-id="1a060-162">Para controlar o volume de um fluxo individual ou para controlar o volume de canais individuais em um fluxo, use a interface [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) .</span><span class="sxs-lookup"><span data-stu-id="1a060-162">To control the volume of an individual stream, or to control the volume of individual channels within a stream, use the [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) interface.</span></span> <span data-ttu-id="1a060-163">Ambas as interfaces são obtidas chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span><span class="sxs-lookup"><span data-stu-id="1a060-163">Both interfaces are obtained by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice).</span></span> <span data-ttu-id="1a060-164">Você pode chamar **GetService** diretamente no SAR ou chamá-lo na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="1a060-164">You can call **GetService** directly on the SAR, or call it on the Media Session.</span></span> <span data-ttu-id="1a060-165">Os níveis de volume são expressos como valores de atenuação.</span><span class="sxs-lookup"><span data-stu-id="1a060-165">Volume levels are expressed as attenuation values.</span></span> <span data-ttu-id="1a060-166">Para cada canal, o nível de atenuação é o produto do volume mestre e do volume do canal.</span><span class="sxs-lookup"><span data-stu-id="1a060-166">For each channel, the attenuation level is the product of the master volume and the channel volume.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a060-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a060-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a060-168">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="1a060-168">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 
