---
description: Os componentes geralmente são projetados para executar tarefas de inicialização quando são chamados pela primeira vez, em vez de quando são carregados.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: One-Time inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e513c18be3fcce85c8d2cde16bbe11edcf6a1597bb06c37279ecaa8add6598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073076"
---
# <a name="one-time-initialization"></a>One-Time inicialização

Os componentes geralmente são projetados para executar tarefas de inicialização quando são chamados pela primeira vez, em vez de quando são carregados. As funções de inicialização única garantem que essa inicialização ocorra apenas uma vez, mesmo quando vários threads podem tentar a inicialização.

**Windows Server 2003 e Windows XP:** Os aplicativos devem fornecer sua própria sincronização para inicialização única usando as [funções interlocked](interlocked-variable-access.md) ou outro mecanismo de sincronização. As funções de inicialização única estão disponíveis a partir do Windows Vista e Windows Server 2008.

As funções de inicialização avissas fornecem vantagens significativas para garantir que apenas um thread execute a inicialização:

-   Eles são otimizados para velocidade.
-   Eles criam as barreiras apropriadas nas arquiteturas do processador que as exigem.
-   Eles suportam inicialização bloqueada e paralela.
-   Eles evitam o bloqueio interno para que o código possa operar de forma assíncrona ou síncrona.

O sistema gerencia o processo de inicialização por meio de uma estrutura **INIT \_ ONCE** opaca que contém dados e informações de estado. O chamador aloca essa estrutura e a inicializa chamando [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (para inicializar a estrutura dinamicamente) ou atribuindo a constante **INIT \_ ONCE STATIC \_ \_ INIT** à variável de estrutura (para inicializar estaticamente a estrutura). Inicialmente, os dados armazenados na estrutura de inicialização única são NULL e seu estado não é inicializado.

Estruturas de inicialização única não podem ser compartilhadas entre processos.

O thread que executa a inicialização pode, opcionalmente, definir um contexto que está disponível para o chamador após a conclusão da inicialização. O contexto pode ser um objeto de sincronização ou pode ser um valor ou estrutura de dados. Se o contexto for um valor, seu **INIT \_ ONCE \_ CTX \_ RESERVED \_ BITS** de ordem baixa deverá ser zero. Se o contexto for uma estrutura de dados, a estrutura de dados deverá ser alinhada a **DWORD.** O contexto é retornado ao chamador no parâmetro de saída *lpContext* da função [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) ou [**InitOnceExecuteOnce.**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce)

A inicialização única pode ser executada de forma síncrona ou assíncrona. Uma função de retorno de chamada opcional pode ser usada para inicialização síncrona única.

## <a name="synchronous-one-time-initialization"></a>Inicialização síncrona única

As etapas a seguir descrevem a inicialização única síncrona que não usa uma função de retorno de chamada.

1.  O primeiro thread a chamar a [**função InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) faz com que a inicialização única seja iniciada com êxito. Para inicialização síncrona única, **InitOnceBeginInitialize** deve ser chamado sem o sinalizador **\_ \_ ASYNC INIT ONCE.**
2.  Threads subsequentes que tentam inicialização são bloqueados até que o primeiro thread conclua a inicialização ou falhe. Se o primeiro thread falhar, o próximo thread poderá tentar a inicialização e assim por diante.
3.  Quando a inicialização for concluída, o thread chamará a [**função InitOnceComplete.**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) Opcionalmente, o thread pode criar um objeto de sincronização (ou outros dados de contexto) e especificá-lo no parâmetro *lpContext* da **função InitOnceComplete.**
4.  Se a inicialização for bem-sucedida, o estado da estrutura de inicialização única será alterado para inicializado e o handle *lpContext* (se algum) for armazenado na estrutura de inicialização. As tentativas de inicialização subsequentes retornam esses dados de contexto. Se a inicialização falhar, os dados serão **NULL.**

As etapas a seguir descrevem a inicialização única síncrona que usa uma função de retorno de chamada.

1.  O primeiro thread para chamar com êxito a função [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) passa um ponteiro para uma função de retorno de chamada [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) definida pelo aplicativo e todos os dados exigidos pela função de retorno de chamada. Se a chamada for bem-sucedida, a função de retorno de chamada *InitOnceCallback* será executada.
2.  Threads subsequentes que tentam inicialização são bloqueados até que o primeiro thread conclua a inicialização ou falhe. Se o primeiro thread falhar, o próximo thread poderá tentar a inicialização e assim por diante.
3.  Quando a inicialização for concluída, a função de retorno de chamada retornará. A função de retorno de chamada pode, opcionalmente, criar um objeto de sincronização (ou outros dados de contexto) e especificá-lo em seu *parâmetro de* saída context.
4.  Se a inicialização for bem-sucedida, o estado da estrutura de  inicialização única será alterado para inicializado e o alça de contexto (se algum) for armazenado na estrutura de inicialização. As tentativas de inicialização subsequentes retornam esses dados de contexto. Se a inicialização falhar, os dados serão **NULL.**

## <a name="asynchronous-one-time-initialization"></a>Inicialização assíncrona única

As etapas a seguir descrevem a inicialização assíncrona única.

1.  Se vários threads tentarem iniciar simultaneamente a inicialização chamando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) com **INIT \_ ONCE \_ ASYNC**, a função terá êxito para todos os threads com o parâmetro *fPending* definido como **TRUE.** Somente um thread terá êxito na inicialização; outras tentativas simultâneas não alteram o estado de inicialização.
2.  Quando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) retorna, o *parâmetro fPending* indica o status de inicialização:
    -   Se *fPending* for **FALSE,** um thread terá sido bem-sucedido na inicialização. Outros threads devem limpar todos os dados de contexto que eles criaram e usar os dados de contexto no parâmetro de saída *lpContext* [**de InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Se *fPending* for **TRUE,** a inicialização ainda não foi concluída e outros threads devem continuar.
3.  Cada thread chama a [**função InitOnceComplete.**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) Opcionalmente, o thread pode criar um objeto de sincronização (ou outros dados de contexto) e especificá-lo no parâmetro *lpContext* **de InitOnceComplete.**
4.  Quando [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) retorna, seu valor de retorno indica se o thread de chamada foi bem-sucedido na inicialização.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) for bem-sucedido, o thread de chamada terá êxito na inicialização. O estado da estrutura de inicialização única é alterado para inicializado e o alça *lpContext* (se algum) é armazenado na estrutura de inicialização.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) falhar, outro thread terá êxito na inicialização. O thread de chamada deve limpar todos os dados de contexto criados e chamar [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) com **INIT \_ ONCE CHECK \_ \_ APENAS** para recuperar todos os dados de contexto armazenados na estrutura de inicialização única.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Chamando One-Time inicialização de vários sites

A inicialização única, protegido por uma única estrutura **INIT \_ ONCE,** pode ser executada de sites mutiple; um retorno de chamada diferente pode ser passado de cada site e a sincronização com e sem retorno de chamada pode ser misturada. A inicialização ainda é uma boa ideia para executar com sucesso apenas uma vez.

No entanto, a inicialização assíncrona e síncrona não pode ser misturada: depois que a inicialização assíncrona é tentada, as tentativas de iniciar a inicialização síncrona falhariam.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando One-Time inicialização](using-one-time-initialization.md)
</dt> </dl>

 

 
