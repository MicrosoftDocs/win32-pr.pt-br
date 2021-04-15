---
title: Códigos de erro WinSNMP
description: Códigos de erro WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Códigos de erro WinSNMP SNMP
- Códigos de erro SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454277"
---
# <a name="winsnmp-error-codes"></a>Códigos de erro WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

> [!Note]  
> Os erros descritos neste tópico são distintos dos códigos de erro SNMP definidos pelos RFCs relevantes.

 

Todas as funções WinSNMP retornarão o valor **snmpapi \_ falha** se a função falhar. O aplicativo WinSNMP deve chamar imediatamente a função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) para recuperar informações de erro estendidas quando uma função WinSNMP falhar. A tabela a seguir lista os tópicos que discutem os códigos de erro estendidos retornados pelas funções de WinSNMP.



| Tópico                                                        | Descrição                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Códigos de erro de WinSNMP comuns](winsnmp-common-error-codes.md) | Descreve os códigos de erro comuns para a API WinSNMP.       |
| [Erros de transporte de rede](network-transport-errors.md)     | Descreve os erros de transporte de rede para a API WinSNMP. |



 

Os erros de WinSNMP que transmitem informações específicas do contexto são incluídos na página de referência da função.

 

 