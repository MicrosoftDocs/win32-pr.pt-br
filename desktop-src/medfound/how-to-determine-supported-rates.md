---
description: Como determinar as taxas com suporte
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Como determinar as taxas com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164841"
---
# <a name="how-to-determine-supported-rates"></a>Como determinar as taxas com suporte

Antes de alterar a taxa de reprodução, um aplicativo deve verificar se a taxa de reprodução é suportada pelos objetos no pipeline. A interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fornece métodos para obter as taxas máximas de avanço e reversão, a taxa com suporte mais próxima a uma taxa solicitada e a taxa mais lenta. Cada uma dessas consultas de taxa pode especificar a direção da reprodução e se deseja usar a fina. A taxa de reprodução exata é consultada usando a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .

Para obter informações sobre como alterar as taxas de reprodução, consulte [como definir a taxa de reprodução na sessão de mídia](how-to-set-the-playback-rate-on-the-media-session.md).

Para obter informações gerais sobre taxas de reprodução, consulte [sobre o controle de taxa](about-rate-control.md).

## <a name="to-determine-the-current-playback-rate"></a>Para determinar a taxa de reprodução atual

1.  Obtenha o serviço de controle de taxa da sessão de mídia.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no parâmetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    O aplicativo deve consultar o serviço de controle de taxa por meio da sessão de mídia. Internamente, a sessão de mídia consulta os objetos na topologia.

2.  Chame o método [**IMFRateControl:: GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) para obter a taxa de reprodução atual.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    O parâmetro *pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) recebe um valor **bool** que indica se o fluxo está sendo fino no momento. O aplicativo deve passar **nulo** se não quiser consultar o suporte de finamento para o fluxo. O parâmetro *pflRate* recebe a taxa de reprodução atual.

## <a name="to-determine-the-nearest-supported-rate"></a>Para determinar a taxa mais próxima com suporte

1.  Obtenha a taxa de serviço de suporte da sessão de mídia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no parâmetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Chame o método [**IMFRateSupport:: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) para recuperar a taxa com suporte mais próxima de uma taxa de reprodução solicitada.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    O exemplo consulta se uma taxa de reprodução de 4,0 tem suporte com finamento. Isso é indicado passando **true** no parâmetro *fThin* de [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported). Se essa taxa for suportada, *actualRate* conterá a taxa de reprodução de 4,0 e a chamada terá um valor de retorno de S \_ OK. Se a taxa de reprodução exata não for suportada, a taxa com suporte mais próxima será recebida em *actualRate*. Se a taxa não for suportada e não houver uma taxa de reprodução mais próxima disponível, a chamada retornará um código de erro apropriado.

    Esses valores podem ser alterados dependendo de quais componentes de pipeline são carregados. Portanto, você deve consultar os valores novamente sempre que carregar um novo topololgy.

    Se a taxa de reprodução desejada não for suportada, uma opção é consultar cada objeto na topologia individualmente para descobrir se um componente específico não oferece suporte à taxa. Talvez seja possível recriar a topologia sem esse componente e, em seguida, reproduzir a taxa desejada. Por exemplo, se cada componente, exceto o processador de áudio, der suporte a uma determinada taxa, você poderá recriar a topologia sem a ramificação de áudio e tocar na taxa desejada sem áudio.

## <a name="to-determine-the-slowest-supported-rate"></a>Para determinar a taxa com suporte mais lenta

1.  Obtenha a taxa de serviço de suporte da sessão de mídia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no parâmetro *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Chame o método [**IMFRateSupport:: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) para recuperar a taxa com suporte mais lenta.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    O exemplo consulta a taxa de reprodução inversa mais lenta com finamento. A taxa de limite inferior é recebida no parâmetro *slowestRate* de [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).

    Se a reprodução reversa ou a fina não for suportada, a chamada retornará um código de erro apropriado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, avanço rápido e reprodução reversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



