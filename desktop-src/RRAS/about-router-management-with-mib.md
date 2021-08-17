---
title: Sobre o gerenciamento de roteador com MIB
description: As APIs de MIB (base de informações de gerenciamento) para o gerenciamento de roteador possibilitam consultar e definir os valores das variáveis de MIB exportadas por um dos gerenciadores de roteadores ou qualquer um dos protocolos de roteamento que os gerenciadores de roteadores possuem.
ms.assetid: d0fafd82-e7cb-4524-a499-d14830f02b21
keywords:
- Roteamento, base de informações de gerenciamento
- Roteamento, base de informações de gerenciamento, descrito
- Base de informações de gerenciamento RRAS
- MIB
- MIB, consulte base de informações de gerenciamento
- Base de informações de gerenciamento RRAS
- Base de informações de gerenciamento RRAS, descrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a867d903e0fb79f9360dc5f1cb485040ed4489b328365bc2daa063a35fbe27d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792191"
---
# <a name="about-router-management-with-mib"></a>Sobre o gerenciamento de roteador com MIB

As APIs de MIB (base de informações de gerenciamento) para o gerenciamento de roteador possibilitam consultar e definir os valores das variáveis de MIB exportadas por um dos gerenciadores de roteadores ou qualquer um dos protocolos de roteamento que os gerenciadores de roteadores possuem. Usando essa API, o roteador dá suporte ao SNMP (Simple Network Management Protocol).

Na estrutura SNMP, cada um dos objetos gerenciáveis no roteador é representado por uma variável que tem um OID (identificador de objeto exclusivo). Correspondente a cada OID é um valor que representa o estado atual do objeto. A coleção de OIDs e valores é conhecida como MIB (base de informações de gerenciamento). As chamadas MprAdminMib permitem que um desenvolvedor especifique um objeto por seu OID e uma consulta ou gravação ("set") do valor do objeto.

Para consultar e definir variáveis MIB, o módulo que serviços de chamadas deve definir um conjunto de estruturas de dados. Essas estruturas de dados incluem estruturas para usar como identificadores de objeto e estruturas que contêm os valores das variáveis MIB que estão sendo acessadas. Essas estruturas de dados são opacas a todos, exceto o chamador da função MIB e o módulo que está atendendo à chamada.

O módulo que atende à chamada MIB é um Gerenciador de roteador ou um dos protocolos de roteamento. O chamador deve especificar um Gerenciador de roteador mesmo se a chamada for tratada por um dos protocolos de roteamento. Nesse caso, o chamador deve especificar o Gerenciador de roteador que corresponde à família de protocolos para esse protocolo de roteamento. Por exemplo, se o protocolo de roteamento OSPF (Open Shortest Path First) estivesse lidando com a chamada MIB, o chamador precisaria especificar o Gerenciador do roteador IP, pois o OSPF pertence à família de protocolos IP. Em cada uma das funções de MIB, o parâmetro *dwTransportId* especifica um Gerenciador de roteador e o parâmetro *RoutingPid* especifica o protocolo de roteamento. O Gerenciador de roteador também tem um *RoutingPid* exclusivo, já que algumas das variáveis MIB podem ser tratadas pelo próprio Gerenciador de roteador.

As funções MprAdminMib podem ser chamadas em um computador diferente daquele que está sendo administrado. As funções MprAdminMIB que consultam ou gravam valores, assumem como um parâmetro um identificador para o computador administrar. Use a função [**MprAdminMIBServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverconnect) para estabelecer a conexão com o computador remoto e obter esse identificador. Depois de chamar as funções MprAdminMIB necessárias para realizar uma tarefa administrativa específica, chame a função [**MprAdminMIBServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibserverdisconnect) para encerrar a conexão com o computador remoto.

As funções [**MprAdminMIBEntryCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrycreate) e [**MprAdminMIBEntrySet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryset) usam como parâmetros um OID e um buffer que contém o novo valor para o objeto.

As funções [**MprAdminMIBEntryGet**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentryget), [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) e [**MPRADMINMIBENTRYGETNEXT**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) usam como parâmetros um OID e o endereço de uma variável de ponteiro. Após o retorno bem-sucedido, a variável de ponteiro aponta para um buffer que contém o valor do objeto. O chamador deve liberar a memória para esse buffer chamando a função [**MprAdminMIBBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibbufferfree) .

As funções [**MprAdminMIBEntryGetFirst**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetfirst) e [**MprAdminMIBEntryGetNext**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminmibentrygetnext) permitem que um desenvolvedor execute uma *passagem SNMP*. Como os OIDs são ordenados, cada OID e, portanto, cada objeto gerenciável tem uma OID *seguinte* . Uma visão SNMP refere-se à passagem de uma parte da MIB lendo ou gravando uma sequência de OIDs.

Todas as chamadas de MprAdminMib passam pelo Gerenciador de interface dinâmica (DIM). Dependendo do OID, DIM passa a chamada para um dos gerenciadores do roteador. (IP e IPX dão suporte a SNMP). Novamente, dependendo do OID, o Gerenciador do roteador pode manipular a chamada em si ou passar a chamada para um de seus clientes. Todos os clientes de roteador são necessários para implementar e exportar as seguintes funções que correspondem às funções de MprAdminMIB chamadas de forma semelhante:

-   [**MibCreate**](/windows/desktop/api/Routprot/nc-routprot-pmib_create)
-   [**MibDelete**](/windows/desktop/api/Routprot/nc-routprot-pmib_delete)
-   [**MibSet**](/windows/desktop/api/Routprot/nc-routprot-pmib_set)
-   [**MibGet**](/windows/desktop/api/Routprot/nc-routprot-pmib_get)
-   [**MibGetFirst**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_first)
-   [**MibGetNext**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_next)
-   [**MibGetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_get_trap_info)
-   [**MibSetTrapInfo**](/windows/desktop/api/Routprot/nc-routprot-pmib_set_trap_info)

 

 




