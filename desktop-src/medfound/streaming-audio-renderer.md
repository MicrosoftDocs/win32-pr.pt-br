---
description: O SAR (renderador de áudio de streaming) é um sink de mídia que renderiza áudio.
ms.assetid: 5884a128-597d-432b-a706-e10c894d7965
title: Renderização de áudio de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01752cbec7d801177b39d939baeca93f720e12aafeaf9845c1aa0ded033c3fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238261"
---
# <a name="streaming-audio-renderer"></a>Renderização de áudio de streaming

O SAR (renderador de áudio de streaming) é um sink de mídia que renderiza áudio. Cada instância da SAR renderiza um único fluxo de áudio. Para renderizar vários fluxos, use várias instâncias da SAR.

Para criar a SAR, chame uma das seguintes funções:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Retorna um ponteiro para o SAR.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Retorna um ponteiro para um objeto de ativação, que pode ser usado para criar a SAR.

A segunda função, que retorna um objeto de ativação, será necessária se você estiver tocando conteúdo protegido, pois o objeto de ativação deve ser serializado para o processo protegido. Para conteúdo não claro, você pode usar qualquer função.

A SAR pode receber áudio descompactado no formato de ponto flutuante PCM ou IEEE. Se a taxa de reprodução for mais rápida ou mais lenta que 1×, a SAR ajustará automaticamente a apresentação.

## <a name="configuring-the-audio-renderer"></a>Configurando o renderdor de áudio

O SAR dá suporte a vários atributos de configuração. O mecanismo para definir esses atributos depende de qual função você chama para criar a SAR. Se você usar a [**função MFCreateAudioRenderer,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) faça o seguinte:

1.  Crie um novo armazenamento de atributos chamando [**MFCreateAttributes.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes)
2.  Adicione os atributos ao armazenamento de atributos.
3.  Passe o armazenamento de atributos [**para a função MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) no *parâmetro pAudioAttributes.*

Se você usar a [**função MFCreateAudioRendererActivate,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) a função retornará um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) no *parâmetro ppActivate.* Use este ponteiro para adicionar os atributos.

Para ver uma lista de atributos de configuração, consulte [Atributos do renderdor de áudio.](audio-renderer-attributes.md)

## <a name="selecting-the-audio-endpoint-device"></a>Selecionando o dispositivo de ponto de extremidade de áudio

Um *dispositivo de ponto de extremidade de* áudio é um dispositivo de hardware que renderiza ou captura áudio. Exemplos incluem alto-falantes, fones de ouvido, microfones e players de CD. A SAR sempre usa um dispositivo de renderização de áudio. Há duas maneiras de selecionar o dispositivo.

A primeira abordagem é enumerar os dispositivos de renderização de áudio no sistema, usando a interface [**IMMDeviceEnumerator.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Essa interface está documentada na documentação principal da API de áudio.

1.  Crie o objeto de enumerador de dispositivo.
2.  Use o enumerador de dispositivo para enumerar dispositivos de renderização de áudio. Cada dispositivo é representado por um ponteiro para a interface [**IMMDevice.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
3.  Selecione um dispositivo, com base nas propriedades do dispositivo ou na seleção do usuário.
4.  Chame [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter o identificador do dispositivo.
5.  De definir o identificador do dispositivo como o valor do atributo [**MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ ENDPOINT \_ ID.**](mf-audio-renderer-attribute-endpoint-id-attribute.md)

Em vez de enumerar dispositivos, você pode especificar o dispositivo de áudio por sua *função*. Uma função de áudio identifica uma categoria geral de uso. Por exemplo, a função *de console* é definida para jogos e notificações do sistema, enquanto a função *multimídia* é definida para música e filmes. Cada função tem um dispositivo de renderização de áudio atribuído a ela e o usuário pode alterar essas atribuições. Se você especificar uma função de dispositivo, a SAR usará qualquer dispositivo de áudio atribuído a essa função. Para especificar a função de dispositivo, de definido o atributo [**MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ ENDPOINT \_ ROLE.**](mf-audio-renderer-attribute-endpoint-role-attribute.md)

Os dois atributos listados nesta seção são mutuamente exclusivos. Se você não definir nenhuma delas, a SAR usará o dispositivo de áudio atribuído à **função eConsole.**

O código a seguir enumera os dispositivos de renderização de áudio e atribui o primeiro dispositivo na lista à SAR. Este exemplo usa a [**função MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) para criar a SAR.


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



Para criar o objeto de ativação para o SAR, altere o código que aparece após a chamada para [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para o seguinte:


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



## <a name="selecting-the-audio-session"></a>Selecionando a sessão de áudio

Uma sessão de áudio é um grupo de fluxos de áudio relacionados que um aplicativo pode gerenciar coletivamente. O aplicativo pode controlar o nível de volume e o estado de mute de cada sessão. As sessões são identificadas pelo GUID. Para especificar a sessão de áudio para o SAR, use o atributo [MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE SESSION \_ \_ ID.](mf-audio-renderer-attribute-session-id-attribute.md) Se você não definir esse atributo, o SAR ingressará na sessão padrão desse processo, identificada por **GUID \_ NULL.**

Por padrão, uma sessão de áudio é específica do processo, o que significa que ela contém apenas fluxos do processo de chamada. Para ingressar em uma sessão entre processos, de definido o atributo [MF \_ AUDIO \_ RENDERER \_ ATTRIBUTE \_ FLAGS](mf-audio-renderer-attribute-flags-attribute.md) com o valor SINALIZADORES DE ATRIBUTO DO RENDERADOR DE ÁUDIO **MF \_ \_ \_ \_ \_ CROSSPROCESS**.

Depois de criar a SAR, use a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) para unir a sessão a um grupo de sessões, todas elas controladas pelo mesmo controle de volume no painel de controle. Você também pode usar essa interface para definir o nome de exibição e o ícone que aparecem no controle de volume.

## <a name="controlling-volume-levels"></a>Controlando níveis de volume

Para controlar o nível de volume mestre de todos os fluxos na sessão de áudio da SAR, use a interface [**IMFSimpleAudioVolume.**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) Para controlar o volume de um fluxo individual ou para controlar o volume de canais individuais dentro de um fluxo, use a interface [**IMFAudioStreamVolume.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) Ambas as interfaces são obtidas chamando [**IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Você pode chamar **GetService** diretamente no SAR ou chamá-lo na Sessão de Mídia. Os níveis de volume são expressos como valores de atenuação. Para cada canal, o nível de atenuação é o produto do volume mestre e do volume do canal.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 
