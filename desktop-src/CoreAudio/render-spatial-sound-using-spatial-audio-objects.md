---
description: Este artigo apresenta alguns exemplos simples que ilustram como implementar o som espacial usando objetos de áudio espacial estáticos, objetos de áudio espacial dinâmicos e objetos de áudio espacial que usam a função de transferência relativa de cabeçalho (HRTF) da Microsoft.
ms.assetid: C99C342E-0BD9-486A-92AA-F8DCB72C1B00
title: Renderizar som espacial usando objetos de áudio espaciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd541026aa3e144ec8333c8ac045a17970735f17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646411"
---
# <a name="render-spatial-sound-using-spatial-audio-objects"></a><span data-ttu-id="8738a-103">Renderizar som espacial usando objetos de áudio espaciais</span><span class="sxs-lookup"><span data-stu-id="8738a-103">Render Spatial Sound Using Spatial Audio Objects</span></span>

<span data-ttu-id="8738a-104">Este artigo apresenta alguns exemplos simples que ilustram como implementar o som espacial usando objetos de áudio espacial estáticos, objetos de áudio espacial dinâmicos e objetos de áudio espacial que usam a função de transferência relativa de cabeçalho (HRTF) da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8738a-104">This article presents some simple examples that illustrate how to implement spatial sound using static spatial audio objects, dynamic spatial audio objects, and spatial audio objects that use Microsoft's Head Relative Transfer Function (HRTF).</span></span> <span data-ttu-id="8738a-105">As etapas de implementação para todas essas três técnicas são muito semelhantes e este artigo fornece um exemplo de código estruturado da mesma forma para cada técnica.</span><span class="sxs-lookup"><span data-stu-id="8738a-105">The implementation steps for all three of these techniques are very similar and this article provides a similarly structured code example for each technique.</span></span> <span data-ttu-id="8738a-106">Para obter exemplos completos de ponta a ponta de implementações de áudio espacial do mundo real, consulte [repositório do GitHub de exemplos de sons espaciais da Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span><span class="sxs-lookup"><span data-stu-id="8738a-106">For complete end-to-end examples of real-world spatial audio implementations, see [Microsoft Spatial Sound samples github repository](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio).</span></span> <span data-ttu-id="8738a-107">Para obter uma visão geral do Windows Sonic, a solução em nível de plataforma da Microsoft para suporte a sons espaciais no Xbox e no Windows, consulte [som espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="8738a-107">For an overview of Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, see [Spatial Sound](spatial-sound.md).</span></span>

## <a name="render-audio-using-static-spatial-audio-objects"></a><span data-ttu-id="8738a-108">Renderizar áudio usando objetos de áudio espacial estáticos</span><span class="sxs-lookup"><span data-stu-id="8738a-108">Render audio using static spatial audio objects</span></span>

