---
description: Descreve a sintaxe básica de uma instrução SELECT para consultas de evento.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instrução SELECT para consultas de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e36eaa8f396f8dd7b7c0b0c013d1d6738fefeb7ed2ae565ee7114ebb524faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315835"
---
# <a name="select-statement-for-event-queries"></a>Instrução SELECT para consultas de evento

Você pode usar uma variedade de instruções SELECT para consultar informações de evento. As instruções podem ser instruções básicas ou podem ser mais restritivas para restringir o conjunto de resultados retornado da consulta.

O exemplo a seguir é uma instrução SELECT básica que é usada para consultar informações de evento.


```sql
SELECT * FROM EventClass
```



Quando um consumidor envia uma consulta, é uma solicitação a ser notificada de todas as ocorrências do evento representado por **EventClass**. Essa solicitação inclui uma solicitação de notificação sobre todas as propriedades do sistema de eventos e não sistema. Quando um provedor de eventos envia uma consulta, ele registra o suporte para gerar notificações quando ocorre um evento representado por **EventClass.**

Os consumidores podem especificar propriedades individuais em vez do asterisco ( \* ) na instrução SELECT.

O exemplo a seguir mostra como consultar propriedades específicas.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



No entanto, todas as propriedades de um objeto inserido são retornadas, mesmo que a consulta especifique as propriedades do objeto inserido.

O exemplo a seguir mostra duas consultas que retornam os mesmos dados.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Se uma propriedade do sistema não for relevante para uma consulta específica, ela conterá **NULL.** Por exemplo, o valor da propriedade do sistema **\_ \_ RELPATH** é **NULL para** todas as consultas de evento.

As seguintes propriedades do sistema **contêm NULL** para consultas de evento:

<dl> \_\_Namespace  
\_\_Caminho  
\_\_Relpath  
\_\_Servidor  
</dl>

Para obter mais informações, consulte [Referência de propriedade do sistema WMI](wmi-system-properties.md).

Todas as consultas de evento podem incluir uma [cláusula WHERE](where-clause.md)opcional, mas as cláusulas WHERE são usadas principalmente pelos consumidores para especificar filtragem adicional. É altamente recomendável que os consumidores sempre especifiquem uma cláusula WHERE. O custo de uma consulta complexa é mínimo em comparação com o custo de entrega e processamento de notificações não obrigatórias.

O exemplo a seguir mostra uma consulta que solicita notificações de todos os eventos de modificação de instância que afetam a classe hipotética **EmailEvent**.


```sql
SELECT * FROM EmailEvent
```



Se eventos associados ao **EmailEvent** ocorrerem com frequência, o consumidor será inundado por eventos. Uma consulta melhor solicita eventos somente quando condições específicas usam propriedades da classe especificada, como quando o nível de importância é alto.

O exemplo a seguir mostra a consulta que você pode usar se **EmailImportance** for uma propriedade da **classe EmailEvent**.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Observe que o WMI pode rejeitar uma consulta por vários motivos. Por exemplo, a consulta pode ser muito complexa ou com uso intensivo de recursos para avaliação. Quando isso ocorre, o WMI retorna códigos de erro específicos, como **WBEM \_ E \_ INVALID \_ QUERY.**

As propriedades de objetos inseridos podem ser usadas na cláusula WHERE.

O exemplo a seguir mostra como consultar objetos em que a propriedade **TargetInstance** da classe do sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) é um objeto [**\_ LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) inserido e **FreeSpace** é uma propriedade de **Win32 \_ LogicalDisk**.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Exemplos

O [evento de](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) criação monitor para o exemplo de VBScript de nome de processo específico no TechNet usa a instrução SELECT para monitorar eventos de criação de instância WMI para o Processo Win32, filtrando um nome de processo \_ específico.

 

 
