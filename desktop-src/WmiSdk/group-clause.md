---
description: A cláusula GROUP faz com que o WMI gere uma única notificação para representar um grupo de eventos.
ms.assetid: 811e72f8-2e50-4696-ad58-50bb5e211afb
ms.tgt_platform: multiple
title: Cláusula GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032a8e86c84c0b317b3739c0e203a249b432b0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765193"
---
# <a name="group-clause"></a>Cláusula GROUP

A cláusula GROUP faz com que o WMI gere uma única notificação para representar um grupo de eventos. A notificação representativa é uma instância da classe de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) . A classe de sistema **\_ \_ AggregateEvent** contém duas propriedades: **Representation** e **NumberOfEvents**. A propriedade **Representation** é um objeto inserido que contém uma das instâncias recebidas durante o intervalo de Agrupamento especificado na [cláusula Within](within-clause.md). Por exemplo, se um evento de agregação for gerado para notificar sobre eventos de modificação de instância, **representará** uma instância da classe [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) . A propriedade **NumberOfEvents** contém o número de eventos recebidos durante o intervalo de agrupamento. O intervalo de agrupamento especifica o período de tempo, após o recebimento de um evento inicial, durante o qual o WMI deve coletar eventos semelhantes.

A cláusula GROUP deve conter uma cláusula WITHIN para especificar o intervalo de agrupamento e pode conter a palavra-chave BY ou HAVING, ou ambos. A cláusula GROUP é colocada após a cláusula WHERE, conforme mostrado a seguir:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
    GROUP WITHIN interval [BY property_list]
    [HAVING NumberOfEvents operator integer]
```

O valor *EventClass* é a classe de evento da qual o evento é um membro e *Value* é o valor para a propriedade na qual a notificação é necessária. O intervalo é um inteiro sem sinal que representa o intervalo de agrupamento após o recebimento do primeiro evento. O inteiro sem sinal é um número de segundos. A lista de propriedades é uma lista delimitada por vírgula de uma ou mais propriedades que são incluídas na classe de evento; o *operador* é qualquer operador relacional; e *Integer* é um inteiro de 32 bits sem sinal indicando um número de eventos.

Ao usar a cláusula GROUP, as cláusulas WHERE, BY e HAVING são opcionais.

Um uso básico da cláusula GROUP pode solicitar um agrupamento de eventos dentro de um intervalo de tempo que é iniciado quando o primeiro evento é recebido. Por exemplo, a consulta a seguir agrupa todos os eventos de email enviados em 5 minutos. Em vez de paginar um usuário sempre que um novo email for recebido, o consumidor permanente poderá usar essa consulta para informar o usuário somente se um novo email tiver sido recebido nos últimos 5 minutos.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300
```



Se forem necessárias informações mais detalhadas, os eventos poderão ser agrupados por uma ou mais propriedades da classe de evento. A consulta a seguir solicita que os eventos de email sejam combinados com outros eventos que têm o mesmo valor na propriedade **Sender** :


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 BY Sender
```



Um nível ainda maior de detalhes pode ser obtido com a adição de uma cláusula WHERE. Por exemplo, a consulta a seguir notifica um usuário sobre o novo email de um remetente específico que chegou nos últimos 10 minutos, combinado com outros eventos que têm o mesmo valor na propriedade de **importância** :


```sql
SELECT * FROM EventClass WHERE Sender = "MyBoss" 
  GROUP WITHIN 300 BY Importance
```



 

 



