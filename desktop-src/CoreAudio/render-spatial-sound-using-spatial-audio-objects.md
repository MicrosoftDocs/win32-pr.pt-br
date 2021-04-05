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
# <a name="render-spatial-sound-using-spatial-audio-objects"></a>Renderizar som espacial usando objetos de áudio espaciais

Este artigo apresenta alguns exemplos simples que ilustram como implementar o som espacial usando objetos de áudio espacial estáticos, objetos de áudio espacial dinâmicos e objetos de áudio espacial que usam a função de transferência relativa de cabeçalho (HRTF) da Microsoft. As etapas de implementação para todas essas três técnicas são muito semelhantes e este artigo fornece um exemplo de código estruturado da mesma forma para cada técnica. Para obter exemplos completos de ponta a ponta de implementações de áudio espacial do mundo real, consulte [repositório do GitHub de exemplos de sons espaciais da Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio). Para obter uma visão geral do Windows Sonic, a solução em nível de plataforma da Microsoft para suporte a sons espaciais no Xbox e no Windows, consulte [som espacial](spatial-sound.md).

## <a name="render-audio-using-static-spatial-audio-objects"></a>Renderizar áudio usando objetos de áudio espacial estáticos

Um objeto de áudio estático é usado para processar o som para um dos 18 canais de áudio estáticos definidos na enumeração [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) . Cada um desses canais representa um palestrante real ou virtualizado em um ponto fixo no espaço que não é movido ao longo do tempo. Os canais estáticos que estão disponíveis em um determinado dispositivo dependem do formato de som espacial usado. Para obter uma lista dos formatos com suporte e suas contagens de canal, consulte [som espacial](spatial-sound.md).

Ao inicializar um fluxo de áudio espacial, você deve especificar quais dos canais estáticos disponíveis serão usados pelo fluxo. As definições de constante de exemplo a seguir podem ser usadas para especificar configurações comuns de alto-falante e obter o número de canais disponíveis para cada um.


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



