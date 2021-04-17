---
description: O Microsoft Media Foundation dá suporte à captura de áudio e vídeo.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Captura de áudio/vídeo no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105789612"
---
# <a name="audiovideo-capture-in-media-foundation"></a>Captura de áudio/vídeo no Media Foundation

O Microsoft Media Foundation dá suporte à captura de áudio e vídeo. Os dispositivos de captura de vídeo têm suporte por meio do driver de classe UVC e devem ser compatíveis com o UVC 1,1. Os dispositivos de captura de áudio têm suporte por meio da API de sessão de áudio do Windows (WASAPI).

Um dispositivo de captura é representado em Media Foundation por um objeto de origem de mídia, que expõe a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . Na maioria dos casos, o aplicativo não usará essa interface diretamente, mas usará uma API de nível superior, como o [leitor de origem](source-reader.md) para controlar o dispositivo de captura.

## <a name="enumerate-capture-devices"></a>Enumerar dispositivos de captura

Para enumerar os dispositivos de captura no sistema, execute as seguintes etapas:

1.  Chame a função [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.
2.  Defina o atributo de [ \_ tipo de origem do \_ atributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) com um dos seguintes valores:

    | Valor                                                    | Descrição                      |
    |----------------------------------------------------------|----------------------------------|
    | **\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID** | Enumere dispositivos de captura de áudio. |
    | **\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ GUID** | Enumere dispositivos de captura de vídeo. |

    

     

3.  Chame a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Essa função aloca uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Cada ponteiro representa um objeto de ativação para um dispositivo no sistema.
4.  Chame o método [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar uma instância da fonte de mídia de um dos objetos de ativação.

O exemplo a seguir cria uma origem de mídia para o primeiro dispositivo de captura de vídeo na lista de enumeração:


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



Você pode consultar os objetos de ativação para vários atributos, incluindo o seguinte:

-   O atributo de [ \_ \_ \_ \_ nome amigável do atributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) contém o nome de exibição do dispositivo. O nome de exibição é adequado para mostrar ao usuário, mas pode não ser exclusivo.
-   Para dispositivos de vídeo, o atributo de [ \_ DEVSOURCE MF tipo de \_ \_ fonte VIDCAP de \_ \_ \_ \_ link simbólico](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contém o link simbólico para o dispositivo. O link simbólico identifica exclusivamente o dispositivo no sistema, mas não é uma cadeia de caracteres legível.
-   Para dispositivos de áudio, o atributo [MF \_ DEVSOURCE do tipo de \_ \_ fonte \_ \_ AUDCAP ponto de extremidade da \_ \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contém a ID do ponto de extremidade de áudio do dispositivo. A ID do ponto de extremidade de áudio é semelhante a um link simbólico. Ele identifica exclusivamente o dispositivo no sistema, mas não é uma cadeia de caracteres legível.

O exemplo a seguir usa uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e imprime o nome de exibição de cada dispositivo na janela de depuração:


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



Se você já souber o link simbólico para um dispositivo de vídeo, há outra maneira de criar a origem da mídia para o dispositivo:

1.  Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.
2.  Defina o atributo do [ \_ \_ \_ \_ tipo de origem DEVSOURCE](mf-devsource-attribute-source-type.md) do atributo MF como **MF \_ DEVSOURCE \_ atributo \_ Source \_ tipo \_ VIDCAP \_ GUID**.
3.  Defina o atributo de [ \_ \_ \_ \_ \_ \_ \_ link DEVSOURCE do tipo de origem MF VIDCAP](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) para o link simbólico.
4.  Chame a função [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . O primeiro retorna um ponteiro [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . O último retorna um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para um objeto de ativação. Você pode usar o objeto de ativação para criar a origem. (Um objeto de ativação pode ser empacotado para outro processo, portanto, será útil se você quiser criar a origem em outro processo. Para obter mais informações, consulte [Activation Objects](activation-objects.md).)

O exemplo a seguir usa o link simbólico de um dispositivo de vídeo e cria uma fonte de mídia.


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



Há uma maneira equivalente de criar um dispositivo de áudio a partir da ID do ponto de extremidade de áudio:

1.  Chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um repositório de atributos.
2.  Defina o atributo do [ \_ \_ \_ \_ tipo de origem DEVSOURCE](mf-devsource-attribute-source-type.md) do atributo MF como **MF \_ DEVSOURCE \_ atributo \_ Source \_ tipo \_ AUDCAP \_ GUID**.
3.  Defina o atributo de [ \_ ID de ponto de \_ \_ \_ \_ \_ extremidade \_ AUDCAP de DEVSOURCE MF](mf-devsource-attribute-source-type-audcap-endpoint-id.md) para a ID do ponto de extremidade.
4.  Chame a função [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

O exemplo a seguir usa uma ID de ponto de extremidade de áudio e cria uma origem de mídia.


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a>Usar um dispositivo de captura

Depois de criar a origem de mídia para um dispositivo de captura, use o [leitor de origem](source-reader.md) para obter dados do dispositivo. O leitor de origem fornece amostras de mídia que contêm os dados de áudio ou quadros de vídeo de captura. A próxima etapa depende do cenário do seu aplicativo:

-   Visualização de vídeo: Use Microsoft Direct3D ou Direct2D para exibir o vídeo.
-   Captura de arquivo: Use o [gravador de coletor](sink-writer.md) para codificar o arquivo.
-   Visualização de áudio: use [WASAPI](/windows/desktop/CoreAudio/wasapi).

Se você quiser combinar a captura de áudio com a captura de vídeo, use a *fonte de mídia agregada*. A fonte de mídia agregada contém uma coleção de fontes de mídia e combina todos os seus fluxos em um único objeto de origem de mídia. Para criar uma instância da fonte de mídia agregada, chame a função [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .

## <a name="shut-down-the-capture-device"></a>Desligar o dispositivo de captura

Quando o dispositivo de captura não for mais necessário, você deverá desligar o dispositivo chamando o [**desligamento**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) no objeto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) obtido chamando [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). A falha ao chamar o **desligamento** pode resultar em links de memória porque o sistema pode manter uma referência a recursos de **IMFMediaSource** até que o **desligamento** seja chamado.


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Se você alocou uma cadeia de caracteres que contém o link simbólico para um dispositivo de captura, deverá liberar esse objeto também.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> </dl>

 

 
