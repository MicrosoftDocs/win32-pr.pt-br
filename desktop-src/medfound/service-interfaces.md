---
description: Interfaces de serviço
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfaces de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31687cc1c1283eb59c7731743eaf4ece0127b392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780407"
---
# <a name="service-interfaces"></a>Interfaces de serviço

Algumas interfaces no Media Foundation devem ser obtidas chamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) em vez de chamando **QueryInterface**. O método [**GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funciona como QueryInterface, mas com as seguintes diferenças:

-   Ele usa um GUID de identificador de serviço além do identificador de interface.
-   Ele pode retornar um ponteiro para outro objeto que implementa a interface, em vez de retornar um ponteiro para o objeto original que é consultado.

> [!Note]  
> A interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) é muito semelhante à interface **IServiceProvider** usada em algumas outras APIs.

 

Um *serviço* é uma interface específica Obtida de uma determinada classe de objetos por meio da interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Os serviços a seguir são definidos.



| Identificador de serviço                          | Interface                                                                                                                                | Objetos que podem expor este serviço                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| \_serviço do \_ provedor de metadados MF \_             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Fontes de mídia                                                                                                                                     |
| \_serviço de mídia \_ MF                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Com suporte no Windows 8.1 e posterior.<br/>                                                                                                    |
| \_ \_ contexto do servidor PMP MF \_                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Sessão de mídia do PMP (caminho de mídia protegida).                                                                                                         |
| \_serviços de qualidade MF \_                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Fontes de mídia.                                                                                                                                    |
| \_serviço de \_ controle de taxa MF \_                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Fontes de mídia, sessão de mídia                                                                                                                      |
| \_serviço de \_ controle de taxa MF \_                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Fontes de mídia, coletores de mídia, sessão de mídia                                                                                                         |
| \_proxy remoto \_ MF                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxies para objetos remotos.                                                                                                                       |
| \_serviço de Sami MF \_                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Fonte de mídia SAMI (Media Interchange) sincronizada.                                                                                    |
| \_serviço do \_ provedor de apresentação de origem MF \_ \_ | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Origem do sequenciador                                                                                                                                  |
| \_serviço de código de caso MF \_                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Fonte de mídia ASF.                                                                                                                                 |
| \_serviço do \_ Editor de atributos TOPONODE \_ MF \_    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Sessão de mídia                                                                                                                                     |
| \_objeto inserido em MF \_                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Objetos encapsulados                                                                                                                                   |
| \_serviço de \_ buffer EMPACOTAdo MF \_                |                                                                                                                                          | Com suporte no Windows 8.1 e posterior.<br/>                                                                                                    |
| \_serv. \_ amostra ENCAPSULAdo MF \_                 |                                                                                                                                          | Com suporte no Windows 8.1 e posterior.<br/>                                                                                                    |
| serviços do MF \_ telefila \_                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Sessão de mídia                                                                                                                                     |
| \_serviço MFNET SAVEJOB \_                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Fluxos de bytes                                                                                                                                      |
| \_serviço de estatísticas do MFNETSOURCE \_            | **IPropertyStore**                                                                                                                       | Origem da rede. Use este serviço para recuperar as estatísticas de rede. Consulte [**a \_ Propriedade MFNETSOURCE Statistics**](mfnetsource-statistics-property.md). |
| \_serviço de \_ política de áudio do Mr \_                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Processador de áudio                                                                                                                                    |
| \_serviço de buffer do Mr \_                         | **IDirect3DSurface9**                                                                                                                    | Buffers de superfície DirectX                                                                                                                           |
| \_serviço de \_ volume da política de captura do Mr \_ \_        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Fonte de captura de áudio                                                                                                                              |
| \_serviço de \_ volume da política Mr \_                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Processador de áudio                                                                                                                                    |
| \_serviço de \_ volume de fluxo do Mr \_                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Processador de áudio                                                                                                                                    |
| \_serviço de \_ aceleração de vídeo Mr \_            | [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9), [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Processador de vídeo avançado (EVR)                                                                                                                     |
| \_serviço de \_ aceleração de vídeo Mr \_            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Pins de entrada no filtro EVR do DirectShow                                                                                                           |
| \_serviço de \_ aceleração de vídeo Mr \_            | [**Interface IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Coletores de fluxo EVR.                                                                                                                                 |
| \_serviço de \_ mixer de vídeo Mr \_                   | Várias interfaces expostas pelo mixer EVR. Consulte [usando os controles do mixer de vídeo](using-the-video-mixer-controls.md).                   | EVR                                                                                                                                               |
| \_serviço de \_ renderização de vídeo Mr \_                  | Várias interfaces expostas pelo apresentador EVR. Consulte [usando os controles de exibição de vídeo](using-the-video-display-controls.md).           | EVR                                                                                                                                               |



 

Você deve usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter as interfaces listadas nesta tabela dos objetos listados nesta tabela.

Em alguns casos, uma interface é retornada como um serviço por uma classe de objetos e retornada por meio de **QueryInterface** por outra classe de objetos. As páginas de referência para cada interface indicam quando usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) e quando usar **QueryInterface**.

> [!Caution]  
> Um objeto pode ser implementado de forma que ele retorne uma interface de serviço por meio de **QueryInterface** , bem como [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). No entanto, usar **QueryInterface** quando **GetService** for necessário pode levar a problemas de compatibilidade mais tarde.

 

A função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) é uma função auxiliar que consulta um objeto para [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e, em seguida, chama o método [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) do objeto.

## <a name="examples"></a>Exemplos

O exemplo a seguir consulta a sessão de mídia para [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e obtém a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .


```C++
IMFGetService *pGetService = NULL;
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = pMediaSession->QueryInterface(
    IID_IMFGetService, 
    (void**)&pGetService);

if (SUCCEEDED(hr))
{
    hr = pGetService->GetService(
        MF_RATE_CONTROL_SERVICE, 
        IID_IMFRateControl,
        (void**)&pRateControl);
}
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_REELEASE(pGetService);
SAFE_RELEASE(pRateControl);
```



O exemplo a seguir é equivalente ao exemplo anterior, mas usa a função [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) .


```C++
IMFRateControl *pRateControl = NULL;
HRESULT hr = S_OK;

hr = MFGetService(
    pMediaSession, 
    MF_RATE_CONTROL_SERVICE, 
    IID_IMFRateControl, 
    (void**) &pRateCtl 
); 
if (SUCCEEDED(hr))
{
    // Use IMFRateControl. (Not shown.)
}

// Clean up.
SAFE_RELEASE(pRateControl);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
</dt> <dt>

[APIs da plataforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 




