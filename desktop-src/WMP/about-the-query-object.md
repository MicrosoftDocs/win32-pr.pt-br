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
# <a name="about-the-query-object"></a>Sobre o objeto de consulta

O objeto de **consulta** representa uma consulta composta. Você cria um novo objeto de **consulta** vazio chamando *mediacollection*. **CreateQuery**. Depois de criar um objeto de **consulta** , você pode chamar **addcondition** para adicionar uma condição à consulta composta. Cada chamada subsequente para **addcondition** acrescenta uma nova condição à consulta existente usando and Logic.

Por exemplo, suponha que você queira criar uma consulta que representa todas as mídias digitais em que o **WM/gênero** é igual a "Jazz" e o **autor** contém "Jim". Você pode criar uma consulta composta para representar essas condições usando o seguinte código JScript:


```C++
// Create the query object.
var Query = player.mediaCollection.createQuery();

// Add the conditions.
Query.addCondition("WM/Genre", "Equals", "Jazz");
Query.addCondition("Author", "Contains", "Jim");
```



Para adicionar uma condição a uma consulta composta usando ou lógica, você deve chamar **Query. beginNextGroup**. Esse método sinaliza que o grupo de condição anterior foi concluído e que a próxima chamada para **addcondition** representa o início de um novo grupo de condição.

Por exemplo, para criar uma consulta que representa todas as mídias digitais em que o **WM/gênero** é igual a "Jazz" e o **autor** contém "Jim" ou o **autor** contém "Dave", você pode usar o seguinte código de exemplo:


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



Para executar a consulta composta, chame **mediacollection. getPlaylistByQuery**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Mediacollection. getPlaylistByQuery**](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objeto de consulta**](query-object.md)
</dt> </dl>

 

 




