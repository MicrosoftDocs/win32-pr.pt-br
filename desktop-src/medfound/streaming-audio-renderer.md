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
# <a name="streaming-audio-renderer"></a>Processador de streaming de áudio

O SAR (processamento de áudio de streaming) é um coletor de mídia que renderiza áudio. Cada instância do SAR renderiza um fluxo de áudio único. Para renderizar vários fluxos, use várias instâncias do SAR.

Para criar o SAR, chame uma das seguintes funções:

-   [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer). Retorna um ponteiro para o SAR.
-   [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate). Retorna um ponteiro para um objeto de ativação, que pode ser usado para criar o SAR.

A segunda função, que retorna um objeto de ativação, é necessária se você estiver executando conteúdo protegido, pois o objeto de ativação deve ser serializado para o processo protegido. Para limpar conteúdo, você pode usar qualquer uma das funções.

O SAR pode receber áudio descompactado no formato de ponto flutuante PCM ou IEEE. Se a taxa de reprodução for mais rápida ou mais lenta que 1 ×, o SAR ajustará automaticamente o timbre.

## <a name="configuring-the-audio-renderer"></a>Configurando o processador de áudio

O SAR dá suporte a vários atributos de configuração. O mecanismo para definir esses atributos depende de qual função você chama para criar o SAR. Se você usar a função [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) , faça o seguinte:

1.  Crie um novo repositório de atributos chamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Adicione os atributos ao repositório de atributos.
3.  Passe o repositório de atributos para a função [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) no parâmetro *pAudioAttributes* .

Se você usar a função [**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) , a função retornará um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) no parâmetro *ppActivate* . Use esse ponteiro para adicionar os atributos.

Para obter uma lista de atributos de configuração, consulte [atributos do processador de áudio](audio-renderer-attributes.md).

## <a name="selecting-the-audio-endpoint-device"></a>Selecionando o dispositivo de ponto de extremidade de áudio

Um *dispositivo de ponto de extremidade de áudio* é um dispositivo de hardware que renderiza ou captura áudio. Os exemplos incluem alto-falantes, fones de ouvido, microfones e CD players. O SAR sempre usa um dispositivo de renderização de áudio. Há duas maneiras de selecionar o dispositivo.

A primeira abordagem é enumerar os dispositivos de renderização de áudio no sistema, usando a interface [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) . Essa interface está documentada na documentação da API de áudio principal.

1.  Crie o objeto enumerador de dispositivo.
2.  Use o enumerador de dispositivo para enumerar dispositivos de renderização de áudio. Cada dispositivo é representado por um ponteiro para a interface [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice) .
3.  Selecione um dispositivo, com base nas propriedades do dispositivo ou na seleção do usuário.
4.  Chame [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para obter o identificador do dispositivo.
5.  Defina o identificador do dispositivo como o valor do [**atributo \_ ID do \_ ponto de extremidade do atributo do processador \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) .

Em vez de enumerar dispositivos, você pode especificar o dispositivo de áudio por sua *função*. Uma função de áudio identifica uma categoria geral de uso. Por exemplo, a função de *console* é definida para jogos e notificações do sistema, enquanto a função de *multimídia* é definida para música e filmes. Cada função tem um dispositivo de renderização de áudio atribuído a ele e o usuário pode alterar essas atribuições. Se você especificar uma função de dispositivo, o SAR usará qualquer dispositivo de áudio atribuído para essa função. Para especificar a função de dispositivo, defina o atributo de [**\_ função de ponto de \_ extremidade do atributo de processamento \_ \_ \_ de áudio MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) .

Os dois atributos listados nesta seção são mutuamente exclusivos. Se você não definir nenhum deles, o SAR usará o dispositivo de áudio atribuído à função **eConsole** .

O código a seguir enumera os dispositivos de renderização de áudio e atribui o primeiro dispositivo na lista para o SAR. Este exemplo usa a função [**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer) para criar o SAR.


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



Para criar o objeto de ativação para o SAR, altere o código que aparece após a chamada para [**IMMDevice:: GetID**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) para o seguinte:


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

Uma sessão de áudio é um grupo de fluxos de áudio relacionados que um aplicativo pode gerenciar coletivamente. O aplicativo pode controlar o nível de volume e o estado de mudo de cada sessão. As sessões são identificadas por GUID. Para especificar a sessão de áudio para o SAR, use o atributo de [ID de sessão de atributo do \_ processador de áudio \_ \_ \_ \_ MF](mf-audio-renderer-attribute-session-id-attribute.md) . Se você não definir esse atributo, o SAR ingressará na sessão padrão para esse processo, identificado pelo **GUID \_ NULL**.

Por padrão, uma sessão de áudio é específica do processo, o que significa que ela contém somente fluxos do processo de chamada. Para ingressar em uma sessão de processo cruzado, defina o atributo de [sinalizadores de atributo do \_ processador de áudio \_ \_ \_ MF](mf-audio-renderer-attribute-flags-attribute.md) com o valor **MF \_ Audio processador de o \_ \_ atributo \_ flags \_ CROSSPROCESS**.

Depois de criar o SAR, você usa a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) para unir a sessão a um grupo de sessões, todas controladas pelo mesmo controle de volume no painel de controle. Você também pode usar essa interface para definir o nome de exibição e o ícone que aparecem no controle de volume.

## <a name="controlling-volume-levels"></a>Controlando os níveis de volume

Para controlar o nível de volume mestre de todos os fluxos na sessão de áudio do SAR, use a interface [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume) . Para controlar o volume de um fluxo individual ou para controlar o volume de canais individuais em um fluxo, use a interface [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume) . Ambas as interfaces são obtidas chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). Você pode chamar **GetService** diretamente no SAR ou chamá-lo na sessão de mídia. Os níveis de volume são expressos como valores de atenuação. Para cada canal, o nível de atenuação é o produto do volume mestre e do volume do canal.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reprodução de áudio/vídeo](audio-video-playback.md)
</dt> </dl>

 

 
