---
description: Como determinar as taxas com suporte
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Como determinar as taxas com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aadbf0f9a0ce9608b58019d64ddb18a2227bbeb2941540086a6f998e40ebc3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878938"
---
# <a name="how-to-determine-supported-rates"></a>Como determinar as taxas com suporte

Antes de alterar a taxa de reprodução, um aplicativo deve verificar se a taxa de reprodução é suportada pelos objetos no pipeline. A interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fornece métodos para obter as taxas de avanço e inversa máximas, a taxa com suporte mais próxima de uma taxa solicitada e a taxa mais lenta. Cada uma dessas consultas de taxa pode especificar a direção de reprodução e se deve usar a afinação. A taxa de reprodução exata é consultada usando a interface [**IMFRateControl.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)

Para obter informações sobre como alterar as taxas de reprodução, [consulte How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).

Para obter informações gerais sobre taxas de reprodução, consulte [About Rate Control](about-rate-control.md).

## <a name="to-determine-the-current-playback-rate"></a>Para determinar a taxa de reprodução atual

1.  Obter o serviço de controle de taxa da Sessão de Mídia.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no *parâmetrobject de* [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

    O aplicativo deve consultar o serviço de controle de taxa por meio da Sessão de Mídia. Internamente, a Sessão de Mídia consulta os objetos na topologia.

2.  Chame o [**método IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) para obter a taxa de reprodução atual.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    O *parâmetro pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) recebe um **valor BOOL** que indica se o fluxo está sendo afinado no momento. O aplicativo deverá passar **NULL** se não quiser consultar o suporte de afinação para o fluxo. O *parâmetro pflRate* recebe a taxa de reprodução atual.

## <a name="to-determine-the-nearest-supported-rate"></a>Para determinar a taxa com suporte mais próxima

1.  Obter o serviço de suporte de taxa da Sessão de Mídia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no *parâmetrobject de* [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

2.  Chame o [**método IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) para recuperar a taxa com suporte mais próxima de uma taxa de reprodução solicitada.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    O exemplo consulta se há suporte para uma taxa de reprodução de 4,0 com a afinação. Isso é indicado passando **TRUE no** parâmetro *fThin* de [**IsRateSupported.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) Se essa taxa for suportada, *actualRate* conterá a taxa de reprodução de 4,0 e a chamada terá êxito com um valor de retorno de S \_ OK. Se a taxa de reprodução exata não for suportada, a taxa com suporte mais próxima será recebida em *actualRate*. Se a taxa não tiver suporte e não houver nenhuma taxa de reprodução mais próxima disponível, a chamada retornará um código de erro apropriado.

    Esses valores podem mudar dependendo de quais componentes de pipeline são carregados. Portanto, você deve consultar os valores novamente sempre que carregar uma nova topololgy.

    Se não há suporte para a taxa de reprodução desejada, uma opção é consultar cada objeto na topologia individualmente, para descobrir se um componente específico não dá suporte à taxa. Você pode recomilar a topologia sem esse componente e, em seguida, reproduzir na taxa desejada. Por exemplo, se cada componente, exceto o renderdor de áudio, for compatível com uma determinada taxa, você poderá recriar a topologia sem o branch de áudio e reproduzir na taxa desejada sem áudio.

## <a name="to-determine-the-slowest-supported-rate"></a>Para determinar a taxa com suporte mais lenta

1.  Obter o serviço de suporte de taxa da Sessão de Mídia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Passe um ponteiro de interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) inicializado no *parâmetrobject de* [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

2.  Chame o [**método IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) para recuperar a taxa com suporte mais lenta.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    O exemplo consulta a taxa de reprodução inversa mais lenta com a afinação. A taxa de limite inferior é recebida no *parâmetro slowestRate* de [**GetSlowestRate.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)

    Se não há suporte para reprodução inversa ou afinação, a chamada retorna um código de erro apropriado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[Busca, Avançar e reprodução inversa](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



