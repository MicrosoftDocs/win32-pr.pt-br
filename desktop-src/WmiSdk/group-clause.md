---
description: A cláusula GROUP faz com que o WMI gere uma única notificação para representar um grupo de eventos.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Cláusula GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f5f796c563376853896213c5418039ac0104d04437ec7c9e0b444db6692e60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993176"
---
# <a name="group-clause"></a>Cláusula GROUP

A cláusula GROUP faz com que o WMI gere uma única notificação para representar um grupo de eventos. A notificação representativa é uma instância da [**\_ \_ classe de sistema AggregateEvent.**](--aggregateevent.md) A **\_ \_ classe de sistema AggregateEvent** contém duas propriedades: **Representative** e **NumberOfEvents.** A **propriedade Representative** é um objeto inserido que contém uma das instâncias recebidas durante o intervalo de agrupamento especificado na cláusula [WITHIN](within-clause.md). Por exemplo, se um evento de agregação for gerado para notificar os eventos de modificação da instância, **o Representante** conterá uma instância da [**\_ \_ classe InstanceModificationEvent.**](--instancemodificationevent.md) A **propriedade NumberOfEvents** contém o número de eventos recebidos durante o intervalo de agrupação. O intervalo de agrupamento especifica o período de tempo, depois de receber um evento inicial, durante o qual o WMI deve coletar eventos semelhantes.

A cláusula GROUP deve conter uma cláusula WITHIN para especificar o intervalo de agrupação e pode conter a palavra-chave BY ou HAVING ou ambos. A cláusula GROUP é colocada após a cláusula WHERE, conforme mostrado a seguir:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

O *valor EventClass* é a classe de evento da qual o evento é membro e *value* é o valor da propriedade na qual a notificação é necessária. O intervalo é um inteiro sem sinal que representa o intervalo de agrupação depois de receber o primeiro evento. O inteiro sem sinal é um número de segundos. A lista de propriedades é uma lista delimitada por vírgulas de uma ou mais propriedades incluídas na classe de evento; *operador* é qualquer operador relacional; e *integer* é um inteiro sem sinal de 32 bits que indica um número de eventos.

Ao usar a cláusula GROUP, as cláusulas WHERE, BY e HAVING são opcionais.

Um uso básico da cláusula GROUP pode solicitar um grupo de eventos dentro de um intervalo de tempo que começa quando o primeiro evento é recebido. Por exemplo, a consulta a seguir grupos todos os eventos de email enviados dentro de 5 minutos. Em vez de paciar um usuário sempre que uma parte do novo email for recebida, o consumidor permanente poderá usar essa consulta para informar o usuário somente se um novo email tiver sido recebido nos últimos 5 minutos.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Se informações mais detalhadas são necessárias, os eventos podem ser agrupados por uma ou mais propriedades da classe de evento. A consulta a seguir solicita que os eventos de email sejam combinados com outros eventos que têm o mesmo valor na **propriedade Remetente:**


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



Um nível ainda maior de detalhes pode ser obtido adicionando uma cláusula WHERE. Por exemplo, a consulta a seguir notifica um usuário de novo email de um remetente específico que chegou nos últimos 10 minutos, combinado com outros eventos que têm o mesmo valor na propriedade **Importance:**


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



