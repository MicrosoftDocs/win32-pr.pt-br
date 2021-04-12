---
title: Gerenciamento de objetos
description: Esta seção aborda o uso correto dos tipos de objeto da API da Windows Filtering Platform (WFP).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc41560bb85a7e79c0262d77c0b34fe6c1d9bfd6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454012"
---
# <a name="object-management"></a>Gerenciamento de objetos

Esta seção aborda o uso correto dos tipos de objeto da API da Windows Filtering Platform (WFP).

## <a name="sessions"></a>Sessões

A API WFP é orientada a sessão e a maioria das chamadas de função são feitas dentro do contexto de uma sessão. Uma nova sessão de cliente é criada chamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). A sessão termina quando o cliente chama [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) ou o processo do cliente é encerrado. Quando uma sessão é destruída, seja por finalidade ou pelo encerramento de RPC, o mecanismo de filtragem base (BFE) primeiro anula qualquer transação existente.

Ao criar uma nova sessão, o chamador pode criar uma sessão dinâmica passando o sinalizador [**\_ \_ \_ dinâmico sinalizador de sessão FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) para [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Todos os objetos adicionados durante uma sessão dinâmica são excluídos automaticamente quando a sessão termina.

## <a name="transactions"></a>Transactions

A API WFP é transacional e a maioria das chamadas de função são feitas dentro do contexto de uma transação. Os chamadores podem usar [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0), [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)e [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) para controlar explicitamente as transações. No entanto, se uma chamada de função for feita fora de uma transação explícita, ela será executada dentro de uma transação implícita. Se uma transação estiver em andamento, quando uma sessão for encerrada, ela será anulada automaticamente. As transações implícitas nunca são anuladas forçosamente.

As transações são somente leitura ou leitura/gravação e aplicam semântica[Acid](../cossdk/acid-properties.md)(durável) consistente de atomicidade.

Cada sessão de cliente pode ter apenas uma transação em andamento por vez. Se o chamador tentar iniciar uma segunda transação antes de confirmar ou anular a primeira, o BFE retornará um erro.

Se uma operação falhar durante o curso de uma transação, ela não afetará o estado geral da transação. Por exemplo, suponha que o cliente inicie uma transação e chame com êxito [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) três vezes antes de uma quarta chamada falhar. Agora, o cliente tem a opção de:

-   Anulando a transação; nesse caso, nenhum dos filtros será adicionado.
-   Confirmando a transação, caso em que os três primeiros filtros serão adicionados.
-   Continuando com mais operações, incluindo possivelmente repetir o [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)com falha.

Ao iniciar uma transação, o BFE aguardará até que a [**txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) da sessão expire para adquirir o bloqueio. Se o bloqueio não for adquirido dentro desse tempo, a aquisição de bloqueio (e a chamada [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) ) falhará. Isso impede que os clientes não respondam indefinidamente. Se o cliente não tiver especificado um tempo limite de bloqueio, o padrão será 15 segundos.

Cada transação também tem um tempo limite de bloqueio. Essa é a quantidade máxima de tempo que pode ser proprietária do bloqueio. Se o proprietário não liberar o bloqueio dentro desse tempo, a transação será anulada à força, fazendo com que o bloqueio seja liberado. O tempo limite de bloqueio não é configurável. Ele é infinito para chamadores de modo kernel e uma hora para chamadores de modo de usuário. Se uma transação for forçosamente anulada, a próxima chamada feita dentro dessa transação falhará com **fwp \_ E \_ TXN \_ abortado**.

## <a name="object-lifetimes"></a>Tempos de vida do objeto

Os objetos podem ter um dos quatro tempos de vida possíveis:

-   Dinâmico — um objeto será dinâmico somente se for adicionado usando um identificador de sessão dinâmica. Objetos dinâmicos até que sejam excluídos ou a sessão de propriedade seja encerrada.
-   Estático – os objetos são estáticos por padrão. Os objetos estáticos são ativados até serem excluídos, o BFE é interrompido ou o sistema é desligado.
-   Persistent – objetos persistentes são criados passando o sinalizador **\_ \* \_ \_ persistente de sinalizador FWPM** apropriado para uma função **\* Add0 FWPM** . Objetos persistentes em tempo real até que sejam excluídos.
-   Interno — os objetos internos são predefinidos por BFE e não podem ser adicionados ou excluídos. Eles vivem para sempre.

Filtros em camadas de modo kernel podem ser marcados como filtros de tempo de inicialização passando o sinalizador apropriado para [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). Os filtros de tempo de inicialização são adicionados ao sistema quando o driver TCP/IP é iniciado e removido quando o BFE conclui a inicialização. Os objetos persistentes são adicionados quando o BFE é iniciado.

Em muitos casos, um provedor de política pode não querer que sua política persistente seja imposta se o provedor tiver sido desabilitado. Ao adicionar um provedor, o chamador pode especificar um nome de serviço Windows opcional. Ao adicionar objetos persistentes, o chamador pode opcionalmente especificar o provedor que "possui" esse objeto. No início do serviço, o BFE adiciona somente objetos persistentes ao sistema se eles não estiverem associados a um provedor ou se o provedor associado não tiver nenhum nome de serviço do Windows ou se o serviço do Windows associado estiver definido como início automático.

## <a name="object-associations"></a>Associações de objeto

Alguns objetos têm referências a outros objetos. Por exemplo, um filtro sempre faz referência a uma camada e pode fazer referência a um texto explicativo e a um contexto de provedor. Os objetos não podem se referir a objetos que podem ter um tempo de vida menor. Portanto, um objeto dinâmico não pode se referir a um objeto dinâmico de uma sessão diferente. Um objeto estático não pode se referir a um objeto dinâmico. Um objeto persistente não pode se referir a um objeto dinâmico, um objeto estático ou um objeto persistente de propriedade de um provedor diferente.

Um objeto não pode ser excluído até que todos os objetos que fazem referência a ele tenham sido excluídos primeiro.

## <a name="luids-and-guids"></a>LUIDs e GUIDs

Todos os FWPM (objetos de API WFP) de modo de usuário são identificados por um **GUID**(identificador global exclusivo) e fazem referência a outros objetos por seus s **GUID**. O **GUID** só precisa ser exclusivo dentro do tipo de objeto. Por exemplo, um filtro e um contexto de provedor podem ter o mesmo **GUID**, mas dois filtros não podem. Ao adicionar um novo objeto, os chamadores podem atribuir o **GUID** do objeto ou deixá-los inicializados com zero e deixar o BFE atribuir o **GUID**.

Todos os FWPS (objetos de API WFP) de modo kernel são identificados por um **LUID**(identificador local exclusivo) e fazem referência a outros objetos por sua LUID. A mudança de **GUID** para **LUID** permite que a WFP preserve pool não paginável e otimize o processamento em tempo de execução. A largura da **LUID** depende do tipo de objeto e varia de um **UINT16** para um **UINT64**. Os s de **LUID** são sempre atribuídos por BFE.

 

 