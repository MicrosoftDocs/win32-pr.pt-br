---
description: Você tem várias opções para o formulário que uma consulta usa ao consultar uma classe de evento que contém objetos incorporados. Os resultados retornados pela consulta variam de acordo com o formulário da consulta que você usa.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Consultando objetos inseridos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af6e0933ae12bb5867ff2ad446928d1b55f5ee7c2022ec60f53de61a3bd4bb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130908"
---
# <a name="querying-embedded-objects"></a>Consultando objetos inseridos

Você tem várias opções para o formulário que uma consulta usa ao consultar uma classe de evento que contém objetos incorporados. Os resultados retornados pela consulta variam de acordo com o formulário da consulta que você usa.

## <a name="class-definitions"></a>Definições de classe

O exemplo a seguir mostra as definições de classe que são usadas para as consultas WQL neste tópico.

``` syntax
class MyClass
{
   string Prop1;
   string Prop2;
};

class MyEvent : __ExtrinsicEvent
{
   MyClass E1;
   MyClass E2;
};
```

## <a name="examples"></a>Exemplos

A consulta a seguir retorna ambas as classes inseridas, **E1** e **E2**, cada uma com **Prop1** e **Prop2** populadas com dados.

`SELECT * FROM MyEvent`

A consulta a seguir retorna o objeto **E1** Embedded, mas com nenhum **Prop1** nem **Prop2** populado com dados.

`SELECT E1 FROM MyEvent`

A consulta a seguir retorna a classe embutida **E1** com apenas **Prop1** populadas com dados.

`SELECT E1.Prop1 FROM MyEvent`

A consulta a seguir retorna ambas as classes inseridas, **E1** e **E2**, cada uma com **Prop1** e **Prop2** populadas com dados.

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

Isso é equivalente à primeira consulta usando o asterisco ( \* ) em vez de especificar cada objeto e propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Consultando com WQL](querying-with-wql.md)
</dt> </dl>

 

 



