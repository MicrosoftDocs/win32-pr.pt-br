---
description: Um pool de threads é uma coleção de threads de trabalho que executam com eficiência retornos de chamada assíncronos em nome do aplicativo.
ms.assetid: abe0798a-0b60-4bdb-a61e-45393f1e958d
title: Pools de threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7918a0f6f0b881233ebea8e664d6e743a7bff105e265270063b08af313417e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081256"
---
# <a name="thread-pools"></a>Pools de threads

Um *pool de threads* é uma coleção de threads de trabalho que executam com eficiência retornos de chamada assíncronos em nome do aplicativo. O pool de threads é usado principalmente para reduzir o número de threads do aplicativo e fornecer gerenciamento dos threads de trabalho. Os aplicativos podem enfileirar itens de trabalho, associar o trabalho a identificadores de espera, enfileirar automaticamente com base em um temporizador e associar a e/s.

## <a name="thread-pool-architecture"></a>Arquitetura do pool de threads

Os aplicativos a seguir podem se beneficiar do uso de um pool de threads:

-   Um aplicativo que é altamente paralelo e pode distribuir um grande número de itens de trabalho pequenos de forma assíncrona (como a pesquisa de índice distribuído ou e/s de rede).
-   Um aplicativo que cria e destrói um grande número de threads que cada um é executado por um curto período de tempo. O uso do pool de threads pode reduzir a complexidade do gerenciamento de threads e a sobrecarga envolvida na criação e destruição de threads.
-   Um aplicativo que processa itens de trabalho independentes em segundo plano e em paralelo (como carregar várias guias).
-   Um aplicativo que deve executar uma espera exclusiva em objetos de kernel ou bloquear eventos de entrada em um objeto. O uso do pool de threads pode reduzir a complexidade do gerenciamento de threads e aumentar o desempenho, reduzindo o número de alternâncias de contexto.
-   Um aplicativo que cria threads de WaIter personalizados para aguardar eventos.

o pool de threads original foi totalmente rearquitetado no Windows Vista. O novo pool de segmentos é melhorado porque fornece um único tipo de thread de trabalho (dá suporte a e/s e não e/s), não usa um thread de temporizador, fornece uma fila de temporizador único e fornece um thread persistente dedicado. Ele também fornece grupos de limpeza, melhor desempenho, vários pools por processo que são agendados de forma independente e uma nova API de pool de threads.

A arquitetura do pool de threads consiste no seguinte:

-   Threads de trabalho que executam as funções de retorno de chamada
-   Threads de WaIter que esperam em vários identificadores de espera
-   Uma fila de trabalho
-   Um pool de threads padrão para cada processo
-   Uma fábrica de trabalho que gerencia os threads de trabalho

## <a name="best-practices"></a>Práticas Recomendadas

A nova [API do pool de threads](thread-pool-api.md) fornece mais flexibilidade e controle do que a [API do pool de threads original](thread-pooling.md). No entanto, há algumas diferenças sutis, mas importantes. Na API original, a espera de redefinição era automática; na nova API, a espera deve ser redefinida explicitamente a cada vez. A API original tratou a representação automaticamente, transferindo o contexto de segurança do processo de chamada para o thread. Com a nova API, o aplicativo deve definir explicitamente o contexto de segurança.

Veja a seguir as práticas recomendadas ao usar um pool de threads:

-   Os threads de um processo compartilham o pool de threads. Um único thread de trabalho pode executar várias funções de retorno de chamada, uma de cada vez. Esses threads de trabalho são gerenciados pelo pool de threads. Portanto, não encerre um thread do pool de threads chamando [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) no thread ou chamando [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) de uma função de retorno de chamada.
-   Uma solicitação de e/s pode ser executada em qualquer thread no pool de threads. Cancelar a e/s em um thread de pool de threads requer sincronização porque a função de cancelamento pode ser executada em um thread diferente daquele que está tratando a solicitação de e/s, o que pode resultar em cancelamento de uma operação desconhecida. Para evitar isso, sempre forneça a estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) com a qual uma solicitação de e/s foi iniciada ao chamar [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) para e/s assíncrona, ou use sua própria sincronização para garantir que nenhuma outra e/s possa ser iniciada no thread de destino antes de chamar a função [**CancelSynchronousIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelsynchronousio) ou **CancelIoEx** .
-   Limpe todos os recursos criados na função de retorno de chamada antes de retornar da função. Isso inclui TLS, contextos de segurança, prioridade de thread e registro COM. As funções de retorno de chamada também devem restaurar o estado do thread antes de retornar.
-   Mantenha os identificadores de espera e seus objetos associados ativos até que o pool de threads tenha sinalizado que ele foi concluído com o identificador.
-   Marque todos os threads que estão aguardando por operações demoradas (como liberações de e/s ou limpeza de recursos) para que o pool de threads possa alocar novos threads em vez de aguardar este.
-   Antes de descarregar uma DLL que usa o pool de threads, cancele todos os itens de trabalho, e/s, operações de espera e temporizadores e aguarde a conclusão da execução de retornos de chamada.
-   Evite deadlocks eliminando as dependências entre os itens de trabalho e entre os retornos de chamada, garantindo que um retorno de chamada não esteja aguardando a conclusão dele e preservando a prioridade do thread.
-   Não enfileirar muitos itens muito rapidamente em um processo com outros componentes usando o pool de threads padrão. Há um pool de threads padrão por processo, incluindo Svchost.exe. Por padrão, cada pool de threads tem um máximo de 500 threads de trabalho. O pool de threads tenta criar mais threads de trabalho quando o número de threads de trabalho no estado pronto/em execução deve ser menor que o número de processadores.
-   Evite o modelo de apartamento de thread único COM, pois ele é incompatível com o pool de threads. O STA cria um estado de thread que pode afetar o próximo item de trabalho para o thread. O STA geralmente é de longa duração e tem afinidade de thread, que é o oposto do pool de threads.
-   Crie um novo pool de threads para controlar a prioridade e o isolamento do thread, criar características personalizadas e possivelmente melhorar a capacidade de resposta. No entanto, pools de threads adicionais exigem mais recursos do sistema (threads, memória do kernel). Um número excessivo de pools aumenta o potencial de contenção de CPU.
-   Se possível, use um objeto que pode ser aguardado em vez de um mecanismo baseado em APC para sinalizar um thread do pool de threads. O APCs não funciona bem com threads de pool de threads como outros mecanismos de sinalização porque o sistema controla o tempo de vida dos threads do pool de threads, de modo que é possível que um thread seja encerrado antes de a notificação ser entregue.
-   Use a extensão do depurador do pool de threads,! TP. Este comando tem o seguinte uso:

    -   *sinalizadores* de *endereço* do pool
    -   *sinalizadores* de *endereço* do obj
    -   *sinalizadores* de *endereço* Tnão
    -   *endereço* de WaIter
    -   *endereço* do trabalhador

    Para pool, WaIter e Worker, se o endereço for zero, o comando despejará todos os objetos. Para o WaIter e o trabalho, omitir o endereço despeja o thread atual. Os seguintes sinalizadores são definidos: 0x1 (saída de linha única), 0x2 (membros de despejo) e 0x4 (fila de trabalho do pool de despejo).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API do pool de threads](thread-pool-api.md)
</dt> <dt>

[Usando as funções do pool de threads](using-the-thread-pool-functions.md)
</dt> </dl>

 

 
