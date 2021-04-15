---
description: Os componentes geralmente são projetados para executar tarefas de inicialização quando são chamados pela primeira vez, em vez de quando são carregados.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: Inicialização de One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f451e3c51716b4ff6f33b55d8d8602b5d5c28f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753699"
---
# <a name="one-time-initialization"></a>Inicialização de One-Time

Os componentes geralmente são projetados para executar tarefas de inicialização quando são chamados pela primeira vez, em vez de quando são carregados. As funções de inicialização única garantem que essa inicialização ocorra apenas uma vez, mesmo quando vários threads podem tentar a inicialização.

**Windows Server 2003 e Windows XP:** Os aplicativos devem fornecer sua própria sincronização para inicialização única usando as [funções](interlocked-variable-access.md) interligadas ou outro mecanismo de sincronização. As funções de inicialização única estão disponíveis a partir do Windows Vista e do Windows Server 2008.

As funções de inicialização única fornecem vantagens significativas para garantir que apenas um thread execute a inicialização:

-   Eles são otimizados para velocidade.
-   Eles criam as barreiras apropriadas em arquiteturas de processador que os exigem.
-   Eles dão suporte a inicialização bloqueada e paralela.
-   Eles evitam o bloqueio interno para que o código possa operar de forma assíncrona ou síncrona.

O sistema gerencia o processo de inicialização por meio de uma estrutura de **inicialização opaca \_ uma vez** que contém dados e informações de estado. O chamador aloca essa estrutura e a inicializa chamando [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (para inicializar a estrutura dinamicamente) ou atribuindo a constante **init \_ uma vez \_ estática \_ init** à variável de estrutura (para inicializar a estrutura estaticamente). Inicialmente, os dados armazenados na estrutura de inicialização única são nulos e seu estado não é inicializado.

Estruturas de inicialização única não podem ser compartilhadas entre processos.

O thread que executa a inicialização pode, opcionalmente, definir um contexto que está disponível para o chamador após a conclusão da inicialização. O contexto pode ser um objeto de sincronização ou pode ser um valor ou estrutura de dados. Se o contexto for um valor, sua inicialização de ordem **inferior \_ uma vez que os \_ \_ \_ bits reservados CTX** devem ser zero. Se o contexto for uma estrutura de dados, a estrutura de dados deverá ser alinhada em **DWORD**. O contexto é retornado para o chamador no parâmetro de saída *lpContext* da função [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) ou [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) .

A inicialização única pode ser executada de forma síncrona ou assíncrona. Uma função de retorno de chamada opcional pode ser usada para inicialização única síncrona.

## <a name="synchronous-one-time-initialization"></a>Inicialização única síncrona

As etapas a seguir descrevem a inicialização única síncrona que não usa uma função de retorno de chamada.

1.  O primeiro thread para chamar a função [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) faz com que a inicialização única seja iniciada. Para inicialização única síncrona, **InitOnceBeginInitialize** deve ser chamado sem o sinalizador **assíncrono Init \_ Once \_** .
2.  Os threads subsequentes que tentam a inicialização são bloqueados até que o primeiro thread conclua a inicialização ou falhe. Se o primeiro thread falhar, o próximo thread terá permissão para tentar a inicialização e assim por diante.
3.  Quando a inicialização é concluída, o thread chama a função [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . Opcionalmente, o thread pode criar um objeto de sincronização (ou outros dados de contexto) e especificá-lo no parâmetro *lpContext* da função **InitOnceComplete** .
4.  Se a inicialização for realizada com sucesso, o estado da estrutura de inicialização única será alterado para inicializado e o identificador *lpContext* (se houver) será armazenado na estrutura de inicialização. As tentativas de inicialização subsequentes retornam esses dados de contexto. Se a inicialização falhar, os dados serão **nulos**.

As etapas a seguir descrevem a inicialização única síncrona que usa uma função de retorno de chamada.

1.  O primeiro thread a chamar com êxito a função [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) passa um ponteiro para uma função de retorno de chamada [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) definida pelo aplicativo e quaisquer dados exigidos pela função de retorno de chamada. Se a chamada for realizada com sucesso, a função de retorno de chamada *InitOnceCallback* será executada.
2.  Os threads subsequentes que tentam a inicialização são bloqueados até que o primeiro thread conclua a inicialização ou falhe. Se o primeiro thread falhar, o próximo thread terá permissão para tentar a inicialização e assim por diante.
3.  Quando a inicialização é concluída, a função de retorno de chamada retorna. A função de retorno de chamada pode, opcionalmente, criar um objeto de sincronização (ou outros dados de contexto) e especificá-lo em seu parâmetro de saída de *contexto* .
4.  Se a inicialização for realizada com sucesso, o estado da estrutura de inicialização única será alterado para inicializado e o identificador de *contexto* (se houver) será armazenado na estrutura de inicialização. As tentativas de inicialização subsequentes retornam esses dados de contexto. Se a inicialização falhar, os dados serão **nulos**.

## <a name="asynchronous-one-time-initialization"></a>Inicialização única assíncrona

As etapas a seguir descrevem a inicialização única assíncrona.

1.  Se vários threads tentarem iniciar a inicialização simultaneamente chamando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) com **init \_ após \_ Async**, a função terá sucesso para todos os threads com o parâmetro *fPending* definido como **true**. Apenas um thread terá sucesso na inicialização; outras tentativas simultâneas não alteram o estado de inicialização.
2.  Quando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) retorna, o parâmetro *fPending* indica o status de inicialização:
    -   Se *fPending* for **false**, um thread terá êxito na inicialização. Outros threads devem limpar todos os dados de contexto que criaram e usar os dados de contexto no parâmetro de saída *lpContext* de [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Se *fPending* for **true**, a inicialização ainda não foi concluída e outros threads devem continuar.
3.  Cada thread chama a função [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . Opcionalmente, o thread pode criar um objeto de sincronização (ou outros dados de contexto) e especificá-lo no parâmetro *lpContext* de **InitOnceComplete**.
4.  Quando [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) retorna, seu valor de retorno indica se o thread de chamada foi bem-sucedido na inicialização.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) tiver êxito, o thread de chamada terá êxito na inicialização. O estado da estrutura de inicialização única é alterado para inicializado e o identificador *lpContext* (se houver) é armazenado na estrutura de inicialização.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) falhar, outro thread terá êxito na inicialização. O thread de chamada deve limpar todos os dados de contexto que foram criados e chamar [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) com **init \_ \_ \_ somente uma vez** para recuperar os dados de contexto armazenados na estrutura de inicialização única.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Chamando One-Time inicialização de vários sites

A inicialização única protegida por um único **init \_ Once** pode ser executada a partir de sites vários; um retorno de chamada diferente pode ser passado de cada site, e a sincronização com e sem o retorno de chamada pode ser mista. A inicialização ainda é guaranted para executar sucesfully apenas uma vez.

No entanto, a inicialização assíncrona e síncrona não pode ser mista: após a tentativa de inicialização assíncrona, as tentativas de iniciar a inicialização síncrona falharão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a inicialização do One-Time](using-one-time-initialization.md)
</dt> </dl>

 

 
