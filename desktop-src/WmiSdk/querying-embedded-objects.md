---
description: Você tem várias opções para o formulário que uma consulta usa ao consultar uma classe de evento que contém objetos incorporados. Os resultados retornados pela consulta variam de acordo com o formulário da consulta que você usa.
ms.assetid: b959a695-be15-4aa7-9368-b840962ae0da
ms.tgt_platform: multiple
title: Consultando objetos inseridos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed2e13bd9d9dc798891a723a6fed1b1734e1735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661770"
---
# <a name="querying-embedded-objects"></a><span data-ttu-id="6e13c-104">Consultando objetos inseridos</span><span class="sxs-lookup"><span data-stu-id="6e13c-104">Querying Embedded Objects</span></span>

<span data-ttu-id="6e13c-105">Você tem várias opções para o formulário que uma consulta usa ao consultar uma classe de evento que contém objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="6e13c-105">You have several options as to the form a query takes when querying an event class that contains embedded objects.</span></span> <span data-ttu-id="6e13c-106">Os resultados retornados pela consulta variam de acordo com o formulário da consulta que você usa.</span><span class="sxs-lookup"><span data-stu-id="6e13c-106">The results returned by the query vary, depending on the form of the query you use.</span></span>

## <a name="class-definitions"></a><span data-ttu-id="6e13c-107">Definições de classe</span><span class="sxs-lookup"><span data-stu-id="6e13c-107">Class Definitions</span></span>

<span data-ttu-id="6e13c-108">O exemplo a seguir mostra as definições de classe que são usadas para as consultas WQL neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6e13c-108">The following example shows the class definitions that are used for the WQL queries in this topic.</span></span>

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

## <a name="examples"></a><span data-ttu-id="6e13c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6e13c-109">Examples</span></span>

<span data-ttu-id="6e13c-110">A consulta a seguir retorna ambas as classes inseridas, **E1** e **E2**, cada uma com **Prop1** e **Prop2** populadas com dados.</span><span class="sxs-lookup"><span data-stu-id="6e13c-110">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`SELECT * FROM MyEvent`

<span data-ttu-id="6e13c-111">A consulta a seguir retorna o objeto **E1** Embedded, mas com nenhum **Prop1** nem **Prop2** populado com dados.</span><span class="sxs-lookup"><span data-stu-id="6e13c-111">The following query returns the **E1** embedded object, but with neither **Prop1** nor **Prop2** populated with data.</span></span>

`SELECT E1 FROM MyEvent`

<span data-ttu-id="6e13c-112">A consulta a seguir retorna a classe embutida **E1** com apenas **Prop1** populadas com dados.</span><span class="sxs-lookup"><span data-stu-id="6e13c-112">The following query returns the embedded class **E1** with only **Prop1** populated with data.</span></span>

`SELECT E1.Prop1 FROM MyEvent`

<span data-ttu-id="6e13c-113">A consulta a seguir retorna ambas as classes inseridas, **E1** e **E2**, cada uma com **Prop1** e **Prop2** populadas com dados.</span><span class="sxs-lookup"><span data-stu-id="6e13c-113">The following query returns both embedded classes, **E1** and **E2**, each having **Prop1** and **Prop2** populated with data.</span></span>

`ELECT E1.Prop1, E1.Prop2, E2.Prop1, E2.Prop2 FROM MyEvent`

<span data-ttu-id="6e13c-114">Isso é equivalente à primeira consulta usando o asterisco ( \* ) em vez de especificar cada objeto e propriedade.</span><span class="sxs-lookup"><span data-stu-id="6e13c-114">This is equivalent to the first query using the asterisk (\*) instead of specifying each object and property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e13c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e13c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e13c-116">Consultando com WQL</span><span class="sxs-lookup"><span data-stu-id="6e13c-116">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

 



