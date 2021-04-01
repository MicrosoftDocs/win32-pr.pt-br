---
title: Valores de retorno da função WinSNMP
description: O valor de retorno de uma chamada de função WinSNMP pode ser um identificador para um recurso que a implementação do Microsoft WinSNMP aloca para o aplicativo WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008042"
---
# <a name="winsnmp-function-return-values"></a>Valores de retorno da função WinSNMP

\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]

O valor de retorno de uma chamada de função WinSNMP pode ser um identificador para um recurso que a implementação do Microsoft WinSNMP aloca para o aplicativo WinSNMP.

A tabela a seguir lista os cinco tipos de recursos que a implementação aloca.



| Tipo de identificador    | Descrição                       |
|----------------|-----------------------------------|
| \_sessão HSNMP | Tratar de uma sessão WinSNMP       |
| \_entidade HSNMP  | Identificador para uma entidade SNMP          |
| contexto de HSNMP \_ | Identificador para um contexto SNMP         |
| PDU de HSNMP \_     | Identificador para uma unidade de dados de protocolo    |
| HSNMP \_ VBL     | Identificador para uma lista de associação de variável |



 

Para obter mais informações, consulte [objetos de identificador de recursos](resource-handle-objects.md).

O valor de retorno também pode ser um valor inteiro longo sem sinal do tipo **smiUINT32** que representa um valor de \_ status de snmpapi.

A tabela a seguir lista os valores de status de WinSNMP e seu significado.



| Status           | Descrição                                                                      |
|------------------|----------------------------------------------------------------------------------|
| falha de SNMPAPI \_ | Indica um erro. Equivale a 0 ou **NULL**.                                    |
| SNMPAPI \_ êxito | Indica que a função foi concluída com êxito. Equivale a 1 ou uma contagem positiva. |



 

 

 