A primeira etapa na renderização do áudio espacial é obter o ponto de extremidade de áudio para o qual os dados de áudio serão enviados. Crie uma instância de [**MMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chame [**GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obter o dispositivo de processamento de áudio padrão.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Ao criar um fluxo de áudio espacial, você deve especificar o formato de áudio que o fluxo usará, fornecendo uma estrutura [WAVEFORMATEX](../medfound/mf-mt-audio-prefer-waveformatex-attribute.md) . Se você estiver reproduzindo áudio de um arquivo, o formato normalmente será determinado pelo formato de arquivo de áudio. Este exemplo usa um formato mono, 32 bits, 48Hz.


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



A próxima etapa na renderização do áudio espacial é inicializar um fluxo de áudio espacial. Primeiro, obtenha uma instância de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Chame [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para certificar-se de que o formato de áudio que você está usando tem suporte. Crie um evento que o pipeline de áudio usará para notificar o aplicativo de que está pronto para mais dados de áudio.

Preencha uma estrutura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) que será usada para inicializar o fluxo de áudio espacial. Neste exemplo, o campo **StaticObjectTypeMask** é definido como a constante **de \_ estéreo ChannelMask** definida anteriormente neste artigo, o que significa que somente os canais frontal direito e esquerdo podem ser usados pelo fluxo de áudio. Como este exemplo usa apenas objetos de áudio estáticos e nenhum objeto dinâmico, o campo **MaxDynamicObjectCount** é definido como 0. O campo **categoria** é definido como um membro da enumeração [**de \_ \_ categoria de fluxo de áudio**](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) , que define como o sistema mistura o som desse fluxo com outras fontes de áudio.

Chame [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para ativar o fluxo.


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
> Ao usar as interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) em um título de XDK (Xbox One Development Kit), primeiro você deve chamar **EnableSpatialAudio** antes de chamar [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) ou [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). A falha em fazer isso resultará em um \_ erro E nointerface ser retornado da chamada para Activate. **EnableSpatialAudio** só está disponível para títulos XDK e não precisa ser chamado para plataforma universal do Windows aplicativos em execução no Xbox One, nem para nenhum dispositivo não Xbox.

 

Declare um ponteiro para um [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject) que será usado para gravar dados de áudio em um canal estático. Aplicativos típicos usarão um objeto para cada canal especificado no campo **StaticObjectTypeMask** . Para simplificar, este exemplo usa apenas um único objeto de áudio estático.


```C++
// In this simple example, one object will be rendered
Microsoft::WRL::ComPtr<ISpatialAudioObject> audioObjectFrontLeft;
```



Antes de entrar no loop de processamento de áudio, chame [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para instruir o pipeline de mídia a começar a solicitar dados de áudio. Este exemplo usa um contador para interromper a renderização de áudio após 5 segundos.

Dentro do loop de processamento, aguarde o evento de conclusão do buffer, fornecido quando o fluxo de áudio espacial foi inicializado, para ser sinalizado. Você deve definir um limite de tempo limite razoável, como 100 ms, ao aguardar o evento, pois qualquer alteração no tipo de renderização ou no ponto de extremidade fará com que esse evento nunca seja sinalizado. Nesse caso, você pode chamar [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para tentar redefinir o fluxo de áudio espacial.

Em seguida, chame [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para permitir que o sistema saiba que você está prestes a preencher os buffers dos objetos de áudio com dados. Esse método retorna o número de objetos de áudio dinâmicos disponíveis, não usados neste exemplo, e a contagem de quadros do buffer para objetos de áudio renderizados por esse fluxo.

Se um objeto de áudio espacial estático ainda não tiver sido criado, crie um ou mais chamando [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject), passando um valor da enumeração [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) indicando o canal estático para o qual o áudio do objeto é renderizado.

Em seguida, chame [**ISpatialAudioObject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obter um ponteiro para o buffer de áudio do objeto de áudio espacial. Esse método também retorna o tamanho do buffer, em bytes. Este exemplo usa um método auxiliar, **WriteToAudioObjectBuffer**, para preencher o buffer com dados de áudio. Esse método é mostrado posteriormente neste artigo. Depois de gravar no buffer, o exemplo verifica se o tempo de vida de 5 segundos do objeto foi atingido e, nesse caso, [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) é chamado para permitir que o pipeline de áudio saiba que nenhum outro áudio será gravado usando esse objeto e o objeto é definido como **nullptr** para liberar seus recursos.

Depois de gravar dados em todos os seus objetos de áudio, chame [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para permitir que o sistema saiba que os dados estão prontos para renderização. Você só pode chamar **GetBuffer** entre uma chamada para **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.


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



Quando você terminar de renderizar o áudio espacial, pare o fluxo de áudio espacial chamando [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Se você não pretende usar o fluxo novamente, libere seus recursos chamando [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream
hr = spatialAudioStream->Stop();

// Don't want to start again, so reset the stream to free its resources
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



O método auxiliar **WriteToAudioObjectBuffer** grava um buffer completo de exemplos ou o número de exemplos restantes especificados por nosso limite de tempo definido pelo aplicativo. Isso também pode ser determinado, por exemplo, pelo número de amostras restantes em um arquivo de áudio de origem. Uma onda Sin simples, a frequência que é dimensionada pelo parâmetro de entrada *Frequency* , é gerada e gravada no buffer.


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



## <a name="render-audio-using-dynamic-spatial-audio-objects"></a>Renderizar áudio usando objetos de áudio espacial dinâmico

Os objetos dinâmicos permitem que você processe o áudio de uma posição arbitrária no espaço, em relação ao usuário. A posição e o volume de um objeto de áudio dinâmico podem ser alterados ao longo do tempo. Normalmente, os jogos usarão a posição de um objeto 3D no mundo do jogo para especificar a posição do objeto de áudio dinâmico associado a ele. O exemplo a seguir usará uma estrutura simples, **My3dObject**, para armazenar o conjunto mínimo de dados necessários para representar um objeto. Esses dados incluem um ponteiro para um [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), a posição, a velocidade, o volume e a frequência de Tom para o objeto e um valor que armazena o número total de quadros para os quais o objeto deve renderizar o som.


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



As etapas de implementação para objetos de áudio dinâmicos são basicamente as mesmas que as etapas para objetos de áudio estáticos descritos acima. Primeiro, obtenha um ponto de extremidade de áudio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Em seguida, inicialize o fluxo de áudio espacial. Obtenha uma instância de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Chame [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para certificar-se de que o formato de áudio que você está usando tem suporte. Crie um evento que o pipeline de áudio usará para notificar o aplicativo de que está pronto para mais dados de áudio.

Chame [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar o número de objetos dinâmicos com suporte no sistema. Se essa chamada retornar 0, os objetos de áudio espacial dinâmico não têm suporte ou estão habilitados no dispositivo atual. Para obter informações sobre como habilitar o áudio espacial e obter detalhes sobre o número de objetos de áudio dinâmico disponíveis para diferentes formatos de áudio espacial, consulte [som espacial](spatial-sound.md).

Ao preencher a estrutura [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) , defina o campo **MaxDynamicObjectCount** para o número máximo de objetos dinâmicos que seu aplicativo usará.

Chame [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para ativar o fluxo.


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



Veja a seguir alguns códigos específicos do aplicativo necessários para dar suporte a esse exemplo, que gerará dinamicamente objetos de áudio posicionados aleatoriamente e os armazenará em um vetor.


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



Antes de entrar no loop de processamento de áudio, chame [**ISpatialAudioObjectRenderStream:: Start**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-start) para instruir o pipeline de mídia a começar a solicitar dados de áudio.

Dentro do loop de processamento, aguarde o evento de conclusão de buffer que fornecemos quando o fluxo de áudio espacial foi inicializado para ser sinalizado. Você deve definir um limite de tempo limite razoável, como 100 ms, ao aguardar o evento, pois qualquer alteração no tipo de renderização ou no ponto de extremidade fará com que esse evento nunca seja sinalizado. Nesse caso, você pode chamar [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset) para tentar redefinir o fluxo de áudio espacial.

Em seguida, chame [**ISpatialAudioObjectRenderStream:: BeginUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-beginupdatingaudioobjects) para permitir que o sistema saiba que você está prestes a preencher os buffers dos objetos de áudio com dados. Esse método retorna o número de objetos de áudio dinâmicos disponíveis e a contagem de quadros do buffer para objetos de áudio renderizados por esse fluxo.

Sempre que o contador de geração atingir o valor especificado, ativaremos um novo objeto de áudio dinâmico chamando [**ISpatialAudioObjectRenderStream:: ActivateSpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstream-activatespatialaudioobject) especificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Se todos os objetos de áudio dinâmico disponíveis já tiverem sido alocados, esse método retornará **SPLAUDCLNT \_ E \_ não \_ mais \_ objetos**. Nesse caso, você pode optar por liberar um ou mais objetos de áudio ativados anteriormente com base em sua priorização específica do aplicativo. Depois que o objeto de áudio dinâmico tiver sido criado, ele será adicionado a uma nova estrutura **My3dObject** , com posição aleatória, velocidade, volume e valores de frequência, que é então adicionado à lista de objetos ativos.

Em seguida, itere sobre todos os objetos ativos, representados neste exemplo com a estrutura **My3dObject** definida pelo aplicativo. Para cada objeto de áudio, chame [**ISpatialAudioObject:: GetBuffer**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-getbuffer) para obter um ponteiro para o buffer de áudio do objeto de áudio espacial. Esse método também retorna o tamanho do buffer, em bytes. O método auxiliar, **WriteToAudioObjectBuffer**, para preencher o buffer com dados de áudio. Depois de gravar no buffer, o exemplo atualiza a posição do objeto de áudio dinâmico chamando [**ISpatialAudioObject:: SETPOSITION**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setposition). O volume do objeto de áudio também pode ser modificado chamando [**SetVolume**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobject-setvolume). Se você não atualizar a posição ou o volume do objeto, ele reterá a posição e o volume da última vez que foi definido. Se o tempo de vida definido pelo aplicativo do objeto tiver sido atingido, [**ISpatialAudioObject:: SetEndOfStream**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectbase-setendofstream) será chamado para permitir que o pipeline de áudio saiba que nenhum áudio será gravado usando esse objeto e o objeto será definido como **nullptr** para liberar seus recursos.

Depois de gravar dados em todos os seus objetos de áudio, chame [**ISpatialAudioObjectRenderStream:: EndUpdatingAudioObjects**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-endupdatingaudioobjects) para permitir que o sistema saiba que os dados estão prontos para renderização. Você só pode chamar **GetBuffer** entre uma chamada para **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.


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



Quando você terminar de renderizar o áudio espacial, pare o fluxo de áudio espacial chamando [**ISpatialAudioObjectRenderStream:: Stop**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-stop). Se você não pretende usar o fluxo novamente, libere seus recursos chamando [**ISpatialAudioObjectRenderStream:: Reset**](/windows/win32/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioobjectrenderstreambase-reset).


```C++
// Stop the stream 
hr = spatialAudioStream->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStream->Reset();

CloseHandle(bufferCompletionEvent);
```



## <a name="render-audio-using-dynamic-spatial-audio-objects-for-hrtf"></a>Renderizar áudio usando objetos de áudio espacial dinâmico para HRTF

Outro conjunto de APIs, [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), permite o áudio espacial que usa a função de transferência relativa (HRTF) da Microsoft para atenuar sons a fim de simular a posição do emissor no espaço, em relação ao usuário, que pode ser alterado ao longo do tempo. Além da posição, os objetos de áudio HRTF permitem que você especifique uma orientação no espaço, um directivity no qual o som é emitido, como uma forma cônica ou cardioid, e um modelo decaimento à medida que o objeto se move mais próximo e além do ouvinte virtual. Observe que essas interfaces HRTF estão disponíveis apenas quando o usuário tiver selecionado o Windows Sonic para fones de ouvido como o mecanismo de áudio espacial do dispositivo. Para obter informações sobre como configurar um dispositivo para usar o Windows Sonic para fones de ouvido, consulte [som espacial](spatial-sound.md).

As APIs [**ISpatialAudioRenderStreamForHrtf**](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) e [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf) permitem que um aplicativo use explicitamente o caminho de renderização do Windows Sonic para fones de ouvido diretamente. Essas APIs não dão suporte a formatos de som espaciais, como Dolby Atmos for Home Theater ou Dolby Atmos para fones de ouvido, nem a alternância de formato de saída controlada pelo consumidor por meio do painel de controle de **som** , nem a reprodução de alto-falantes. Essas interfaces são destinadas ao uso em aplicativos do Windows Mixed Reality que desejam usar o Windows Sonic para recursos específicos de fones de ouvido (como predefinições ambientais e rolloff baseadas em distância especificadas de forma programática, fora dos pipelines de criação de conteúdo típicos). A maioria dos jogos e os cenários de realidade virtual preferem usar o [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) em vez disso. As etapas de implementação para ambos os conjuntos de API são quase idênticas, portanto, é possível implementar as duas tecnologias e alternar no tempo de execução, dependendo de qual recurso está disponível no dispositivo atual.

Aplicativos de realidade misturada normalmente usarão a posição de um objeto 3D no mundo virtual para especificar a posição do objeto de áudio dinâmico associado a ele. O exemplo a seguir usará uma estrutura simples, **My3dObjectForHrtf**, para armazenar o conjunto mínimo de dados necessários para representar um objeto. Esses dados incluem um ponteiro para um [**ISpatialAudioObjectForHrtf**](/windows/desktop/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectforhrtf), a posição, a orientação, a velocidade e a frequência de Tom do objeto, e um valor que armazena o número total de quadros para os quais o objeto deve renderizar o som.


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



As etapas de implementação para objetos de áudio dinâmicos HRTF são basicamente as mesmas que as etapas para objetos de áudio dinâmicos descritos na seção anterior. Primeiro, obtenha um ponto de extremidade de áudio.


```C++
HRESULT hr;
Microsoft::WRL::ComPtr<IMMDeviceEnumerator> deviceEnum;
Microsoft::WRL::ComPtr<IMMDevice> defaultDevice;

hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), nullptr, CLSCTX_ALL, __uuidof(IMMDeviceEnumerator), (void**)&deviceEnum);
hr = deviceEnum->GetDefaultAudioEndpoint(EDataFlow::eRender, eMultimedia, &defaultDevice);
```



Em seguida, inicialize o fluxo de áudio espacial. Obtenha uma instância de [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) chamando [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate). Chame [**ISpatialAudioClient:: IsAudioObjectFormatSupported**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-isaudioobjectformatsupported) para certificar-se de que o formato de áudio que você está usando tem suporte. Crie um evento que o pipeline de áudio usará para notificar o aplicativo de que está pronto para mais dados de áudio.

Chame [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para recuperar o número de objetos dinâmicos com suporte no sistema. Se essa chamada retornar 0, os objetos de áudio espacial dinâmico não têm suporte ou estão habilitados no dispositivo atual. Para obter informações sobre como habilitar o áudio espacial e obter detalhes sobre o número de objetos de áudio dinâmico disponíveis para diferentes formatos de áudio espacial, consulte [som espacial](spatial-sound.md).

Ao preencher a estrutura [**SpatialAudioHrtfActivationParams**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfactivationparams) , defina o campo **MaxDynamicObjectCount** para o número máximo de objetos dinâmicos que seu aplicativo usará. Os params de ativação para HRTF dão suporte a alguns parâmetros adicionais, como um [**SpatialAudioHrtfDistanceDecay**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdistancedecay), um [**SpatialAudioHrtfDirectivityUnion**](/windows/desktop/api/spatialaudiohrtf/ns-spatialaudiohrtf-spatialaudiohrtfdirectivityunion), um [**SpatialAudioHrtfEnvironmentType**](/windows/desktop/api/spatialaudiohrtf/ne-spatialaudiohrtf-spatialaudiohrtfenvironmenttype)e um [**SpatialAudioHrtfOrientation**](spatialaudiohrtforientation.md), que especificam os valores padrão dessas configurações para novos objetos criados a partir do fluxo. Esses parâmetros são opcionais. Defina os campos como **nullptr** para não fornecer nenhum valor padrão.

Chame [**ISpatialAudioClient:: ActivateSpatialAudioStream**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-activatespatialaudiostream) para ativar o fluxo.


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



Veja a seguir alguns códigos específicos do aplicativo necessários para dar suporte a esse exemplo, que gerará dinamicamente objetos de áudio posicionados aleatoriamente e os armazenará em um vetor.


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



Antes de entrar no loop de processamento de áudio, chame [**ISpatialAudioObjectRenderStreamForHrtf:: Start**](/previous-versions/windows/desktop/legacy/mt779304(v=vs.85)) para instruir o pipeline de mídia a começar a solicitar dados de áudio.

Dentro do loop de processamento, aguarde o evento de conclusão de buffer que fornecemos quando o fluxo de áudio espacial foi inicializado para ser sinalizado. Você deve definir um limite de tempo limite razoável, como 100 ms, ao aguardar o evento, pois qualquer alteração no tipo de renderização ou no ponto de extremidade fará com que esse evento nunca seja sinalizado. Nesse caso, você pode chamar [**ISpatialAudioRenderStreamForHrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)) para tentar redefinir o fluxo de áudio espacial.

Em seguida, chame [**ISpatialAudioRenderStreamForHrtf:: BeginUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779299(v=vs.85)) para permitir que o sistema saiba que você está prestes a preencher os buffers dos objetos de áudio com dados. Esse método retorna o número de objetos de áudio dinâmicos disponíveis, não usados neste exemplo, e a contagem de quadros do buffer para objetos de áudio renderizados por esse fluxo.

Sempre que o contador de geração atingir o valor especificado, ativaremos um novo objeto de áudio dinâmico chamando [**ISpatialAudioRenderStreamForHrtf:: ActivateSpatialAudioObjectForHrtf**](/windows/win32/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf-activatespatialaudioobjectforhrtf) especificando [**AudioObjectType \_ Dynamic**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype). Se todos os objetos de áudio dinâmico disponíveis já tiverem sido alocados, esse método retornará **SPLAUDCLNT \_ E \_ não \_ mais \_ objetos**. Nesse caso, você pode optar por liberar um ou mais objetos de áudio ativados anteriormente com base em sua priorização específica do aplicativo. Depois que o objeto de áudio dinâmico tiver sido criado, ele será adicionado a uma nova estrutura **My3dObjectForHrtf** , com valores aleatórios de posição, rotação, velocidade, volume e frequência, que são adicionados à lista de objetos ativos.

Em seguida, itere sobre todos os objetos ativos, representados neste exemplo com a estrutura **My3dObjectForHrtf** definida pelo aplicativo. Para cada objeto de áudio, chame [**ISpatialAudioObjectForHrtf:: GetBuffer**](/previous-versions/windows/desktop/legacy/mt779271(v=vs.85)) para obter um ponteiro para o buffer de áudio do objeto de áudio espacial. Esse método também retorna o tamanho do buffer, em bytes. O método auxiliar, **WriteToAudioObjectBuffer**, listado anteriormente neste artigo, para preencher o buffer com dados de áudio. Depois de gravar no buffer, o exemplo atualiza a posição e a orientação do objeto de áudio HRTF chamando [**ISpatialAudioObjectForHrtf:: SETPOSITION**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setposition) e [**ISpatialAudioObjectForHrtf:: setOrientation**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setorientation). Neste exemplo, um método auxiliar, **CalculateEmitterConeOrientationMatrix**, é usado para calcular a matriz de orientação de acordo com a direção que o objeto 3D está apontando. A implementação desse método é mostrada abaixo. O volume do objeto de áudio também pode ser modificado chamando [**ISpatialAudioObjectForHrtf:: setlucro**](/windows/desktop/api/spatialaudiohrtf/nf-spatialaudiohrtf-ispatialaudioobjectforhrtf-setgain). Se você não atualizar a posição, a orientação ou o volume do objeto, ele manterá a posição, a orientação e o volume da última vez que ele foi definido. Se o tempo de vida definido pelo aplicativo do objeto tiver sido atingido, [**ISpatialAudioObjectForHrtf:: SetEndOfStream**](/previous-versions/windows/desktop/legacy/mt779275(v=vs.85)) será chamado para permitir que o pipeline de áudio saiba que nenhum áudio será gravado usando esse objeto e o objeto será definido como **nullptr** para liberar seus recursos.

Depois de gravar dados em todos os seus objetos de áudio, chame [**ISpatialAudioRenderStreamForHrtf:: EndUpdatingAudioObjects**](/previous-versions/windows/desktop/legacy/mt779300(v=vs.85)) para permitir que o sistema saiba que os dados estão prontos para renderização. Você só pode chamar **GetBuffer** entre uma chamada para **BeginUpdatingAudioObjects** e **EndUpdatingAudioObjects**.


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



Quando você terminar de renderizar o áudio espacial, pare o fluxo de áudio espacial chamando [**ISpatialAudioRenderStreamForHrtf:: Stop**](/previous-versions/windows/desktop/legacy/mt779305(v=vs.85)). Se você não pretende usar o fluxo novamente, libere seus recursos chamando [**ISpatialAudioRenderStreamForHrtf:: Reset**](/previous-versions/windows/desktop/legacy/mt779303(v=vs.85)).


```C++
// Stop the stream 
hr = spatialAudioStreamForHrtf->Stop();

// We don't want to start again, so reset the stream to free it's resources.
hr = spatialAudioStreamForHrtf->Reset();

CloseHandle(bufferCompletionEvent);
```



O exemplo de código a seguir mostra a implementação do método auxiliar **CalculateEmitterConeOrientationMatrix** que foi usado no exemplo acima para calcular a matriz de orientação, considerando a direção em que o objeto 3D está apontando.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Som espacial](spatial-sound.md)
</dt> <dt>

[**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)
</dt> <dt>

[**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)
</dt> </dl>

 

 
