---
description: Os threads de streaming e aplicativo
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Os threads de streaming e aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432e613ff0322377c042e796d84ef7affdda99c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506258"
---
# <a name="the-streaming-and-application-threads"></a>Os threads de streaming e aplicativo

Qualquer aplicativo do DirectShow contém pelo menos dois threads importantes: o thread do aplicativo e um ou mais threads de streaming. Os exemplos são entregues nos threads de streaming e as alterações de estado acontecem no thread do aplicativo. O thread de streaming principal é criado por um filtro de origem ou analisador. Outros filtros podem criar threads de trabalho que entregam amostras, e esses são considerados threads de streaming também.

Alguns métodos são chamados no thread do aplicativo, enquanto outros são chamados em um thread de streaming. Por exemplo:

-   Thread (s) de streaming: [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Thread do aplicativo: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking:: setposições**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Ou: [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Ter um thread de streaming separado permite que os dados fluam por meio do grafo, enquanto o thread do aplicativo aguarda a entrada do usuário. No entanto, o perigo de vários threads é que um filtro pode criar recursos quando pausa (no thread do aplicativo), usá-los dentro de um método de streaming e destruí-los quando ele parar (também no thread do aplicativo). Se você não tiver cuidado, o thread de streaming poderá tentar usar os recursos depois que eles forem destruídos. A solução é proteger os recursos usando seções críticas e sincronizar métodos de streaming com alterações de estado.

Um filtro precisa de uma seção crítica para proteger o estado do filtro. A classe [**CBaseFilter**](cbasefilter.md) tem uma variável de membro para essa seção crítica, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md). Essa seção crítica é chamada de bloqueio de filtro. Além disso, cada PIN de entrada precisa de uma seção crítica para proteger os recursos usados pelo thread de streaming. Essas seções críticas são chamadas de bloqueios de streaming; Você deve declará-los em sua classe de PIN derivada. É mais fácil usar a classe [**CCritSec**](ccritsec.md) , que encapsula um objeto de **\_ seção crítica** do Windows e pode ser bloqueado usando a classe [**CAutoLock**](cautolock.md) . A classe **CCritSec** também fornece algumas funções de depuração úteis. Para obter mais informações, consulte [funções críticas de depuração de seção](critical-section-debugging-functions.md).

Quando um filtro é interrompido ou liberado, ele deve sincronizar o thread do aplicativo com o thread de streaming. Para evitar deadlocks, primeiro ele deve desbloquear o thread de streaming, que pode ser bloqueado por vários motivos:

-   Está esperando obter um exemplo dentro do método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , pois todas as amostras do alocador estão em uso.
-   Ele está aguardando que outro filtro retorne de um método de streaming, como **Receive**.
-   Ele está esperando dentro de um de seus próprios métodos de streaming, para que algum recurso fique disponível.
-   É um filtro de processador aguardando o tempo de apresentação do próximo exemplo
-   É um filtro de processador esperando dentro do método **Receive** enquanto estiver em pausa.

Portanto, quando o filtro for interrompido ou liberado, ele deverá fazer o seguinte:

-   Libere qualquer amostra que esteja mantendo por qualquer motivo. Fazer isso desbloqueia o método **GetBuffer** .
-   Retornar de qualquer método de streaming o mais rápido possível. Se um método de streaming estiver aguardando um recurso, ele deverá parar de esperar imediatamente.
-   Comece a rejeitar amostras em **recebimento**, para que o thread de streaming não acesse mais recursos. (A classe [**CBaseInputPin**](cbaseinputpin.md) lida com isso automaticamente.)
-   O método **Stop** deve desconfirmar todos os alocadores do filtro. (A classe **CBaseInputPin** lida com isso automaticamente.)

A liberação e a interrupção de ambos acontecem no thread do aplicativo. Um filtro é interrompido em resposta ao método [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) . O Gerenciador de gráfico de filtro emite o comando parar na ordem de upstream, começando dos renderizadores e trabalhando de volta para os filtros de origem. O comando Stop ocorre completamente dentro do método **CBaseFilter:: Stop** do filtro. Quando o método retorna, o filtro deve estar em um estado parado.

A liberação normalmente ocorre devido a um comando de busca. Um comando flush inicia a partir do filtro de origem ou do analisador e viaja para o downstream. A liberação ocorre em dois estágios: o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informa um filtro para descartar todos os dados pendentes e recebidos; o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sinaliza o filtro para aceitar dados novamente. A liberação requer dois estágios porque a chamada **BeginFlush** está no thread do aplicativo, durante o qual o thread de streaming continua a entregar dados. Portanto, alguns exemplos podem chegar após a chamada **BeginFlush** . O filtro deve descartá-los. Todos os exemplos que chegam após a chamada de **EndFlush** são novos e devem ser entregues.

As seções a seguir contêm exemplos de código que mostram como implementar os métodos de filtro mais importantes, como **Pause**, **Receive** e assim por diante, de maneiras que evitem deadlocks e condições de corrida. No entanto, cada filtro tem requisitos diferentes, portanto, você precisará adaptar esses exemplos ao seu filtro específico.

> [!Note]  
> As classes base [**CTransformFilter**](ctransformfilter.md) e [**CTransInPlaceFilter**](ctransinplacefilter.md) lidam com muitos dos problemas descritos neste artigo. Se você estiver escrevendo um filtro de transformação e o filtro não aguardar eventos dentro de um método de streaming ou mantiver amostras fora do **recebimento**, essas classes base devem ser suficientes.

 

 

 



