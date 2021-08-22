---
description: Os threads de streaming e de aplicativo
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Os threads de streaming e de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90916c14395a21aa5c53481c96b03fb6bbb2a8d4162cf996ef18ac15ce5e856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583116"
---
# <a name="the-streaming-and-application-threads"></a>Os threads de streaming e de aplicativo

Qualquer DirectShow aplicativo contém pelo menos dois threads importantes: o thread do aplicativo e um ou mais threads de streaming. Os exemplos são entregues nos threads de streaming e as alterações de estado ocorrem no thread do aplicativo. O thread de streaming principal é criado por um filtro de origem ou analisador. Outros filtros podem criar threads de trabalho que entregam exemplos, e eles também são considerados threads de streaming.

Alguns métodos são chamados no thread do aplicativo, enquanto outros são chamados em um thread de streaming. Por exemplo:

-   Thread(s) de streaming: [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Thread de aplicativo: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Qualquer um: [**IPin::NewSegment.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Ter um thread de streaming separado permite que os dados fluam pelo grafo enquanto o thread do aplicativo aguarda a entrada do usuário. O risco de vários threads, no entanto, é que um filtro pode criar recursos quando ele pausa (no thread do aplicativo), usá-los dentro de um método de streaming e destruir quando ele para (também no thread do aplicativo). Se você não tiver cuidado, o thread de streaming poderá tentar usar os recursos depois que eles são destruídos. A solução é proteger recursos usando seções críticas e sincronizar métodos de streaming com alterações de estado.

Um filtro precisa de uma seção crítica para proteger o estado do filtro. A [**classe CBaseFilter**](cbasefilter.md) tem uma variável de membro para esta seção crítica, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md). Esta seção crítica é chamada de bloqueio de filtro. Além disso, cada pino de entrada precisa de uma seção crítica para proteger os recursos usados pelo thread de streaming. Essas seções críticas são chamadas de bloqueios de streaming; você deve declare-os em sua classe de pin derivada. É mais fácil usar a [**classe CCritSec,**](ccritsec.md) que envolve um objeto **WINDOWS CRITICAL \_ SECTION** e pode ser bloqueada usando a [**classe CAutoLock.**](cautolock.md) A **classe CCritSec** também fornece algumas funções úteis de depuração. Para obter mais informações, consulte [Funções críticas de depuração de seção.](critical-section-debugging-functions.md)

Quando um filtro é interrompido ou liberado, ele deve sincronizar o thread do aplicativo com o thread de streaming. Para evitar o deadlock, ele deve primeiro desbloquear o thread de streaming, que pode ser bloqueado por vários motivos:

-   Ele está esperando para obter um exemplo dentro do método [**IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) porque todos os exemplos do alocador estão em uso.
-   Ele está aguardando outro filtro retornar de um método de streaming, como **Receber**.
-   Ele está aguardando dentro de um de seus próprios métodos de streaming, para que algum recurso se torne disponível.
-   É um filtro de renderização aguardando o tempo de apresentação do próximo exemplo
-   É um filtro do renderador aguardando dentro do **método Receive** durante a pausa.

Portanto, quando o filtro é interrompido ou liberado, ele deve fazer o seguinte:

-   Libere qualquer exemplo que ele está mantendo por qualquer motivo. Isso desbloqueia o **método GetBuffer.**
-   Retorne de qualquer método de streaming o mais rápido possível. Se um método de streaming estiver aguardando um recurso, ele deverá parar de esperar imediatamente.
-   Comece a rejeitar exemplos em **Receber**, para que o thread de streaming não acesse mais recursos. (A [**classe CBaseInputPin**](cbaseinputpin.md) lida com isso automaticamente.)
-   O **método Stop** deve delimitar todos os alocadores do filtro. (A **classe CBaseInputPin** lida com isso automaticamente.)

A liberação e a interrupção ocorrem no thread do aplicativo. Um filtro é interrompido em resposta ao [**método IMediaControl::Stop.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) O Gerenciador Graph Filtro emite o comando stop em ordem upstream, começando nos renderadores e trabalhando para trás para os filtros de origem. O comando stop ocorre completamente dentro do método **CBaseFilter::Stop do** filtro. Quando o método retorna, o filtro deve estar em um estado parado.

A liberação normalmente ocorre devido a um comando seek. Um comando de liberação começa no filtro de origem ou analisador e percorre downstream. A liberação ocorre em dois estágios: o método [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informa um filtro para descartar todos os dados pendentes e de entrada; O [**método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sinaliza o filtro para aceitar dados novamente. A liberação requer dois estágios porque **a chamada BeginFlush** está no thread do aplicativo, durante o qual o thread de streaming continua a fornecer dados. Portanto, alguns exemplos podem chegar após a **chamada BeginFlush.** O filtro deve descartá-los. Todos os exemplos que chegam após a **chamada endFlush** são garantidos como novos e devem ser entregues.

As seções a seguir contêm exemplos de código que mostram como implementar os métodos de filtro mais importantes, como **Pausar** **,** Receber e assim por diante, de maneiras que evitam deadlocks e condições de corrida. No entanto, cada filtro tem requisitos diferentes, portanto, você precisará adaptar esses exemplos ao filtro específico.

> [!Note]  
> As [**classes base CTransformFilter**](ctransformfilter.md) [**e CTransInPlaceFilter**](ctransinplacefilter.md) lidam com muitos dos problemas descritos neste artigo. Se você estiver escrevendo um filtro de transformação e seu filtro não aguardar eventos dentro de um método de streaming ou manter amostras fora de **Receber**, essas classes base deverão ser suficientes.

 

 

 



