---
title: Códigos de erro de WinSNMP comuns
description: A função SnmpGetLastError pode retornar um código de erro geral após uma falha de uma função WinSNMP. A tabela a seguir lista os códigos de erro WinSNMP comuns.
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beee49aef651784b0b8dc05c0114b7bf906be113
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007882"
---
# <a name="winsnmp-common-error-codes"></a>Códigos de erro de WinSNMP comuns

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

A função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) pode retornar um código de erro geral após uma falha de uma função WinSNMP. A tabela a seguir lista os códigos de erro WinSNMP comuns.



| Código do erro                | Significado                                                                                                                                                                                                        | Ação recomendada                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ não \_ inicializado | A função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) não foi concluída com êxito porque a execução do programa foi iniciada ou porque uma chamada para a função [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) foi concluída com êxito. | O aplicativo deve chamar [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) antes de chamar qualquer outra função de API WinSNMP quando [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) falhar. A função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) retorna informações de erro estendidas sobre a falha de [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup).                                                          |
| \_erro de alocação de snmpapi \_     | O aplicativo especificou um ponteiro inválido ou ocorreu um erro durante a alocação de memória. A implementação do Microsoft WinSNMP não pôde obter recursos suficientes para executar a solicitação.                | O aplicativo deve fornecer ponteiros de memória válidos para todos os parâmetros de saída. Ele deve liberar recursos, reduzir os requisitos de recursos ou facilitar um desligamento normal. Um desligamento normal inclui várias chamadas para a função [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , uma para cada sessão de WinSNMP aberta. Ele também inclui uma chamada para a função [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . |
| \_NOOP snmpapi             | A função não foi concluída com êxito porque todos os parâmetros de saída são **nulos**.                                                                                                                         | O aplicativo deve especificar pelo menos um parâmetro de saída que não seja **nulo** ao chamar uma função que retorna informações para o aplicativo.                                                                                                                                                                                                                                  |
| SNMPAPI \_ outro \_ erro     | Ocorreu um erro desconhecido ou indefinido.                                                                                                                                                                        | O aplicativo geralmente deve responder com um desligamento normal. Um desligamento normal inclui várias chamadas para a função [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , uma para cada sessão de WinSNMP aberta. Ele também inclui uma chamada para a função [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) .                                                                                                           |



 

Os erros de WinSNMP que transmitem informações específicas de contexto são indicados na página de referência de cada função.

 

 