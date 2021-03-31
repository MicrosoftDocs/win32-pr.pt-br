---
title: Trabalhando com listas de associação de variáveis
description: Uma associação de variável é o emparelhamento de um nome de instância de objeto SNMP com um valor associado. Uma lista de associação de variáveis é uma série de entradas de associação de variáveis. No WinSNMP, uma PDU (unidade de dados de protocolo) inclui uma lista de associações de variáveis.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Trabalhando com listas de associação de variáveis SNMP
- Associação de variáveis lista SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640187"
---
# <a name="working-with-variable-binding-lists"></a>Trabalhando com listas de associação de variáveis

Uma *Associação de variável* é o emparelhamento de um nome de instância de objeto SNMP com um valor associado. Uma *lista de associação de variáveis* é uma série de entradas de associação de variáveis. No WinSNMP, uma PDU (unidade de dados de protocolo) inclui uma lista de associações de variáveis.

Os detalhes da estrutura da lista de associação de variáveis são restritos à implementação do Microsoft WinSNMP. Um aplicativo WinSNMP pode acessar uma lista de associação de variáveis com um identificador do tipo **HSNMP \_ VBL**. Para obter mais informações, consulte [objetos de identificador de recursos](resource-handle-objects.md).

O aplicativo WinSNMP pode construir e manipular listas de associação de variáveis e incluí-las em PDUs. Para executar essas operações, o aplicativo usa as [funções de associação de variável](winsnmp-functions.md)WinSNMP. Para obter mais informações sobre como trabalhar com as listas de associação de variáveis e WinSNMP, consulte os tópicos listados na tabela a seguir.



| Tópico                                                                    | Descrição                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [Criando uma lista de associações de variáveis](creating-a-variable-binding-list.md) | Descreve como criar uma lista de associações de variáveis. |
| [Gerenciando uma lista de associação de variáveis](managing-a-variable-binding-list.md) | Descreve como gerenciar uma lista de associações de variáveis. |



 

Para obter mais informações sobre associações de variáveis e listas de associação de variáveis, consulte [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), "operações de protocolo para a versão 2 do protocolo de gerenciamento de rede simples (SNMPv2)" e as [funções de associação de variável](winsnmp-functions.md)WinSNMP.

 

 




