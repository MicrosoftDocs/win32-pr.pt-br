---
description: Como controlar os Estados de apresentação
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Como controlar os Estados de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763426"
---
# <a name="how-to-control-presentation-states"></a>Como controlar os Estados de apresentação

A sessão de mídia fornece controle de transporte, como a alteração de Estados de apresentação (reproduzir, pausar e parar em um cenário de reprodução estilo de playlist). Este tópico descreve os métodos de sessão de mídia que um aplicativo deve chamar para alterar o estado de reprodução.

A tabela a seguir mostra as transições de estado de apresentação válidas.



| Transição de estado | Descrição                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Reproduzir > pausar | O relógio de apresentação congela.                                                            |
| > de execução de reprodução  | O relógio de apresentação é redefinido.                                                           |
| Pausar-> reproduzir | O relógio de apresentação é retomado do tempo que froze durante a transição de reproduzir para pausar. |
| Pausar-> parar | O relógio de apresentação é redefinido.                                                           |
| Stop-> Play  | O relógio de apresentação começa desde o início da apresentação.                      |
| Parar > pausar | Não permitido.                                                                               |



 

## <a name="to-change-presentation-states"></a>Para alterar os Estados de apresentação

-   Chame o método [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) para pausar a reprodução.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Antes de chamar esse método, o aplicativo deve chamar o método [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) para descobrir se a origem da mídia dá suporte ao estado de pausa. Se tiver, esse método retornará **MFSESSIONCAP \_ Pause** no parâmetro *pdwCaps* .

    Pause interrompe temporariamente a sessão de mídia, o relógio de apresentação e o coletor de fluxo para a apresentação atual. Depois que a chamada for concluída com êxito, o aplicativo receberá um evento [MESessionPaused](mesessionpaused.md) .

-   Chame o método [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) para parar a reprodução.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Esse método interrompe a sessão de mídia interrompendo a origem da mídia, os relógios correspondentes e os coletores de fluxo. Se a sessão de mídia estiver controlando a [origem do sequenciador](sequencer-source.md), as fontes nativas subjacentes serão interrompidas pela origem do sequenciador. Depois que a sessão de mídia for interrompida, o aplicativo receberá um evento [MESessionStopped](mesessionstopped.md) .

-   Chame o método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar a reprodução ou buscar uma nova posição.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Esse método inicia a sessão de mídia dos Estados de pausa e parada. A sessão de mídia é responsável por configurar o fluxo de dados no pipeline. Esse método instrui a sessão de mídia a iniciar o relógio de apresentação. Após essa chamada, a sessão de mídia envia um evento [MESessionStarted](mesessionstarted.md) para o aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> </dl>

 

 



