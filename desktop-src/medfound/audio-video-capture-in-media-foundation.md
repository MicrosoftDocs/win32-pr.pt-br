---
description: Microsoft Media Foundation dá suporte à captura de áudio e vídeo.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Captura de áudio/vídeo no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cf225c8e11823779a401288135017d119fe67e4cd32fa39b54f3cd39b7bb45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880901"
---
# <a name="audiovideo-capture-in-media-foundation"></a>Captura de áudio/vídeo no Media Foundation

Microsoft Media Foundation dá suporte à captura de áudio e vídeo. Os dispositivos de captura de vídeo têm suporte por meio do driver de classe UVC e devem ser compatíveis com o UVC 1.1. Há suporte para dispositivos de captura de áudio Windows API de Sessão de Áudio (WASAPI).

Um dispositivo de captura é representado Media Foundation objeto de origem de mídia, que expõe a interface [**IMFMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) Na maioria dos casos, o aplicativo não usará essa interface diretamente, [](source-reader.md) mas usará uma API de nível superior, como o Leitor de Origem, para controlar o dispositivo de captura.

## <a name="enumerate-capture-devices"></a>Enumerar dispositivos de captura

Para enumerar os dispositivos de captura no sistema, execute as seguintes etapas:

1.  Chame a [**função MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um armazenamento de atributos.
2.  De definir [o atributo \_ MF DEVSOURCE \_ ATTRIBUTE SOURCE \_ \_ TYPE](mf-devsource-attribute-source-type.md) como um dos seguintes valores:

    | Valor                                                    | Descrição                      |
    |----------------------------------------------------------|----------------------------------|
    | **GUID \_ \_ \_ \_ \_ AUDCAP DO TIPO DE ORIGEM DO ATRIBUTO MF DEVSOURCE \_** | Enumerar dispositivos de captura de áudio. |
    | **GUID \_ VIDCAP DO TIPO \_ DE ORIGEM DO ATRIBUTO \_ \_ \_ MF \_ DEVSOURCE** | Enumerar dispositivos de captura de vídeo. |

    

     

3.  Chame a [**função MFEnumDeviceSources.**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) Essa função aloca uma matriz de [**ponteiros IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Cada ponteiro representa um objeto de ativação para um dispositivo no sistema.
4.  Chame o [**método IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) para criar uma instância da fonte de mídia de um dos objetos de ativação.

O exemplo a seguir cria uma fonte de mídia para o primeiro dispositivo de captura de vídeo na lista de enumeração:


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

-   O [atributo MF \_ DEVSOURCE \_ ATTRIBUTE FRIENDLY \_ \_ NAME](mf-devsource-attribute-friendly-name.md) contém o nome de exibição do dispositivo. O nome de exibição é adequado para mostrar ao usuário, mas pode não ser exclusivo.
-   Para dispositivos de vídeo, o atributo [MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ SYMBOLIC \_ LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contém o link simbólico para o dispositivo. O link simbólico identifica exclusivamente o dispositivo no sistema, mas não é uma cadeia de caracteres acessível.
-   Para dispositivos de áudio, o atributo [ \_ MF DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ AUDCAP \_ ENDPOINT ID \_ ](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contém a ID do ponto de extremidade de áudio do dispositivo. A ID do ponto de extremidade de áudio é semelhante a um link simbólico. Ele identifica exclusivamente o dispositivo no sistema, mas não é uma cadeia de caracteres acessível.

O exemplo a seguir pega uma matriz [**de ponteiros IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e imprime o nome de exibição de cada dispositivo na janela de depuração:


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



Se você já conhece o link simbólico para um dispositivo de vídeo, há outra maneira de criar a fonte de mídia para o dispositivo:

1.  Chame [**MFCreateAttributes para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) criar um armazenamento de atributos.
2.  De definir o [atributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE \_ \_ TYPE](mf-devsource-attribute-source-type.md) como **MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ GUID**.
3.  Definir o [atributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ SYMBOLIC \_ LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) como o link simbólico.
4.  Chame a [**função MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) [**ou MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) O primeiro retorna um [**ponteiro IMFMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) O último retorna um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para um objeto de ativação. Você pode usar o objeto de ativação para criar a origem. (Um objeto de ativação pode ser marshalado para outro processo, portanto, é útil se você quiser criar a origem em outro processo. Para obter mais informações, consulte [Objetos de ativação](activation-objects.md).)

O exemplo a seguir pega o link simbólico de um dispositivo de vídeo e cria uma fonte de mídia.


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



Há uma maneira equivalente de criar um dispositivo de áudio com a ID do ponto de extremidade de áudio:

1.  Chame [**MFCreateAttributes para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) criar um armazenamento de atributos.
2.  De definir o [atributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE \_ \_ TYPE](mf-devsource-attribute-source-type.md) como **MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ AUDCAP \_ GUID**.
3.  De definir o [atributo MF \_ DEVSOURCE \_ TIPO DE \_ ORIGEM \_ \_ AUDCAP \_ \_ ENDPOINT ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) como a ID do ponto de extremidade.
4.  Chame a [**função MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) [**ou MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)

O exemplo a seguir pega uma ID de ponto de extremidade de áudio e cria uma fonte de mídia.


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

Depois de criar a fonte de mídia para um dispositivo de captura, use o [Leitor de Origem](source-reader.md) para obter dados do dispositivo. O Leitor de Origem fornece exemplos de mídia que contêm os quadros de vídeo ou dados de áudio de captura. A próxima etapa depende do cenário do aplicativo:

-   Visualização de vídeo: use o Microsoft Direct3D ou Direct2D para exibir o vídeo.
-   Captura de arquivo: use o [Sink Writer](sink-writer.md) para codificar o arquivo.
-   Visualização de áudio: use [WASAPI](/windows/desktop/CoreAudio/wasapi).

Se você quiser combinar a captura de áudio com captura de vídeo, use a fonte *de mídia agregada*. A fonte de mídia de agregação contém uma coleção de fontes de mídia e combina todos os seus fluxos em um único objeto de fonte de mídia. Para criar uma instância da fonte de mídia de agregação, chame a [**função MFCreateAggregateSource.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource)

## <a name="shut-down-the-capture-device"></a>Desligar o dispositivo de captura

Quando o dispositivo de captura não for mais necessário, você deverá desligar o dispositivo chamando [**Desligamento**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) no objeto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) obtido chamando [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) ou [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). A falha ao **chamar Desligamento** pode resultar em links de memória porque o sistema pode manter uma referência aos recursos **de IMFMediaSource** até **que o desligamento** seja chamado.


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Se você tiver alocado uma cadeia de caracteres que contém o link simbólico para um dispositivo de captura, deverá liberar esse objeto também.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> </dl>

 

 
