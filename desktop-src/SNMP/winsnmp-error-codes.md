---
title: Códigos de erro WinSNMP
description: Códigos de erro WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Códigos de erro WinSNMP SNMP
- Códigos de erro SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2a9f9dda792008a0e69e6c23e692b4aa4c4e78316eeca015f7b056e2a275df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142859"
---
# <a name="winsnmp-error-codes"></a>Códigos de erro WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. em vez disso, use [Gerenciamento Remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

> [!Note]  
> Os erros descritos neste tópico são distintos dos códigos de erro SNMP definidos pelos RFCs relevantes.

 

Todas as funções WinSNMP retornarão o valor **snmpapi \_ falha** se a função falhar. O aplicativo WinSNMP deve chamar imediatamente a função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) para recuperar informações de erro estendidas quando uma função WinSNMP falhar. A tabela a seguir lista os tópicos que discutem os códigos de erro estendidos retornados pelas funções de WinSNMP.



| Tópico                                                        | Descrição                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Códigos de erro de WinSNMP comuns](winsnmp-common-error-codes.md) | Descreve os códigos de erro comuns para a API WinSNMP.       |
| [Erros de transporte de rede](network-transport-errors.md)     | Descreve os erros de transporte de rede para a API WinSNMP. |



 

Os erros de WinSNMP que transmitem informações específicas do contexto são incluídos na página de referência da função.

 

 