<span data-ttu-id="8738a-109">Um objeto de áudio estático é usado para processar o som para um dos 18 canais de áudio estáticos definidos na enumeração [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) .</span><span class="sxs-lookup"><span data-stu-id="8738a-109">A static audio object is used to render sound to one of 18 static audio channels defined in the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration.</span></span> <span data-ttu-id="8738a-110">Cada um desses canais representa um palestrante real ou virtualizado em um ponto fixo no espaço que não é movido ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="8738a-110">Each of these channels represents a real or virtualized speaker at a fixed point in space that does not move over time.</span></span> <span data-ttu-id="8738a-111">Os canais estáticos que estão disponíveis em um determinado dispositivo dependem do formato de som espacial usado.</span><span class="sxs-lookup"><span data-stu-id="8738a-111">The static channels that are available on a particular device depend on the spatial sound format being used.</span></span> <span data-ttu-id="8738a-112">Para obter uma lista dos formatos com suporte e suas contagens de canal, consulte [som espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="8738a-112">For a list of the supported formats and their channel counts, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="8738a-113">Ao inicializar um fluxo de áudio espacial, você deve especificar quais dos canais estáticos disponíveis serão usados pelo fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-113">When you initialize a spatial audio stream, you must specify which of the available static channels the stream will use.</span></span> <span data-ttu-id="8738a-114">As definições de constante de exemplo a seguir podem ser usadas para especificar configurações comuns de alto-falante e obter o número de canais disponíveis para cada um.</span><span class="sxs-lookup"><span data-stu-id="8738a-114">The following example constant definitions can be used to specify common speaker configurations and get the number of channels available for each one.</span></span>


```C++
const AudioObjectType ChannelMask_Mono = AudioObjectType_FrontCenter;
const AudioObjectType ChannelMask_Stereo = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight);
const AudioObjectType ChannelMask_2_1 = (AudioObjectType)(ChannelMask_Stereo | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_Quad = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_BackLeft | AudioObjectType_BackRight);
const AudioObjectType ChannelMask_4_1 = (AudioObjectType)(ChannelMask_Quad | AudioObjectType_LowFrequency);
const AudioObjectType ChannelMask_5_1 = (AudioObjectType)(AudioObjectType_FrontLeft | AudioObjectType_FrontRight | AudioObjectType_FrontCenter | AudioObjectType_LowFrequency | AudioObjectType_SideLeft | AudioObjectType_SideRight);
const AudioObjectType ChannelMask_7_1 = (AudioObjectType)(ChannelMask_5_1 | AudioObjectType_BackLeft | AudioObjectType_BackRight);

const UINT32 MaxStaticObjectCount_7_1_4 = 12;
const AudioObjectType ChannelMask_7_1_4 = (AudioObjectType)(ChannelMask_7_1 | AudioObjectType_TopFrontLeft | AudioObjectType_TopFrontRight | AudioObjectType_TopBackLeft | AudioObjectType_TopBackRight);

const UINT32 MaxStaticObjectCount_7_1_4_4 = 16;
const AudioObjectType ChannelMask_7_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4 | AudioObjectType_BottomFrontLeft | AudioObjectType_BottomFrontRight |AudioObjectType_BottomBackLeft | AudioObjectType_BottomBackRight);

const UINT32 MaxStaticObjectCount_8_1_4_4 = 17;
const AudioObjectType ChannelMask_8_1_4_4 = (AudioObjectType)(ChannelMask_7_1_4_4 | AudioObjectType_BackCenter);
```



<span data-ttu-id="8738a-115">A primeira etapa na renderização do áudio espacial é obter o ponto de extremidade de áudio para o qual os dados de áudio serão enviados.</span><span class="sxs-lookup"><span data-stu-id="8738a-115">The first step in rendering spatial audio is to get the audio endpoint to which audio data will be sent.</span></span> <span data-ttu-id="8738a-116">Crie uma instância de [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chame [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter o dispositivo de processamento de áudio padrão.</span><span class="sxs-lookup"><span data-stu-id="8738a-116">Create an instance of [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) and call [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the default audio render device.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="8738a-117">Ao criar um fluxo de áudio espacial, você deve especificar o formato de áudio que o fluxo usará, fornecendo uma estrutura [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="8738a-117">When you create a spatial audio stream, you must specify the audio format the stream will use by providing a [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) structure.</span></span> <span data-ttu-id="8738a-118">Se você estiver reproduzindo áudio de um arquivo, o formato normalmente será determinado pelo formato de arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-118">If you are playing back audio from a file, the format is typically determined by the audio file format.</span></span> <span data-ttu-id="8738a-119">Este exemplo usa um formato mono, 32 bits, 48Hz.</span><span class="sxs-lookup"><span data-stu-id="8738a-119">This example uses a mono, 32-bit, 48Hz format.</span></span>


```C++
WAVEFORMATEX format;
format.wFormatTag = WAVE_FORMAT_IEEE_FLOAT;
format.wBitsPerSample = 32;
format.nChannels = 1;
format.nSamplesPerSec = 48000;
format.nBlockAlign = (format.wBitsPerSample >> 3) * format.nChannels;
format.nAvgBytesPerSec = format.nBlockAlign * format.nSamplesPerSec;
format.cbSize = 0;
```



<span data-ttu-id="8738a-120">A próxima etapa na renderização do áudio espacial é inicializar um fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-120">The next step in rendering spatial audio is to initialize a spatial audio stream.</span></span> <span data-ttu-id="8738a-121">Primeiro, obtenha uma instância de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="8738a-121">First, get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="8738a-122">Chame [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para certificar-se de que o formato de áudio que você está usando tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8738a-122">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="8738a-123">Crie um evento que o pipeline de áudio usará para notificar o aplicativo de que está pronto para mais dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-123">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="8738a-124">Preencha uma estrutura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) que será usada para inicializar o fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-124">Populate a [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure that will be used to initialize the spatial audio stream.</span></span> <span data-ttu-id="8738a-125">Neste exemplo, o campo **StaticObjectTypeMask** é definido como a constante **de \_ estéreo ChannelMask** definida anteriormente neste artigo, o que significa que somente os canais frontal direito e esquerdo podem ser usados pelo fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-125">In this example, the **StaticObjectTypeMask** field is set to the **ChannelMask\_Stereo** constant defined previously in this article, meaning that only the front right and left channels can be used by the audio stream.</span></span> <span data-ttu-id="8738a-126">Como este exemplo usa apenas objetos de áudio estáticos e nenhum objeto dinâmico, o campo **MaxDynamicObjectCount** é definido como 0.</span><span class="sxs-lookup"><span data-stu-id="8738a-126">Because this example uses only static audio objects and no dynamic objects, the **MaxDynamicObjectCount** field is set to 0.</span></span> <span data-ttu-id="8738a-127">O campo **categoria** é definido como um membro da enumeração [**de \_ \_ categoria de fluxo de áudio**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , que define como o sistema mistura o som desse fluxo com outras fontes de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-127">The **Category** field is set to a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration, which defines how the system mixes the sound from this stream with other audio sources.</span></span>

<span data-ttu-id="8738a-128">Chame [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para ativar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-128">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;

// Activate ISpatialAudioClient on the desired audio-device 
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = ChannelMask_Stereo;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = 0;
streamParams.Category = AudioCategory_SoundEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT activationParams;
PropVariantInit(&activationParams);
activationParams.vt = VT_BLOB;
activationParams.blob.cbSize = sizeof(streamParams);
activationParams.blob.pBlobData = reinterpret_cast<BYTE *>(&streamParams);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;
hr = spatialAudioClient->ActivateSpatialAudioStream(&activationParams, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



> [!Note]  
> <span data-ttu-id="8738a-129">Ao usar as interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) em um título de XDK (Xbox One Development Kit), primeiro você deve chamar **EnableSpatialAudio** antes de chamar [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) ou [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span><span class="sxs-lookup"><span data-stu-id="8738a-129">When using the [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interfaces on an Xbox One Development Kit (XDK) title, you must first call **EnableSpatialAudio** before calling [**IMMDeviceEnumerator::EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) or [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint).</span></span> <span data-ttu-id="8738a-130">A falha em fazer isso resultará em um \_ erro E nointerface ser retornado da chamada para Activate.</span><span class="sxs-lookup"><span data-stu-id="8738a-130">Failure to do so will result in an E\_NOINTERFACE error being returned from the call to Activate.</span></span> <span data-ttu-id="8738a-131">**EnableSpatialAudio** só está disponível para títulos XDK e não precisa ser chamado para plataforma universal do Windows aplicativos em execução no Xbox One, nem para nenhum dispositivo não Xbox.</span><span class="sxs-lookup"><span data-stu-id="8738a-131">**EnableSpatialAudio** is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</span></span>

 

<span data-ttu-id="8738a-132">Declare um ponteiro para um [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) que será usado para gravar dados de áudio em um canal estático.</span><span class="sxs-lookup"><span data-stu-id="8738a-132">Declare a pointer for an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) that will be used to write audio data to a static channel.</span></span> <span data-ttu-id="8738a-133">Aplicativos típicos usarão um objeto para cada canal especificado no campo **StaticObjectTypeMask** .</span><span class="sxs-lookup"><span data-stu-id="8738a-133">Typical apps will use an object for each channel specified in the **StaticObjectTypeMask** field.</span></span> <span data-ttu-id="8738a-134">Para simplificar, este exemplo usa apenas um único objeto de áudio estático.</span><span class="sxs-lookup"><span data-stu-id="8738a-134">For simplicity, this example only uses a single static audio object.</span></span>


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



<span data-ttu-id="8738a-135">Antes de entrar no loop de processamento de áudio, chame [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para instruir o pipeline de mídia a começar a solicitar dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-135">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span> <span data-ttu-id="8738a-136">Este exemplo usa um contador para interromper a renderização de áudio após 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="8738a-136">This example uses a counter to stop the rendering of audio after 5 seconds.</span></span>

<span data-ttu-id="8738a-137">Dentro do loop de processamento, aguarde o evento de conclusão do buffer, fornecido quando o fluxo de áudio espacial foi inicializado, para ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-137">Inside the render loop, wait for the buffer completion event, provided when the spatial audio stream was initialized, to be signaled.</span></span> <span data-ttu-id="8738a-138">Você deve definir um limite de tempo limite razoável, como 100 ms, ao aguardar o evento, pois qualquer alteração no tipo de renderização ou no ponto de extremidade fará com que esse evento nunca seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-138">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="8738a-139">Nesse caso, você pode chamar [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para tentar redefinir o fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-139">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="8738a-140">Em seguida, chame [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para permitir que o sistema saiba que você está prestes a preencher os buffers dos objetos de áudio com dados.</span><span class="sxs-lookup"><span data-stu-id="8738a-140">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="8738a-141">Esse método retorna o número de objetos de áudio dinâmicos disponíveis, não usados neste exemplo, e a contagem de quadros do buffer para objetos de áudio renderizados por esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-141">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="8738a-142">Se um objeto de áudio espacial estático ainda não tiver sido criado, crie um ou mais chamando [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passando um valor da enumeração [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) indicando o canal estático para o qual o áudio do objeto é renderizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-142">If a static spatial audio object has not yet been created, create one or more by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passing in a value from the [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) enumeration indicating the static channel to which the object's audio is rendered.</span></span>

<span data-ttu-id="8738a-143">Em seguida, chame [**ISpatialAudioObject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obter um ponteiro para o buffer de áudio do objeto de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-143">Next, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="8738a-144">Esse método também retorna o tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8738a-144">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="8738a-145">Este exemplo usa um método auxiliar, **WriteToAudioObjectBuffer**, para preencher o buffer com dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-145">This example uses a helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="8738a-146">Esse método é mostrado posteriormente neste artigo.</span><span class="sxs-lookup"><span data-stu-id="8738a-146">This method is shown later in this article.</span></span> <span data-ttu-id="8738a-147">Depois de gravar no buffer, o exemplo verifica se o tempo de vida de 5 segundos do objeto foi atingido e, nesse caso, [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) é chamado para permitir que o pipeline de áudio saiba que nenhum outro áudio será gravado usando esse objeto e o objeto é definido como **nullptr** para liberar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="8738a-147">After writing to the buffer, the example checks to see if the 5 second lifetime of the object has been reached, and if so, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="8738a-148">Depois de gravar dados em todos os seus objetos de áudio, chame [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para permitir que o sistema saiba que os dados estão prontos para renderização.</span><span class="sxs-lookup"><span data-stu-id="8738a-148">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="8738a-149">Você só pode chamar **GetBuffer** entre uma chamada para **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="8738a-149">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

// This example will render 5 seconds of audio samples
UINT totalFrameCount = format.nSamplesPerSec * 5;

bool isRendering = true;
while (isRendering)
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        hr = spatialAudioStream->Reset();

        if (hr != S_OK)
        {
            // handle the error
            break;
        }
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of dynamic objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    if (audioObjectFrontLeft == nullptr)
    {
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_FrontLeft, &audioObjectFrontLeft);
        if (hr != S_OK) break;
    }

    // Get the buffer to write audio data
    hr = audioObjectFrontLeft->GetBuffer(&buffer, &bufferLength);

    if (totalFrameCount >= frameCount)
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, 200.0f, format.nSamplesPerSec);

        totalFrameCount -= frameCount;
    }
    else
    {
        // Write audio data to the buffer
        WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), totalFrameCount, 750.0f, format.nSamplesPerSec);

        // Set end of stream for the last buffer 
        hr = audioObjectFrontLeft->SetEndOfStream(totalFrameCount);

        audioObjectFrontLeft = nullptr; // Release the object

        isRendering = false;
    }

    // Let the audio engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
};
```



<span data-ttu-id="8738a-150">Quando você terminar de renderizar o áudio espacial, pare o fluxo de áudio espacial chamando [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="8738a-150">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="8738a-151">Se você não pretende usar o fluxo novamente, libere seus recursos chamando [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="8738a-151">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="8738a-152">O método auxiliar **WriteToAudioObjectBuffer** grava um buffer completo de exemplos ou o número de exemplos restantes especificados por nosso limite de tempo definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8738a-152">The **WriteToAudioObjectBuffer** helper method writes either a full buffer of samples or the number of remaining samples specified by our app-defined time limit.</span></span> <span data-ttu-id="8738a-153">Isso também pode ser determinado, por exemplo, pelo número de amostras restantes em um arquivo de áudio de origem.</span><span class="sxs-lookup"><span data-stu-id="8738a-153">This could also be determined, for example, by the number of samples remaining in a source audio file.</span></span> <span data-ttu-id="8738a-154">Uma onda Sin simples, a frequência que é dimensionada pelo parâmetro de entrada *Frequency* , é gerada e gravada no buffer.</span><span class="sxs-lookup"><span data-stu-id="8738a-154">A simple sin wave, the frequency of which is scaled by the *frequency* input parameter, is generated and written to the buffer.</span></span>


```C++
void WriteToAudioObjectBuffer(FLOAT* buffer, UINT frameCount, FLOAT frequency, UINT samplingRate)
{
    const double PI = 4 * atan2(1.0, 1.0);
    static double _radPhase = 0.0;

    double step = 2 * PI * frequency / samplingRate;

    for (UINT i = 0; i < frameCount; i++)
    {
        double sample = sin(_radPhase);

        buffer[i] = FLOAT(sample);

        _radPhase += step; // next frame phase

        if (_radPhase >= 2 * PI)
        {
            _radPhase -= 2 * PI;
        }
    }
}
```



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a><span data-ttu-id="8738a-155">Renderizar áudio usando objetos de áudio espacial dinâmico</span><span class="sxs-lookup"><span data-stu-id="8738a-155">Render audio using dynamic spatial audio objects</span></span>

<span data-ttu-id="8738a-156">Os objetos dinâmicos permitem que você processe o áudio de uma posição arbitrária no espaço, em relação ao usuário.</span><span class="sxs-lookup"><span data-stu-id="8738a-156">Dynamic objects allow you to render audio from an arbitrary position in space, relative to the user.</span></span> <span data-ttu-id="8738a-157">A posição e o volume de um objeto de áudio dinâmico podem ser alterados ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="8738a-157">The position and volume of a dynamic audio object can be changed over time.</span></span> <span data-ttu-id="8738a-158">Normalmente, os jogos usarão a posição de um objeto 3D no mundo do jogo para especificar a posição do objeto de áudio dinâmico associado a ele.</span><span class="sxs-lookup"><span data-stu-id="8738a-158">Games will typically use the position of a 3D object in the game world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="8738a-159">O exemplo a seguir usará uma estrutura simples, **My3dObject**, para armazenar o conjunto mínimo de dados necessários para representar um objeto.</span><span class="sxs-lookup"><span data-stu-id="8738a-159">The following example will use a simple structure, **My3dObject**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="8738a-160">Esses dados incluem um ponteiro para um [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), a posição, a velocidade, o volume e a frequência de Tom para o objeto e um valor que armazena o número total de quadros para os quais o objeto deve renderizar o som.</span><span class="sxs-lookup"><span data-stu-id="8738a-160">This data includes a pointer to an [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), the position, velocity, volume, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObject
{
    Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float volume;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="8738a-161">As etapas de implementação para objetos de áudio dinâmicos são basicamente as mesmas que as etapas para objetos de áudio estáticos descritos acima.</span><span class="sxs-lookup"><span data-stu-id="8738a-161">The implementation steps for dynamic audio objects is largely the same as the steps for static audio objects described above.</span></span> <span data-ttu-id="8738a-162">Primeiro, obtenha um ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-162">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="8738a-163">Em seguida, inicialize o fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-163">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="8738a-164">Obtenha uma instância de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="8738a-164">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="8738a-165">Chame [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para certificar-se de que o formato de áudio que você está usando tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8738a-165">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="8738a-166">Crie um evento que o pipeline de áudio usará para notificar o aplicativo de que está pronto para mais dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-166">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="8738a-167">Chame [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar o número de objetos dinâmicos com suporte no sistema.</span><span class="sxs-lookup"><span data-stu-id="8738a-167">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="8738a-168">Se essa chamada retornar 0, os objetos de áudio espacial dinâmico não têm suporte ou estão habilitados no dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="8738a-168">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="8738a-169">Para obter informações sobre como habilitar o áudio espacial e obter detalhes sobre o número de objetos de áudio dinâmico disponíveis para diferentes formatos de áudio espacial, consulte [som espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="8738a-169">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="8738a-170">Ao preencher a estrutura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , defina o campo **MaxDynamicObjectCount** para o número máximo de objetos dinâmicos que seu aplicativo usará.</span><span class="sxs-lookup"><span data-stu-id="8738a-170">When populating the [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span>

<span data-ttu-id="8738a-171">Chame [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para ativar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-171">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

if (maxDynamicObjectCount == 0)
{
    // Dynamic objects are unsupported
    return;
}

// Set the maximum number of dynamic audio objects that will be used
SpatialAudioObjectRenderStreamActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = nullptr;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStream> spatialAudioStream;;
hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStream), (void**)&spatialAudioStream);
```



<span data-ttu-id="8738a-172">Veja a seguir alguns códigos específicos do aplicativo necessários para dar suporte a esse exemplo, que gerará dinamicamente objetos de áudio posicionados aleatoriamente e os armazenará em um vetor.</span><span class="sxs-lookup"><span data-stu-id="8738a-172">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObject> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-25, 25); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-1, 1); // uniform distribution for random velocity
std::uniform_real_distribution<> vol_dist(0.5, 1.0); // uniform distribution for random volume
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch
int spawnCounter = 0;
```



<span data-ttu-id="8738a-173">Antes de entrar no loop de processamento de áudio, chame [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para instruir o pipeline de mídia a começar a solicitar dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-173">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStream::Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="8738a-174">Dentro do loop de processamento, aguarde o evento de conclusão de buffer que fornecemos quando o fluxo de áudio espacial foi inicializado para ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-174">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="8738a-175">Você deve definir um limite de tempo limite razoável, como 100 ms, ao aguardar o evento, pois qualquer alteração no tipo de renderização ou no ponto de extremidade fará com que esse evento nunca seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-175">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="8738a-176">Nesse caso, você pode chamar [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para tentar redefinir o fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-176">In this case, you can call [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="8738a-177">Em seguida, chame [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para permitir que o sistema saiba que você está prestes a preencher os buffers dos objetos de áudio com dados.</span><span class="sxs-lookup"><span data-stu-id="8738a-177">Next, call [**ISpatialAudioObjectRenderStream::BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="8738a-178">Esse método retorna o número de objetos de áudio dinâmicos disponíveis e a contagem de quadros do buffer para objetos de áudio renderizados por esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-178">This method returns the number of available dynamic audio objects and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="8738a-179">Sempre que o contador de geração atingir o valor especificado, ativaremos um novo objeto de áudio dinâmico chamando [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) especificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="8738a-179">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioObjectRenderStream::ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="8738a-180">Se todos os objetos de áudio dinâmico disponíveis já tiverem sido alocados, esse método retornará **SPLAUDCLNT \_ E \_ não \_ mais \_ objetos**.</span><span class="sxs-lookup"><span data-stu-id="8738a-180">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="8738a-181">Nesse caso, você pode optar por liberar um ou mais objetos de áudio ativados anteriormente com base em sua priorização específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8738a-181">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="8738a-182">Depois que o objeto de áudio dinâmico tiver sido criado, ele será adicionado a uma nova estrutura **My3dObject** , com posição aleatória, velocidade, volume e valores de frequência, que é então adicionado à lista de objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="8738a-182">After the dynamic audio object has been created, it is added to a new **My3dObject** structure, with randomized position, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="8738a-183">Em seguida, itere sobre todos os objetos ativos, representados neste exemplo com a estrutura **My3dObject** definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8738a-183">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObject** structure.</span></span> <span data-ttu-id="8738a-184">Para cada objeto de áudio, chame [**ISpatialAudioObject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obter um ponteiro para o buffer de áudio do objeto de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-184">For each audio object, call [**ISpatialAudioObject::GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="8738a-185">Esse método também retorna o tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8738a-185">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="8738a-186">O método auxiliar, **WriteToAudioObjectBuffer**, para preencher o buffer com dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-186">The helper method, **WriteToAudioObjectBuffer**, to fill the buffer with audio data.</span></span> <span data-ttu-id="8738a-187">Depois de gravar no buffer, o exemplo atualiza a posição do objeto de áudio dinâmico chamando [**ISpatialAudioObject:: SETPOSITION**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span><span class="sxs-lookup"><span data-stu-id="8738a-187">After writing to the buffer, the example updates the position of the dynamic audio object by calling [**ISpatialAudioObject::SetPosition**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition).</span></span> <span data-ttu-id="8738a-188">O volume do objeto de áudio também pode ser modificado chamando [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span><span class="sxs-lookup"><span data-stu-id="8738a-188">The volume of the audio object can also be modified by calling [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume).</span></span> <span data-ttu-id="8738a-189">Se você não atualizar a posição ou o volume do objeto, ele reterá a posição e o volume da última vez que foi definido.</span><span class="sxs-lookup"><span data-stu-id="8738a-189">If you don't update the position or volume of the object, it will retain the position and volume from the last time it was set.</span></span> <span data-ttu-id="8738a-190">Se o tempo de vida definido pelo aplicativo do objeto tiver sido atingido, [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) será chamado para permitir que o pipeline de áudio saiba que nenhum áudio será gravado usando esse objeto e o objeto será definido como **nullptr** para liberar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="8738a-190">If the object's app-defined lifetime has been reached, [**ISpatialAudioObject::SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="8738a-191">Depois de gravar dados em todos os seus objetos de áudio, chame [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para permitir que o sistema saiba que os dados estão prontos para renderização.</span><span class="sxs-lookup"><span data-stu-id="8738a-191">After writing data to all of your audio objects, call [**ISpatialAudioObjectRenderStream::EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="8738a-192">Você só pode chamar **GetBuffer** entre uma chamada para **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="8738a-192">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStream->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStream->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObject;
        hr = spatialAudioStream->ActivateSpatialAudioObject(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObject obj = {
                audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(vol_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObject>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;
            it->audioObject->SetVolume(it->volume);

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStream->EndUpdatingAudioObjects();
} while (objectVector.size() > 0);
```



<span data-ttu-id="8738a-193">Quando você terminar de renderizar o áudio espacial, pare o fluxo de áudio espacial chamando [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span><span class="sxs-lookup"><span data-stu-id="8738a-193">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioObjectRenderStream::Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop).</span></span> <span data-ttu-id="8738a-194">Se você não pretende usar o fluxo novamente, libere seus recursos chamando [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span><span class="sxs-lookup"><span data-stu-id="8738a-194">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioObjectRenderStream::Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a><span data-ttu-id="8738a-195">Renderizar áudio usando objetos de áudio espacial dinâmico para HRTF</span><span class="sxs-lookup"><span data-stu-id="8738a-195">Render audio using dynamic spatial audio objects for HRTF</span></span>

<span data-ttu-id="8738a-196">Outro conjunto de APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), permite o áudio espacial que usa a função de transferência relativa (HRTF) da Microsoft para atenuar sons a fim de simular a posição do emissor no espaço, em relação ao usuário, que pode ser alterado ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="8738a-196">Another set of APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), enable spatial audio that uses Microsoft's Head-relative Transfer Function (HRTF) to attenuate sounds to simulate the emitter's position in space, relative to the user, which can be changed over time.</span></span> <span data-ttu-id="8738a-197">Além da posição, os objetos de áudio HRTF permitem que você especifique uma orientação no espaço, um directivity no qual o som é emitido, como uma forma cônica ou cardioid, e um modelo decaimento à medida que o objeto se move mais próximo e além do ouvinte virtual.</span><span class="sxs-lookup"><span data-stu-id="8738a-197">In addition to position, HRTF audio objects allow you to specify an orientation in space, a directivity in which sound is emitted, such as a cone or cardioid shape, and a decay model as the object moves nearer and further from the virtual listener.</span></span> <span data-ttu-id="8738a-198">Observe que essas interfaces HRTF estão disponíveis apenas quando o usuário tiver selecionado o Windows Sonic para fones de ouvido como o mecanismo de áudio espacial do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8738a-198">Note that these HRTF interfaces are only available when the user has selected Windows Sonic for Headphones as the spatial audio engine for the device.</span></span> <span data-ttu-id="8738a-199">Para obter informações sobre como configurar um dispositivo para usar o Windows Sonic para fones de ouvido, consulte [som espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="8738a-199">For information on configuring a device to use Windows Sonic for Headphones, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="8738a-200">As APIs [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) permitem que um aplicativo use explicitamente o caminho de renderização do Windows Sonic para fones de ouvido diretamente.</span><span class="sxs-lookup"><span data-stu-id="8738a-200">The [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) and [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) APIs allow an application to explicitly use the Windows Sonic for Headphones render path directly.</span></span> <span data-ttu-id="8738a-201">Essas APIs não dão suporte a formatos de som espaciais, como Dolby Atmos for Home Theater ou Dolby Atmos para fones de ouvido, nem a alternância de formato de saída controlada pelo consumidor por meio do painel de controle de **som** , nem a reprodução de alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="8738a-201">These APIs do not support spatial sound formats such as Dolby Atmos for Home Theater or Dolby Atmos for Headphones, nor consumer-controlled output format switching via the **Sound** control panel, nor playback over speakers.</span></span> <span data-ttu-id="8738a-202">Essas interfaces são destinadas ao uso em aplicativos do Windows Mixed Reality que desejam usar o Windows Sonic para recursos específicos de fones de ouvido (como predefinições ambientais e rolloff baseadas em distância especificadas de forma programática, fora dos pipelines de criação de conteúdo típicos).</span><span class="sxs-lookup"><span data-stu-id="8738a-202">These interfaces are intended for use in Windows Mixed Reality applications that want to use Windows Sonic for Headphones-specific capabilities (such as environmental presets and distance-based rolloff specified programmatically, outside of typical content authoring pipelines).</span></span> <span data-ttu-id="8738a-203">A maioria dos jogos e os cenários de realidade virtual preferem usar o [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8738a-203">Most games and virtual reality scenarios will prefer to use [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) instead.</span></span> <span data-ttu-id="8738a-204">As etapas de implementação para ambos os conjuntos de API são quase idênticas, portanto, é possível implementar as duas tecnologias e alternar no tempo de execução, dependendo de qual recurso está disponível no dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="8738a-204">The implementation steps for both API sets are almost identical, so it is possible to implement both technologies and switch at runtime depending on which feature is available on the current device.</span></span>

<span data-ttu-id="8738a-205">Aplicativos de realidade misturada normalmente usarão a posição de um objeto 3D no mundo virtual para especificar a posição do objeto de áudio dinâmico associado a ele.</span><span class="sxs-lookup"><span data-stu-id="8738a-205">Mixed-reality apps will typically use the position of a 3D object in the virtual world to specify the position of the dynamic audio object associated with it.</span></span> <span data-ttu-id="8738a-206">O exemplo a seguir usará uma estrutura simples, **My3dObjectForHrtf**, para armazenar o conjunto mínimo de dados necessários para representar um objeto.</span><span class="sxs-lookup"><span data-stu-id="8738a-206">The following example will use a simple structure, **My3dObjectForHrtf**, to store the minimum set of data needed to represent an object.</span></span> <span data-ttu-id="8738a-207">Esses dados incluem um ponteiro para um [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), a posição, a orientação, a velocidade e a frequência de Tom do objeto, e um valor que armazena o número total de quadros para os quais o objeto deve renderizar o som.</span><span class="sxs-lookup"><span data-stu-id="8738a-207">This data includes a pointer to an [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), the position, orientation, velocity, and tone frequency for the object, and a value that stores the total number of frames for which the object should render sound.</span></span>


```C++
struct My3dObjectForHrtf
{
    Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
    Windows::Foundation::Numerics::float3 position;
    Windows::Foundation::Numerics::float3 velocity;
    float yRotationRads;
    float deltaYRotation;
    float frequency; // in Hz
    UINT totalFrameCount;
};
```



<span data-ttu-id="8738a-208">As etapas de implementação para objetos de áudio dinâmicos HRTF são basicamente as mesmas que as etapas para objetos de áudio dinâmicos descritos na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="8738a-208">The implementation steps for dynamic HRTF audio objects is largely the same as the steps for dynamic audio objects described in the previous section.</span></span> <span data-ttu-id="8738a-209">Primeiro, obtenha um ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-209">First, get an audio endpoint.</span></span>


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



<span data-ttu-id="8738a-210">Em seguida, inicialize o fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-210">Next, initialize the spatial audio stream.</span></span> <span data-ttu-id="8738a-211">Obtenha uma instância de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span><span class="sxs-lookup"><span data-stu-id="8738a-211">Get an instance of [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) by calling [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate).</span></span> <span data-ttu-id="8738a-212">Chame [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para certificar-se de que o formato de áudio que você está usando tem suporte.</span><span class="sxs-lookup"><span data-stu-id="8738a-212">Call [**ISpatialAudioClient::IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) to make sure that the audio format you are using is supported.</span></span> <span data-ttu-id="8738a-213">Crie um evento que o pipeline de áudio usará para notificar o aplicativo de que está pronto para mais dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-213">Create an event that the audio pipeline will use to notify the app that it is ready for more audio data.</span></span>

<span data-ttu-id="8738a-214">Chame [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar o número de objetos dinâmicos com suporte no sistema.</span><span class="sxs-lookup"><span data-stu-id="8738a-214">Call [**ISpatialAudioClient::GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) to retrieve the number of dynamic objects supported by the system.</span></span> <span data-ttu-id="8738a-215">Se essa chamada retornar 0, os objetos de áudio espacial dinâmico não têm suporte ou estão habilitados no dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="8738a-215">If this call returns 0, then dynamic spatial audio objects are not supported or enabled on the current device.</span></span> <span data-ttu-id="8738a-216">Para obter informações sobre como habilitar o áudio espacial e obter detalhes sobre o número de objetos de áudio dinâmico disponíveis para diferentes formatos de áudio espacial, consulte [som espacial](spatial-sound.md).</span><span class="sxs-lookup"><span data-stu-id="8738a-216">For information on enabling spatial audio and for details on the number of dynamic audio objects available for different spatial audio formats, see [Spatial Sound](spatial-sound.md).</span></span>

<span data-ttu-id="8738a-217">Ao preencher a estrutura [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) , defina o campo **MaxDynamicObjectCount** para o número máximo de objetos dinâmicos que seu aplicativo usará.</span><span class="sxs-lookup"><span data-stu-id="8738a-217">When populating the [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) structure, set the **MaxDynamicObjectCount** field to the maximum number of dynamic objects your app will use.</span></span> <span data-ttu-id="8738a-218">Os params de ativação para HRTF dão suporte a alguns parâmetros adicionais, como um [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), um [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), um [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)e um [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), que especificam os valores padrão dessas configurações para novos objetos criados a partir do fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-218">The activation params for HRTF supports a few additional parameters, such as a [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), a [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), a [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype), and a [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), which specify the default values of these settings for new objects created from the stream.</span></span> <span data-ttu-id="8738a-219">Esses parâmetros são opcionais.</span><span class="sxs-lookup"><span data-stu-id="8738a-219">These parameters are optional.</span></span> <span data-ttu-id="8738a-220">Defina os campos como **nullptr** para não fornecer nenhum valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8738a-220">Set the fields to **nullptr** to provide no default values.</span></span>

<span data-ttu-id="8738a-221">Chame [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para ativar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-221">Call [**ISpatialAudioClient::ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) to activate the stream.</span></span>


```C++
// Activate ISpatialAudioClient on the desired audio-device 
Microsoft::WRL::ComPtr<ISpatialAudioClient> spatialAudioClient;
hr = defaultDevice->Activate(__uuidof(ISpatialAudioClient), CLSCTX_INPROC_SERVER, nullptr, (void**)&spatialAudioClient);

Microsoft::WRL::ComPtr<ISpatialAudioObjectRenderStreamForHrtf>  spatialAudioStreamForHrtf;
hr = spatialAudioClient->IsSpatialAudioStreamAvailable(__uuidof(spatialAudioStreamForHrtf), NULL);

hr = spatialAudioClient->IsAudioObjectFormatSupported(&format);

// Create the event that will be used to signal the client for more data
HANDLE bufferCompletionEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);

UINT32 maxDynamicObjectCount;
hr = spatialAudioClient->GetMaxDynamicObjectCount(&maxDynamicObjectCount);

SpatialAudioHrtfActivationParams streamParams;
streamParams.ObjectFormat = &format;
streamParams.StaticObjectTypeMask = AudioObjectType_None;
streamParams.MinDynamicObjectCount = 0;
streamParams.MaxDynamicObjectCount = min(maxDynamicObjectCount, 4);
streamParams.Category = AudioCategory_GameEffects;
streamParams.EventHandle = bufferCompletionEvent;
streamParams.NotifyObject = NULL;

SpatialAudioHrtfDistanceDecay decayModel;
decayModel.CutoffDistance = 100;
decayModel.MaxGain = 3.98f;
decayModel.MinGain = float(1.58439 * pow(10, -5));
decayModel.Type = SpatialAudioHrtfDistanceDecayType::SpatialAudioHrtfDistanceDecay_NaturalDecay;
decayModel.UnityGainDistance = 1;

streamParams.DistanceDecay = &decayModel;

SpatialAudioHrtfDirectivity directivity;
directivity.Type = SpatialAudioHrtfDirectivityType::SpatialAudioHrtfDirectivity_Cone;
directivity.Scaling = 1.0f;

SpatialAudioHrtfDirectivityCone cone;
cone.directivity = directivity;
cone.InnerAngle = 0.1f;
cone.OuterAngle = 0.2f;

SpatialAudioHrtfDirectivityUnion directivityUnion;
directivityUnion.Cone = cone;
streamParams.Directivity = &directivityUnion;

SpatialAudioHrtfEnvironmentType environment = SpatialAudioHrtfEnvironmentType::SpatialAudioHrtfEnvironment_Large;
streamParams.Environment = &environment;

SpatialAudioHrtfOrientation orientation = { 1,0,0,0,1,0,0,0,1 }; // identity matrix
streamParams.Orientation = &orientation;

PROPVARIANT pv;
PropVariantInit(&pv);
pv.vt = VT_BLOB;
pv.blob.cbSize = sizeof(streamParams);
pv.blob.pBlobData = (BYTE *)&streamParams;

hr = spatialAudioClient->ActivateSpatialAudioStream(&pv, __uuidof(spatialAudioStreamForHrtf), (void**)&spatialAudioStreamForHrtf);
```



<span data-ttu-id="8738a-222">Veja a seguir alguns códigos específicos do aplicativo necessários para dar suporte a esse exemplo, que gerará dinamicamente objetos de áudio posicionados aleatoriamente e os armazenará em um vetor.</span><span class="sxs-lookup"><span data-stu-id="8738a-222">The following is some app-specific code to needed support this example, which will dynamically spawn randomly positioned audio objects and store them in a vector.</span></span>


```C++
// Used for generating a vector of randomized My3DObject structs
std::vector<My3dObjectForHrtf> objectVector;
std::default_random_engine gen;
std::uniform_real_distribution<> pos_dist(-10, 10); // uniform distribution for random position
std::uniform_real_distribution<> vel_dist(-.02, .02); // uniform distribution for random velocity
std::uniform_real_distribution<> yRotation_dist(-3.14, 3.14); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> deltaYRotation_dist(.01, .02); // uniform distribution for y-axis rotation
std::uniform_real_distribution<> pitch_dist(40, 400); // uniform distribution for random pitch

int spawnCounter = 0;
```



<span data-ttu-id="8738a-223">Antes de entrar no loop de processamento de áudio, chame [**ISpatialAudioObjectRenderStreamForHrtf:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) para instruir o pipeline de mídia a começar a solicitar dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-223">Before entering the audio render loop, call [**ISpatialAudioObjectRenderStreamForHrtf::Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) to instruct the media pipeline to begin requesting audio data.</span></span>

<span data-ttu-id="8738a-224">Dentro do loop de processamento, aguarde o evento de conclusão de buffer que fornecemos quando o fluxo de áudio espacial foi inicializado para ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-224">Inside the render loop, wait for the buffer completion event we provided when the spatial audio stream was initialized to be signaled.</span></span> <span data-ttu-id="8738a-225">Você deve definir um limite de tempo limite razoável, como 100 ms, ao aguardar o evento, pois qualquer alteração no tipo de renderização ou no ponto de extremidade fará com que esse evento nunca seja sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8738a-225">You should set a reasonable timeout limit, like 100 ms, when waiting for the event because any change to the render type or endpoint will cause that event to never be signaled.</span></span> <span data-ttu-id="8738a-226">Nesse caso, você pode chamar [**ISpatialAudioRenderStreamForHrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) para tentar redefinir o fluxo de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-226">In this case, you can call [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) to attempt to reset the spatial audio stream.</span></span>

<span data-ttu-id="8738a-227">Em seguida, chame [**ISpatialAudioRenderStreamForHrtf:: BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) para permitir que o sistema saiba que você está prestes a preencher os buffers dos objetos de áudio com dados.</span><span class="sxs-lookup"><span data-stu-id="8738a-227">Next, call [**ISpatialAudioRenderStreamForHrtf::BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) to let the system know that you are about to fill the audio objects' buffers with data.</span></span> <span data-ttu-id="8738a-228">Esse método retorna o número de objetos de áudio dinâmicos disponíveis, não usados neste exemplo, e a contagem de quadros do buffer para objetos de áudio renderizados por esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="8738a-228">This method returns the number of available dynamic audio objects, not used in this example, and the frame count of the buffer for audio objects rendered by this stream.</span></span>

<span data-ttu-id="8738a-229">Sempre que o contador de geração atingir o valor especificado, ativaremos um novo objeto de áudio dinâmico chamando [**ISpatialAudioRenderStreamForHrtf:: ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) especificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span><span class="sxs-lookup"><span data-stu-id="8738a-229">Whenever the spawn counter reaches the specified value, we will activate a new dynamic audio object by calling [**ISpatialAudioRenderStreamForHrtf::ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) specifying [**AudioObjectType\_Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype).</span></span> <span data-ttu-id="8738a-230">Se todos os objetos de áudio dinâmico disponíveis já tiverem sido alocados, esse método retornará **SPLAUDCLNT \_ E \_ não \_ mais \_ objetos**.</span><span class="sxs-lookup"><span data-stu-id="8738a-230">If all available dynamic audio objects have already been allocated, this method will return **SPLAUDCLNT\_E\_NO\_MORE\_OBJECTS**.</span></span> <span data-ttu-id="8738a-231">Nesse caso, você pode optar por liberar um ou mais objetos de áudio ativados anteriormente com base em sua priorização específica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8738a-231">In this case, you can choose to release one or more previously activated audio objects based on your app-specific prioritization.</span></span> <span data-ttu-id="8738a-232">Depois que o objeto de áudio dinâmico tiver sido criado, ele será adicionado a uma nova estrutura **My3dObjectForHrtf** , com valores aleatórios de posição, rotação, velocidade, volume e frequência, que são adicionados à lista de objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="8738a-232">After the dynamic audio object has been created, it is added to a new **My3dObjectForHrtf** structure, with randomized position, rotation, velocity, volume, and frequency values, which is then added to the list of active objects.</span></span>

<span data-ttu-id="8738a-233">Em seguida, itere sobre todos os objetos ativos, representados neste exemplo com a estrutura **My3dObjectForHrtf** definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8738a-233">Next, iterate over all of the active objects, represented in this example with the app-defined **My3dObjectForHrtf** structure.</span></span> <span data-ttu-id="8738a-234">Para cada objeto de áudio, chame [**ISpatialAudioObjectForHrtf:: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) para obter um ponteiro para o buffer de áudio do objeto de áudio espacial.</span><span class="sxs-lookup"><span data-stu-id="8738a-234">For each audio object, call [**ISpatialAudioObjectForHrtf::GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) to get a pointer to the spatial audio object's audio buffer.</span></span> <span data-ttu-id="8738a-235">Esse método também retorna o tamanho do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="8738a-235">This method also returns the size of the buffer, in bytes.</span></span> <span data-ttu-id="8738a-236">O método auxiliar, **WriteToAudioObjectBuffer**, listado anteriormente neste artigo, para preencher o buffer com dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="8738a-236">The helper method, **WriteToAudioObjectBuffer**, listed previously in this article, to fill the buffer with audio data.</span></span> <span data-ttu-id="8738a-237">Depois de gravar no buffer, o exemplo atualiza a posição e a orientação do objeto de áudio HRTF chamando [**ISpatialAudioObjectForHrtf:: SETPOSITION**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) e [**ISpatialAudioObjectForHrtf:: setOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span><span class="sxs-lookup"><span data-stu-id="8738a-237">After writing to the buffer, the example updates the position and orientation of the HRTF audio object by calling [**ISpatialAudioObjectForHrtf::SetPosition**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) and [**ISpatialAudioObjectForHrtf::SetOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation).</span></span> <span data-ttu-id="8738a-238">Neste exemplo, um método auxiliar, **CalculateEmitterConeOrientationMatrix**, é usado para calcular a matriz de orientação de acordo com a direção que o objeto 3D está apontando.</span><span class="sxs-lookup"><span data-stu-id="8738a-238">In this example, a helper method, **CalculateEmitterConeOrientationMatrix**, is used to calculate the orientation matrix given the direction the 3D object is pointing.</span></span> <span data-ttu-id="8738a-239">A implementação desse método é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="8738a-239">The implementation of this method is shown below.</span></span> <span data-ttu-id="8738a-240">O volume do objeto de áudio também pode ser modificado chamando [**ISpatialAudioObjectForHrtf:: setlucro**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span><span class="sxs-lookup"><span data-stu-id="8738a-240">The volume of the audio object can also be modified by calling [**ISpatialAudioObjectForHrtf::SetGain**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain).</span></span> <span data-ttu-id="8738a-241">Se você não atualizar a posição, a orientação ou o volume do objeto, ele manterá a posição, a orientação e o volume da última vez que ele foi definido.</span><span class="sxs-lookup"><span data-stu-id="8738a-241">If you don't update the position, orientation, or volume of the object, it will retain the position, orientation, and volume from the last time it was set.</span></span> <span data-ttu-id="8738a-242">Se o tempo de vida definido pelo aplicativo do objeto tiver sido atingido, [**ISpatialAudioObjectForHrtf:: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) será chamado para permitir que o pipeline de áudio saiba que nenhum áudio será gravado usando esse objeto e o objeto será definido como **nullptr** para liberar seus recursos.</span><span class="sxs-lookup"><span data-stu-id="8738a-242">If the object's app-defined lifetime has been reached, [**ISpatialAudioObjectForHrtf::SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) is called to let the audio pipeline know that no more audio will be written using this object and the object is set to **nullptr** to free up its resources.</span></span>

<span data-ttu-id="8738a-243">Depois de gravar dados em todos os seus objetos de áudio, chame [**ISpatialAudioRenderStreamForHrtf:: EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) para permitir que o sistema saiba que os dados estão prontos para renderização.</span><span class="sxs-lookup"><span data-stu-id="8738a-243">After writing data to all of your audio objects, call [**ISpatialAudioRenderStreamForHrtf::EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) to let the system know the data is ready for rendering.</span></span> <span data-ttu-id="8738a-244">Você só pode chamar **GetBuffer** entre uma chamada para **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.</span><span class="sxs-lookup"><span data-stu-id="8738a-244">You can only call **GetBuffer** in between a call to **BeginUpdatingAudioObjects** and **EndUpdatingAudioObjects**.</span></span>


```C++
// Start streaming / rendering 
hr = spatialAudioStreamForHrtf->Start();

do
{
    // Wait for a signal from the audio-engine to start the next processing pass
    if (WaitForSingleObject(bufferCompletionEvent, 100) != WAIT_OBJECT_0)
    {
        break;
    }

    UINT32 availableDynamicObjectCount;
    UINT32 frameCount;

    // Begin the process of sending object data and metadata
    // Get the number of active objects that can be used to send object-data
    // Get the frame count that each buffer will be filled with 
    hr = spatialAudioStreamForHrtf->BeginUpdatingAudioObjects(&availableDynamicObjectCount, &frameCount);

    BYTE* buffer;
    UINT32 bufferLength;

    // Spawn a new dynamic audio object every 200 iterations
    if (spawnCounter % 200 == 0 && spawnCounter < 1000)
    {
        // Activate a new dynamic audio object
        Microsoft::WRL::ComPtr<ISpatialAudioObjectForHrtf> audioObject;
        hr = spatialAudioStreamForHrtf->ActivateSpatialAudioObjectForHrtf(AudioObjectType::AudioObjectType_Dynamic, &audioObject);

        // If SPTLAUDCLNT_E_NO_MORE_OBJECTS is returned, there are no more available objects
        if (SUCCEEDED(hr))
        {
            // Init new struct with the new audio object.
            My3dObjectForHrtf obj = { audioObject,
                Windows::Foundation::Numerics::float3(static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen)), static_cast<float>(pos_dist(gen))),
                Windows::Foundation::Numerics::float3(static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen)), static_cast<float>(vel_dist(gen))),
                static_cast<float>(static_cast<float>(yRotation_dist(gen))),
                static_cast<float>(static_cast<float>(deltaYRotation_dist(gen))),
                static_cast<float>(static_cast<float>(pitch_dist(gen))),
                format.nSamplesPerSec * 5 // 5 seconds of audio samples
            };

            objectVector.insert(objectVector.begin(), obj);
        }
    }
    spawnCounter++;

    // Loop through all dynamic audio objects
    std::vector<My3dObjectForHrtf>::iterator it = objectVector.begin();
    while (it != objectVector.end())
    {
        it->audioObject->GetBuffer(&buffer, &bufferLength);

        if (it->totalFrameCount >= frameCount)
        {
            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), frameCount, it->frequency, format.nSamplesPerSec);

            // Update the position and volume of the audio object
            it->audioObject->SetPosition(it->position.x, it->position.y, it->position.z);
            it->position += it->velocity;


            Windows::Foundation::Numerics::float3 emitterDirection = Windows::Foundation::Numerics::float3(cos(it->yRotationRads), 0, sin(it->yRotationRads));
            Windows::Foundation::Numerics::float3 listenerDirection = Windows::Foundation::Numerics::float3(0, 0, 1);
            DirectX::XMFLOAT4X4 rotationMatrix;

            DirectX::XMMATRIX rotation = CalculateEmitterConeOrientationMatrix(emitterDirection, listenerDirection);
            XMStoreFloat4x4(&rotationMatrix, rotation);

            SpatialAudioHrtfOrientation orientation = {
                rotationMatrix._11, rotationMatrix._12, rotationMatrix._13,
                rotationMatrix._21, rotationMatrix._22, rotationMatrix._23,
                rotationMatrix._31, rotationMatrix._32, rotationMatrix._33
            };

            it->audioObject->SetOrientation(&orientation);
            it->yRotationRads += it->deltaYRotation;

            it->totalFrameCount -= frameCount;

            ++it;
        }
        else
        {
            // If the audio object reaches its lifetime, set EndOfStream and release the object

            // Write audio data to the buffer
            WriteToAudioObjectBuffer(reinterpret_cast<float*>(buffer), it->totalFrameCount, it->frequency, format.nSamplesPerSec);

            // Set end of stream for the last buffer 
            hr = it->audioObject->SetEndOfStream(it->totalFrameCount);

            it->audioObject = nullptr; // Release the object

            it->totalFrameCount = 0;

            it = objectVector.erase(it);
        }
    }

    // Let the audio-engine know that the object data are available for processing now
    hr = spatialAudioStreamForHrtf->EndUpdatingAudioObjects();

} while (objectVector.size() > 0);
```



<span data-ttu-id="8738a-245">Quando você terminar de renderizar o áudio espacial, pare o fluxo de áudio espacial chamando [**ISpatialAudioRenderStreamForHrtf:: Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8738a-245">When you are done rendering spatial audio, stop the spatial audio stream by calling [**ISpatialAudioRenderStreamForHrtf::Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)).</span></span> <span data-ttu-id="8738a-246">Se você não pretende usar o fluxo novamente, libere seus recursos chamando [**ISpatialAudioRenderStreamForHrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8738a-246">If you are not going to use the stream again, free its resources by calling [**ISpatialAudioRenderStreamForHrtf::Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).</span></span>


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



<span data-ttu-id="8738a-247">O exemplo de código a seguir mostra a implementação do método auxiliar **CalculateEmitterConeOrientationMatrix** que foi usado no exemplo acima para calcular a matriz de orientação, considerando a direção em que o objeto 3D está apontando.</span><span class="sxs-lookup"><span data-stu-id="8738a-247">The following code example shows the implementation of the **CalculateEmitterConeOrientationMatrix** helper method which was used in the example above to calculate the orientation matrix given the direction the 3D object is pointing.</span></span>


```C++
DirectX::XMMATRIX CalculateEmitterConeOrientationMatrix(Windows::Foundation::Numerics::float3 listenerOrientationFront, Windows::Foundation::Numerics::float3 emitterDirection)
{
    DirectX::XMVECTOR vListenerDirection = DirectX::XMLoadFloat3(&listenerOrientationFront);
    DirectX::XMVECTOR vEmitterDirection = DirectX::XMLoadFloat3(&emitterDirection);
    DirectX::XMVECTOR vCross = DirectX::XMVector3Cross(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vDot = DirectX::XMVector3Dot(vListenerDirection, vEmitterDirection);
    DirectX::XMVECTOR vAngle = DirectX::XMVectorACos(vDot);
    float angle = DirectX::XMVectorGetX(vAngle);

    // The angle must be non-zero
    if (fabsf(angle) > FLT_EPSILON)
    {
        // And less than PI
        if (fabsf(angle) < DirectX::XM_PI)
        {
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }

        // If equal to PI, find any other non-collinear vector to generate the perpendicular vector to rotate about
        else
        {
            DirectX::XMFLOAT3 vector = { 1.0f, 1.0f, 1.0f };
            if (listenerOrientationFront.x != 0.0f)
            {
                vector.x = -listenerOrientationFront.x;
            }
            else if (listenerOrientationFront.y != 0.0f)
            {
                vector.y = -listenerOrientationFront.y;
            }
            else // if (_listenerOrientationFront.z != 0.0f)
            {
                vector.z = -listenerOrientationFront.z;
            }
            DirectX::XMVECTOR vVector = DirectX::XMLoadFloat3(&vector);
            vVector = DirectX::XMVector3Normalize(vVector);
            vCross = DirectX::XMVector3Cross(vVector, vEmitterDirection);
            return DirectX::XMMatrixRotationAxis(vCross, angle);
        }
    }

    // If the angle is zero, use an identity matrix
    return DirectX::XMMatrixIdentity();
}
```



## <a name="related-topics"></a><span data-ttu-id="8738a-248">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8738a-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8738a-249">Som espacial</span><span class="sxs-lookup"><span data-stu-id="8738a-249">Spatial Sound</span></span>](spatial-sound.md)
</dt> <dt>

[<span data-ttu-id="8738a-250">**ISpatialAudioClient**</span><span class="sxs-lookup"><span data-stu-id="8738a-250">**ISpatialAudioClient**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[<span data-ttu-id="8738a-251">**ISpatialAudioObject**</span><span class="sxs-lookup"><span data-stu-id="8738a-251">**ISpatialAudioObject**</span></span>](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
