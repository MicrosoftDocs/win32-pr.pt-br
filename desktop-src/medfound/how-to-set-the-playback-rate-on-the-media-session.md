---
description: Como definir a taxa de reprodução na sessão de mídia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Como definir a taxa de reprodução na sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696932d0da0147ba87e49cbc22d7ad53a525bc52c9bc2b3518c0f3e956a650aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465986"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Como definir a taxa de reprodução na sessão de mídia

Para implementar a funcionalidade de reprodução, como avanço rápido e rebobinar, os aplicativos talvez precisem alterar a taxa de reprodução de um fluxo de mídia. Media Foundation fornece o serviço de controle de taxa que os aplicativos devem usar para definir a taxa de reprodução dinamicamente.

Antes de definir a taxa de reprodução, um aplicativo deve verificar se a taxa é suportada pela fonte de mídia. Para obter informações sobre como consultar taxas com suporte, consulte [How to Determine Supported Rates](how-to-determine-supported-rates.md).

Para obter informações sobre taxas de reprodução, consulte [About Rate Control](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>Para definir a taxa de reprodução

1.  Chame [**MFGetService para**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) obter o objeto de controle de taxa da Sessão de Mídia.

    Os aplicativos [**que chamam MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) devem garantir o seguinte:

    -   O *parâmetro thebject* contém um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado.
    -   O objeto de controle de taxa recebido no *parâmetro ppvObject* é liberado para evitar vazamentos de memória.

2.  Chame o [**método IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para definir a taxa de reprodução. Depois **que SetRate** é concluído de forma assíncrona, o aplicativo recebe o [evento MESessionRateChanged.](mesessionratechanged.md)

## <a name="example"></a>Exemplo

O código a seguir mostra como definir a taxa de reprodução chamando o [**método SetRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate)


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



O aplicativo deve ser interrompido ou pausado antes de fazer uma transição de uma taxa negativa ou zero para uma taxa positiva. Para obter informações sobre esses estados, [consulte How to Control Presentation States](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, Avançar e reprodução inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



