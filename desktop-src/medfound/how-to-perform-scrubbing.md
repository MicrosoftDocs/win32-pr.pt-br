---
description: Como executar a depuração
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Como executar a depuração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502200"
---
# <a name="how-to-perform-scrubbing"></a>Como executar a depuração

A depuração é executada para buscar instantaneamente pontos específicos dentro de um arquivo interagindo com uma representação visual de tempo, como uma barra de rolagem. No Media Foundation, a depuração significa procurar em um arquivo e obter um quadro atualizado.

Para obter informações sobre a depuração, consulte [sobre o controle de taxa](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>Para executar a depuração

1.  Chame [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) para obter a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) da [sessão de mídia](media-session.md).
    > [!Note]  
    > Não obtenha a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) da origem da mídia. Sempre obtenha a interface da sessão de mídia.

     

2.  Chame [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) para definir a taxa de reprodução como zero. Para obter mais informações sobre como chamar esse método, consulte [como definir a taxa de reprodução na sessão de mídia](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Crie uma posição de busca em um **PROPVARIANT** especificando o tempo de apresentação a ser buscado em um tipo **MFTIME** .
4.  Chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) com a posição de busca para iniciar a reprodução.
5.  Quando a operação de depuração for concluída, a sessão de mídia enviará um evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) . Aguarde esse evento antes de chamar [**Iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) novamente para outra operação de depuração.

## <a name="example"></a>Exemplo

O exemplo de código a seguir mostra como executar a depuração.


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



Uma operação de depuração bem-sucedida gera o evento [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) depois que todos os coletores de fluxo são atualizados com o novo quadro e a operação de depuração é concluída com êxito. Depurar um arquivo de vídeo exibe o quadro que foi buscado, mas não gera uma saída de áudio.

O aplicativo pode executar a revisão do quadro definindo a taxa de reprodução como zero e, em seguida, passando um **PROPVARIANT** que está definido como **VT \_ vazio** na chamada para [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Controle de taxa](rate-control.md)
</dt> </dl>

 

 



