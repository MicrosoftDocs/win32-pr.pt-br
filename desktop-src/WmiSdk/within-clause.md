---
description: Use a cláusula WITHIN em consultas de evento para especificar um intervalo de sondagem ou um intervalo de agrupamento.
ms.assetid: e2fc7627-fb3d-4966-b38b-441333868ae3
ms.tgt_platform: multiple
title: Cláusula WITHIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee35350a52ef6af1aa22aacf775d22b3c7629fb479967a74aed1408aa5e1f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757596"
---
# <a name="within-clause"></a>Cláusula WITHIN

Os consumidores de eventos usam a cláusula WITHIN em consultas de evento para especificar um *intervalo de sondagem* ou um *intervalo de agrupamento*.

um intervalo de sondagem é o intervalo que Instrumentação de Gerenciamento do Windows (WMI) usa para sondar o provedor de dados responsável pela classe para [eventos intrínsecos](determining-the-type-of-event-to-receive.md), dos quais o evento consultado é um membro. Este intervalo é o período máximo de tempo que pode ser decorrido antes que um evento de notificação precise ser entregue. Um consumidor usa um intervalo de sondagem em uma cláusula WITHIN quando o consumidor requer notificação de alterações em uma classe e um provedor de eventos não está disponível. O consumidor registra um evento intrínseco e inclui o intervalo de sondagem.

Para especificar um intervalo de sondagem, coloque a cláusula WITHIN imediatamente antes da cláusula WHERE, conforme mostrado a seguir:


```sql
SELECT * FROM IntrinsicEventClass WITHIN interval  WHERE property = value
```



IntrinsicEventClass é a classe de evento intrínseca da qual o evento é um membro, Interval é o intervalo de sondagem e Value é o valor para a propriedade na qual o consumidor requer notificação.

O intervalo de sondagem é um número de ponto flutuante e pode ser fracionário para aceitar valores menores que 1 segundo. No entanto, o intervalo deve representar um número de segundos em vez de um valor extremamente pequeno, como 0, 1, porque a especificação de um valor muito pequeno pode fazer com que o WMI rejeite a instrução como inválida — devido à natureza de sondagem intensiva de recursos. Como a maioria dos consumidores de eventos não requer notificação imediata, é recomendável que eles usem um intervalo maior do que 5 minutos.

O exemplo de consulta a seguir solicita que o WMI Verifique a cada 10 segundos se há alterações que ocorrem em instâncias da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Se uma instância da classe for modificada dentro do intervalo de sondagem especificado, um evento de notificação será enviado para cada modificação.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 10  WHERE TargetInstance ISA "Win32_LogicalDisk"
```



Dependendo da consulta, um provedor de eventos e o WMI podem compartilhar a tarefa de fornecer eventos. Por exemplo, um provedor de eventos que dá suporte a eventos das classes de sistema [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md) e [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) , e não a eventos da classe de sistema [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) . A consulta a seguir permite que o provedor de eventos gere os eventos de criação e modificação à medida que eles ocorrem e os tenha entregue quando forem criados. A consulta também permite que o WMI gere eventos **\_ \_ InstanceDeletionEvent** a cada 10 (dez) segundos usando o mecanismo de sondagem.


```sql
SELECT * FROM __InstanceOperationEvent WITHIN 10  WHERE TargetInstance ISA "MyOwnClass"
```



Você também pode usar a cláusula WITHIN para especificar um intervalo de agrupamento. Um intervalo de agrupamento é um inteiro de 32 bits sem sinal que especifica o período de tempo, após o recebimento de um evento inicial, durante o qual o WMI deve coletar eventos semelhantes. Quando esse período de tempo expira, o WMI entrega o evento de agregação, composto de todos os eventos semelhantes. Para obter mais informações, consulte [Group Clause](group-clause.md).

Os consumidores de eventos que se registram para eventos que ocorrem com frequência usam um intervalo de agrupamento com a cláusula WITHIN. Adicionar o grupo dentro da cláusula WHERE em uma consulta de evento faz com que o WMI envie um evento de agregação em vez de muitos eventos. O evento de agregação é representado pela classe de sistema [**\_ \_ AggregateEvent**](--aggregateevent.md) .

Para especificar um intervalo de agrupamento, coloque a cláusula WITHIN imediatamente após a cláusula GROUP.


```sql
SELECT * FROM EventClass WHERE property = value GROUP WITHIN Interval
```



EventClass é a classe de evento da qual o evento é um membro, value é o valor para a propriedade na qual o consumidor requer notificação e Interval é o intervalo de agrupamento.

Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

Os consumidores de eventos permanentes podem ser criados com consultas de sondagem somente se você tiver privilégios de administrador.

 

 
