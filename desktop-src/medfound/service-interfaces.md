---
description: Interfaces de serviço
ms.assetid: 264a0e86-49e9-4777-956b-a83e9db52a25
title: Interfaces de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d99155eb5cfb8c435281a5f23567759931cc53fae3743d9c76ce7be75f68c380
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060406"
---
# <a name="service-interfaces"></a>Interfaces de serviço

Algumas interfaces no Media Foundation devem ser obtidas chamando [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) em vez de chamando **QueryInterface**. O [**método GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) funciona como QueryInterface, mas com as seguintes diferenças:

-   Ele leva um GUID do identificador de serviço além do identificador de interface.
-   Ele pode retornar um ponteiro para outro objeto que implementa a interface, em vez de retornar um ponteiro para o objeto original consultado.

> [!Note]  
> A interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) é muito semelhante à interface **IServiceProvider** usada em algumas outras APIs.

 

Um *serviço* é uma interface específica obtida de uma classe específica de objetos por meio da interface [**IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) Os serviços a seguir são definidos.



| Identificador de serviço                          | Interface                                                                                                                                | Objetos que podem expor esse serviço                                                                                                            |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| SERVIÇO DE PROVEDOR \_ DE METADADOS MF \_ \_             | [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)                                                                                       | Fontes de mídia                                                                                                                                     |
| MF \_ MEDIASOURCE \_ SERVICE                    | [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                                                                                                 | Com suporte no Windows 8.1 e posterior.<br/>                                                                                                    |
| CONTEXTO DO \_ SERVIDOR MF PMP \_ \_                    | [**IMFPMPServer**](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver)                                                                                                     | Sessão de mídia PMP (caminho de mídia protegido).                                                                                                         |
| MF \_ QUALITY \_ SERVICES                       | [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                                                                                             | Fontes de mídia.                                                                                                                                    |
| SERVIÇO DE CONTROLE \_ DE TAXA \_ DE MF \_                  | [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)                                                                                                 | Fontes de mídia, Sessão de Mídia                                                                                                                      |
| SERVIÇO DE CONTROLE \_ DE TAXA \_ DE MF \_                  | [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                                                                                                 | Fontes de mídia, sinks de mídia, Sessão de Mídia                                                                                                         |
| PROXY \_ REMOTO MF \_                           | [**IMFRemoteProxy**](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy)                                                                                                 | Proxies para objetos remotos.                                                                                                                       |
| SERVIÇO \_ SAMI do MF \_                           | [**IMFSAMIStyle**](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)                                                                                                     | Fonte de mídia SAMI (Intercâmbio de Mídia Acessível Sincronizado).                                                                                    |
| SERVIÇO DE PROVEDOR \_ DE \_ APRESENTAÇÃO DE ORIGEM \_ MF \_ | [**IMFMediaSourcePresentationProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider)                                                         | Origem do sequencer                                                                                                                                  |
| SERVIÇO MF \_ TIMECODE \_                       | [**IMFTimecodeTranslate**](/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate)                                                                                     | Fonte de mídia do ASF.                                                                                                                                 |
| SERVIÇO EDITOR \_ DE ATRIBUTO TOPONODE \_ \_ DO \_ MF    | [**IMFTopologyNodeAttributeEditor**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor)                                                                 | Sessão de mídia                                                                                                                                     |
| OBJETO \_ EMPACOTADO MF \_                         | [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)                                                                                                   | Objetos empacotados                                                                                                                                   |
| SERVIÇO DE \_ \_ BUFFER EMPACOTADO MF \_                |                                                                                                                                          | Com suporte no Windows 8.1 e posterior.<br/>                                                                                                    |
| SERVIÇO DE EXEMPLO DE MF \_ WRAPPED \_ \_                 |                                                                                                                                          | Com suporte no Windows 8.1 e posterior.<br/>                                                                                                    |
| SERVIÇOS \_ DE MF \_ WORKQUEUE                     | [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)                                                                                     | Sessão de mídia                                                                                                                                     |
| MFNET \_ SAVEJOB \_ SERVICE                     | [**IMFSaveJob**](/windows/desktop/api/mfidl/nn-mfidl-imfsavejob)                                                                                                         | Fluxos de byte                                                                                                                                      |
| SERVIÇO DE ESTATÍSTICAS MFNETSOURCE \_ \_            | **Ipropertystore**                                                                                                                       | Origem da rede. Use esse serviço para recuperar estatísticas de rede. Consulte [**Propriedade \_ STATISTICS MFNETSOURCE**](mfnetsource-statistics-property.md). |
| SERVIÇO \_ DE POLÍTICA DE ÁUDIO \_ DO MR \_                  | [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)                                                                                                 | Renderdor de áudio                                                                                                                                    |
| SERVIÇO \_ DE BUFFER DO MR \_                         | **IDirect3DSurface9**                                                                                                                    | Buffers de superfície do DirectX                                                                                                                           |
| SERVIÇO \_ DE VOLUME DA POLÍTICA DE CAPTURA DO \_ \_ \_ MR        | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Origem da captura de áudio                                                                                                                              |
| SERVIÇO DE \_ VOLUME DE \_ POLÍTICA DO MR \_                 | [**IMFSimpleAudioVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume)                                                                                     | Renderdor de áudio                                                                                                                                    |
| SERVIÇO DE \_ VOLUME DE FLUXO \_ \_ DO MR                 | [**IMFAudioStreamVolume**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume)                                                                                     | Renderdor de áudio                                                                                                                                    |
| SERVIÇO DE \_ \_ ACELERAÇÃO DE VÍDEO DO MR \_            | [**IDirect3DDeviceManager9,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) [ **IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice) | Renderização de vídeo aprimorada (EVR)                                                                                                                     |
| SERVIÇO DE \_ \_ ACELERAÇÃO DE VÍDEO DO MR \_            | [**IDirectXVideoMemoryConfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)                                                             | Pinos de entrada no filtro DirectShow EVR                                                                                                           |
| SERVIÇO DE \_ \_ ACELERAÇÃO DE VÍDEO DO MR \_            | [**IMFVideoSampleAllocator Interface**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator)                                                                     | Sinks de fluxo EVR.                                                                                                                                 |
| SERVIÇO MIXER \_ \_ DE VÍDEO \_ DO MR                   | Várias interfaces expostas pelo mixer EVR. Consulte [Usando os controles de Mixer vídeo](using-the-video-mixer-controls.md).                   | Evr                                                                                                                                               |
| SERVIÇO \_ DE \_ RENDERIZAÇÃO DE VÍDEO \_ DO MR                  | Várias interfaces expostas pelo apresentador de EVR. Consulte [Usando os controles de exibição de vídeo](using-the-video-display-controls.md).           | Evr                                                                                                                                               |



 

Você deve usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter as interfaces listadas nesta tabela dos objetos listados nesta tabela.

Em alguns casos, uma interface é retornada como um serviço por uma classe de objetos e retornada por **meio de QueryInterface** por outra classe de objetos. As páginas de referência para cada interface indicam quando usar [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) e quando usar **QueryInterface**.

> [!Caution]  
> Um objeto pode ser implementado de forma que ele retorne uma interface de serviço por meio de **QueryInterface,** bem como [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice). No entanto, usar **QueryInterface** quando **GetService** for necessário pode levar a problemas de compatibilidade mais tarde.

 

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

 

 




