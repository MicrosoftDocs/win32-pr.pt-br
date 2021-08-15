---
description: A cláusula HAVING é usada para filtrar os eventos que são recebidos durante o intervalo de Agrupamento especificado na cláusula WITHIN.
ms.assetid: 787e31df-df6a-4fb0-a1c0-18bd60867e2f
ms.tgt_platform: multiple
title: Cláusula HAVING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2662ea337c5664130eb9973c049431daedefe3c947c45eb397a950522fea6bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993156"
---
# <a name="having-clause"></a>Cláusula HAVING

A cláusula HAVING é usada para filtrar os eventos que são recebidos durante o intervalo de Agrupamento especificado na [cláusula Within](within-clause.md). Por exemplo, uma instrução SELECT poderia ser construída para que não retorne nada, a menos que haja pelo menos 5 eventos dentro do intervalo de 30 segundos anteriores.

A cláusula WITHIN segue imediatamente na [instrução SELECT](select-statement-for-event-queries.md) após a cláusula [Group](group-clause.md) . A cláusula HAVING opera na propriedade **NumberOfEvents** da classe de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) , da qual o grupo criado pela cláusula Group é um membro. A cláusula HAVING pode usar todos os operadores relacionais padrão.

A sintaxe dela é a seguinte:

``` syntax
SELECT * FROM EventClass [WHERE property = value] 
  GROUP WITHIN interval [BY property_list]
  HAVING NumberOfEvents operator constant
```

O valor *EventClass* é a classe de evento da qual o evento é um membro e *Value* é o valor para a propriedade na qual a notificação é necessária. O intervalo é um inteiro sem sinal que representa o intervalo de agrupamento (em segundos) após o recebimento do primeiro evento. A lista de propriedades é uma lista delimitada por vírgula de uma ou mais propriedades que são incluídas na classe de evento. O operador é qualquer operador relacional. O valor constante é qualquer inteiro de 32 bits sem sinal que indique o número de eventos usados para filtragem.

Ao usar a cláusula HAVING, as cláusulas WHERE e BY são opcionais.

A consulta de evento a seguir solicita que as notificações da classe **EmailEvent** sejam agrupadas em um evento 300 segundos após o primeiro evento que o WMI recebe. Além disso, a consulta solicitará que a instância [**\_ \_ AggregateEvent**](--aggregateevent.md) seja entregue somente se o WMI receber mais de cinco eventos de email em 300 segundos.


```sql
SELECT * FROM EmailEvent GROUP WITHIN 300 HAVING NumberOfEvents > 5
```



O exemplo a seguir agrupa todos os eventos recebidos em 600 segundos (ou seja, 10 minutos) pelo **TargetInstance**. Propriedade **SourceName** . Neste exemplo, os eventos de agregação serão entregues somente se o número de eventos [**\_ NTLogEvent do Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) recebidos da mesma origem exceder 25. Tenha em mente que o operador ISA faz com que a propriedade **TargetInstance** da classe de sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) represente uma instância da classe **Win32 \_ NTLogEvent** .


```sql
SELECT * FROM __InstanceCreationEvent 
  WHERE TargetInstance ISA "Win32_NTLogEvent" 
  GROUP WITHIN 600 BY TargetInstance.SourceName
  HAVING NumberOfEvents > 25
```



 

 
