---
title: Trabalhando com unidades de dados de protocolo
description: O SNMP (Simple Network Management Protocol) envia solicitações de operação e respostas como mensagens SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Trabalhando com unidades de dados de protocolo SNMP
- Unidades de dados de protocolo SNMP, trabalhando com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005837"
---
# <a name="working-with-protocol-data-units"></a>Trabalhando com unidades de dados de protocolo

O SNMP (Simple Network Management Protocol) envia solicitações de operação e respostas como mensagens SNMP. Uma mensagem SNMP é uma PDU (unidade de dados de protocolo SNMP) e elementos de cabeçalho de mensagem adicionais definidos pela RFC relevante. Uma PDU inclui uma lista de associações de variáveis.

A estrutura de uma PDU é restrita à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar uma PDU com um identificador do tipo **HSNMP \_ PDU**. O aplicativo WinSNMP deve criar um PDU antes de chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .

O aplicativo pode extrair e atualizar os elementos de dados de uma PDU e liberar recursos alocados para PDUs. Para executar essas operações, o aplicativo usa as [funções de PDU](winsnmp-functions.md)de WinSNMP. A tabela a seguir lista os tópicos que abordam o trabalho com PDUs no ambiente de programação WinSNMP.



| Tópico                                                                        | Descrição                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Criando uma PDU](creating-a-pdu.md)                                         | Descreve como criar uma PDU.                                     |
| [Atualizando uma PDU](updating-a-pdu.md)                                         | Descreve como recuperar e atualizar campos de PDU.                   |
| [Duplicando uma PDU](duplicating-a-pdu.md)                                   | Descreve como duplicar uma PDU.                                  |
| [Validando uma PDU](validating-a-pdu.md)                                     | Descreve a validação de uma PDU.                                 |
| [Resposta correspondente e PDUs de solicitação](matching-response-and-request-pdus.md) | Descreve o processo de correspondência de uma PDU de resposta para uma PDU de solicitação. |



 

Para obter mais informações, consulte [trabalhando com as listas de associação de variáveis](working-with-variable-binding-lists.md) e objetos de identificador de [recurso](resource-handle-objects.md).

 

 




