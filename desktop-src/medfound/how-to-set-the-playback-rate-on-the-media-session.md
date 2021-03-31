---
description: Como definir a taxa de reprodução na sessão de mídia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Como definir a taxa de reprodução na sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663779"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Como definir a taxa de reprodução na sessão de mídia

Para implementar a funcionalidade de reprodução, como avançar e retroceder, talvez os aplicativos precisem alterar a taxa de reprodução de um fluxo de mídia. Media Foundation fornece o serviço de controle de taxa que os aplicativos devem usar para definir a taxa de reprodução dinamicamente.

Antes de definir a taxa de reprodução, um aplicativo deve verificar se a taxa é suportada pela origem da mídia. Para obter informações sobre como consultar as taxas com suporte, consulte [como determinar as taxas com suporte](how-to-determine-supported-rates.md).

Para obter informações sobre taxas de reprodução, consulte [sobre o controle de taxa](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>Para definir a taxa de reprodução

1.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter o objeto de controle de taxa da sessão de mídia.

    Aplicativos que chamam [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) devem garantir o seguinte:

    -   O parâmetro *punkObject* contém um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado.
    -   O objeto de controle de taxa recebido no parâmetro *ppvObject* é liberado para evitar vazamentos de memória.

2.  Chame o método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para definir a taxa de reprodução. Após a conclusão da **taxa** de execução assíncrona, o aplicativo recebe o evento [MESessionRateChanged](mesessionratechanged.md) .

## <a name="example"></a>Exemplo

O código a seguir mostra como definir a taxa de reprodução chamando o método [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



O aplicativo deve ser interrompido ou pausado antes que possa fazer uma transição de uma taxa negativa ou zero para uma taxa positiva. Para obter informações sobre esses Estados, consulte [como controlar os Estados de apresentação](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, avanço rápido e reprodução reversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



