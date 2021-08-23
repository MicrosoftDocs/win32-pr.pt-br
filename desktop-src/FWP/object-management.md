---
title: Gerenciamento de objetos
description: Esta seção aborda o uso correto de tipos de objeto de API do WFP (Windows Filtering Platform).
ms.assetid: 2625ef9a-0e62-4e21-ba93-047965d0d782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5cb51d4e78049d7911a4a5ed265091e05bc1cbb00ce470e332d59dd23c6026d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068846"
---
# <a name="object-management"></a>Gerenciamento de objetos

Esta seção aborda o uso correto de tipos de objeto de API do WFP (Windows Filtering Platform).

## <a name="sessions"></a>Sessões

A API do WFP é orientada a sessão e a maioria das chamadas de função é feita dentro do contexto de uma sessão. Uma nova sessão de cliente é criada chamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). A sessão termina quando o cliente chama [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0) ou o processo do cliente é encerrado. Quando uma sessão é destruída, seja de propósito ou pelo rundown de RPC, o BFE (Mecanismo de Filtragem Base) primeiro anula qualquer transação existente.

Ao criar uma nova sessão, o chamador pode criar uma sessão dinâmica passando o sinalizador DINÂMICO [**FWPM \_ SESSION \_ FLAG \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) para [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0). Todos os objetos adicionados durante uma sessão dinâmica são excluídos automaticamente quando a sessão termina.

## <a name="transactions"></a>Transactions

A API do WFP é transacional e a maioria das chamadas de função é feita dentro do contexto de uma transação. Os chamadores podem usar [**FwpmTransactionBegin0,**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) [**FwpmTransactionCommit0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactioncommit0)e [**FwpmTransactionAbort0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionabort0) para controlar explicitamente as transações. No entanto, se uma chamada de função for feita fora de uma transação explícita, ela será executada dentro de uma transação implícita. Se uma transação estiver em andamento, quando uma sessão for encerrada, ela será anulada automaticamente. Transações implícitas nunca são anuladas à força.

As transações são somente leitura ou leitura/gravação e impõem uma rigorosa semântica[ACID](../cossdk/acid-properties.md)(Atomic Consistent Isolated Durable).

Cada sessão de cliente pode ter apenas uma transação em andamento por vez. Se o chamador tentar iniciar uma segunda transação antes de comprometer ou anular a primeira, o BFE retornará um erro.

Se uma operação falhar durante o curso de uma transação, ela não afetará o estado geral da transação. Por exemplo, suponha que o cliente inicie uma transação e chame [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0) três vezes antes de uma quarta chamada falhar. O cliente agora tem a opção de:

-   Anulando a transação, caso em que nenhum dos filtros será adicionado.
-   Confirmação da transação; nesse caso, os três primeiros filtros serão adicionados.
-   Continuando com mais operações, incluindo potencialmente repetir o [**FwpmFilterAdd0 com falha.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

Ao iniciar uma transação, o BFE aguardará até que [**o txnWaitTimeoutInMSec**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_session0) da sessão expire para adquirir o bloqueio. Se o bloqueio não for adquirido dentro desse tempo, a aquisição de bloqueio (e a [**chamada FwpmTransactionBegin0)**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) falhará. Isso impede que os clientes não respondam indefinidamente. Se o cliente não especificou um tempo de bloqueio, ele assume como padrão 15 segundos.

Cada transação também tem um tempo de bloqueio. Essa é a quantidade máxima de tempo que ele pode ter o bloqueio. Se o proprietário não liberar o bloqueio dentro desse tempo, a transação será anulada à força, fazendo com que o bloqueio seja liberado. O tempo de bloqueio não é configurável. Ele é infinito para chamadores de modo kernel e uma hora para chamadores de modo de usuário. Se uma transação for anulada à força, a próxima chamada feita dentro dessa transação falhará com **FWP \_ E \_ TXN \_ ABORTED.**

## <a name="object-lifetimes"></a>Tempo de vida do objeto

Os objetos podem ter um dos quatro possíveis tempo de vida:

-   Dinâmico — um objeto será dinâmico somente se for adicionado usando um identificador de sessão dinâmico. Objetos dinâmicos ficam ativos até que sejam excluídos ou a sessão de propriedade seja encerrada.
-   Estático — os objetos são estáticos por padrão. Objetos estáticos ficam ativos até que sejam excluídos, parados BFE ou o sistema seja desligado.
-   Persistente — os objetos persistentes são criados passando o sinalizador PERSISTENT do **sinalizador FWPM \_ \* \_ \_** apropriado para uma **função \* Add0 do Fwpm.** Objetos persistentes ficam ativos até que sejam excluídos.
-   Integrado – objetos integrados são predefinidos pelo BFE e não podem ser adicionados ou excluídos. Eles ficam para sempre.

Filtros em camadas de modo kernel podem ser marcados como filtros de tempo de inicialização passando o sinalizador apropriado para [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0). Os filtros de tempo de inicialização são adicionados ao sistema quando o driver TCP/IP é iniciado e removidos quando o BFE termina a inicialização. Objetos persistentes são adicionados quando o BFE é iniciado.

Em muitos casos, um provedor de política pode não querer que sua política persistente seja imposta se o provedor tiver sido desabilitado. Ao adicionar um provedor, o chamador pode especificar um nome Windows serviço opcional. Ao adicionar objetos persistentes, o chamador pode, opcionalmente, especificar o provedor que "possui" esse objeto. No início do serviço, o BFE só adiciona objetos persistentes ao sistema se eles não estão associados a um provedor ou o provedor associado não tem nenhum nome de serviço Windows ou o serviço Windows associado é definido como o início automático.

## <a name="object-associations"></a>Associações de objeto

Alguns objetos têm referências a outros objetos. Por exemplo, um filtro sempre faz referência a uma camada e pode referenciar um texto explicado e um contexto de provedor. Objetos não podem se referir a objetos que podem ter um tempo de vida mais curto. Portanto, um objeto dinâmico não pode se referir a um objeto dinâmico de uma sessão diferente. Um objeto estático não pode se referir a um objeto dinâmico. Um objeto persistente não pode se referir a um objeto dinâmico, um objeto estático ou um objeto persistente pertencente a um provedor diferente.

Um objeto não pode ser excluído até que todos os objetos que o referenciam tenham sido excluídos pela primeira vez.

## <a name="luids-and-guids"></a>LUIDs e GUIDs

Todos os objetos de API WFP no modo de usuário (FWPM) são identificados por um **GUID**(identificador global exclusivo) e referenciam outros objetos por **seus GUIDs.** O **GUID** só precisa ser exclusivo dentro do tipo de objeto. Por exemplo, um filtro e um contexto de provedor podem ter o mesmo **GUID,** mas dois filtros não podem. Ao adicionar um novo objeto, os chamadores podem atribuir o **GUID** do objeto ou deixá-lo inicializado em zero e permitir que o BFE atribua o **GUID**.

Todos os objetos de API WFP do modo kernel (FWPS) são identificados por um **LUID**(identificador exclusivo local) e referenciam outros objetos por seu LUID. A opção de **GUID** para **LUID** permite que o WFP conservar o pool não pagedo e otimizar o processamento em tempo de run-time. A largura do **LUID depende** do tipo de objeto e dos intervalos de um **UINT16** a um **UINT64.** **LUIDs** são sempre atribuídos por BFE.

 

 