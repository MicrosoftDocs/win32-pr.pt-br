---
title: Sobre o objeto de consulta
description: Sobre o objeto de consulta
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player, objeto de consulta
- Modelo de objeto do Windows Media Player, objeto de consulta
- modelo de objeto, objeto de consulta
- Controle ActiveX do Windows Media Player, objeto de consulta
- Controle ActiveX, objeto de consulta
- Controle ActiveX móvel do Windows Media Player, objeto de consulta
- Windows Media Player Mobile, objeto de consulta
- Objeto de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a26f60c38e053b91c7e56f5cbd7ccaf2ba0fe2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635999"
---
# <a name="about-the-query-object"></a><span data-ttu-id="ca196-111">Sobre o objeto de consulta</span><span class="sxs-lookup"><span data-stu-id="ca196-111">About the Query Object</span></span>

<span data-ttu-id="ca196-112">O objeto de **consulta** representa uma consulta composta.</span><span class="sxs-lookup"><span data-stu-id="ca196-112">The **Query** object represents a compound query.</span></span> <span data-ttu-id="ca196-113">Você cria um novo objeto de **consulta** vazio chamando *mediacollection*. **CreateQuery**.</span><span class="sxs-lookup"><span data-stu-id="ca196-113">You create a new, empty **Query** object by calling *mediaCollection*.**createQuery**.</span></span> <span data-ttu-id="ca196-114">Depois de criar um objeto de **consulta** , você pode chamar **addcondition** para adicionar uma condição à consulta composta.</span><span class="sxs-lookup"><span data-stu-id="ca196-114">After you have created a **Query** object, you can call **addCondition** to add a condition to the compound query.</span></span> <span data-ttu-id="ca196-115">Cada chamada subsequente para **addcondition** acrescenta uma nova condição à consulta existente usando and Logic.</span><span class="sxs-lookup"><span data-stu-id="ca196-115">Each subsequent call to **addCondition** appends a new condition to the existing query using AND logic.</span></span>

<span data-ttu-id="ca196-116">Por exemplo, suponha que você queira criar uma consulta que representa todas as mídias digitais em que o **WM/gênero** é igual a "Jazz" e o **autor** contém "Jim".</span><span class="sxs-lookup"><span data-stu-id="ca196-116">For example, suppose you want to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim".</span></span> <span data-ttu-id="ca196-117">Você pode criar uma consulta composta para representar essas condições usando o seguinte código JScript:</span><span class="sxs-lookup"><span data-stu-id="ca196-117">You could create a compound query to represent these conditions by using the following JScript code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



<span data-ttu-id="ca196-118">Para adicionar uma condição a uma consulta composta usando ou lógica, você deve chamar **Query. beginNextGroup**.</span><span class="sxs-lookup"><span data-stu-id="ca196-118">To add a condition to a compound query using OR logic, you must call **Query.beginNextGroup**.</span></span> <span data-ttu-id="ca196-119">Esse método sinaliza que o grupo de condição anterior foi concluído e que a próxima chamada para **addcondition** representa o início de um novo grupo de condição.</span><span class="sxs-lookup"><span data-stu-id="ca196-119">This method signals that the previous condition group is completed and that the next call to **addCondition** represents the start of a new condition group.</span></span>

<span data-ttu-id="ca196-120">Por exemplo, para criar uma consulta que representa todas as mídias digitais em que o **WM/gênero** é igual a "Jazz" e o **autor** contém "Jim" ou o **autor** contém "Dave", você pode usar o seguinte código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="ca196-120">For example, to create a query that represents all digital media where **WM/Genre** equals "Jazz" and **Author** contains "Jim" or **Author** contains "Dave", you could use the following example code:</span></span>


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");

// Start the next condition group. This group will be
// combined with the previous group using a logical OR operation.
Query.beginNextGroup();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Dave");
```



<span data-ttu-id="ca196-121">Para executar a consulta composta, chame **mediacollection. getPlaylistByQuery**.</span><span class="sxs-lookup"><span data-stu-id="ca196-121">To execute your compound query, call **MediaCollection.getPlaylistByQuery**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca196-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ca196-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca196-123">**Mediacollection. getPlaylistByQuery**</span><span class="sxs-lookup"><span data-stu-id="ca196-123">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="ca196-124">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="ca196-124">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="ca196-125">**Objeto de consulta**</span><span class="sxs-lookup"><span data-stu-id="ca196-125">**Query Object**</span></span>](query-object.md)
</dt> </dl>

 

 




