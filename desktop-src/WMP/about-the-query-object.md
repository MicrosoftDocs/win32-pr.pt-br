---
title: Sobre o objeto de consulta
description: Sobre o objeto de consulta
ms.assetid: 41488036-bdcf-4fe6-8f7e-f0897157d3d9
keywords:
- Windows Media Player, objeto de consulta
- modelo de objeto Windows Media Player, objeto de consulta
- modelo de objeto, objeto de consulta
- controle de ActiveX de Windows Media Player, objeto de consulta
- controle de ActiveX, objeto de consulta
- Windows Media Player controle de ActiveX móvel, objeto de consulta
- Windows Media Player Móvel, objeto de consulta
- Objeto de consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d649263f981d02e106466c6e0fcada99c316054d4bf6e0acc0faca641c75dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470396"
---
# <a name="about-the-query-object"></a>Sobre o objeto de consulta

O objeto de **consulta** representa uma consulta composta. Você cria um novo objeto de **consulta** vazio chamando *mediacollection*. **CreateQuery**. Depois de criar um objeto de **consulta** , você pode chamar **addcondition** para adicionar uma condição à consulta composta. Cada chamada subsequente para **addcondition** acrescenta uma nova condição à consulta existente usando and Logic.

Por exemplo, suponha que você queira criar uma consulta que representa todas as mídias digitais em que o **WM/gênero** é igual a "Jazz" e o **autor** contém "Jim". você pode criar uma consulta composta para representar essas condições usando o seguinte código de JScript:


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

 

 




