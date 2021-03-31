---
title: A coleção Animationnames
description: A coleção Animationnames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9e0c2c1d42f51f9d50bafaee61b6ab51d5b85f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822644"
---
# <a name="the-animationnames-collection"></a>A coleção Animationnames

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A coleção [**animationnames**](https://www.bing.com/search?q=**AnimationNames**) é uma coleção especial que contém a lista de nomes de animação compilados para um caractere. Você pode usar a coleção para enumerar os nomes das animações de um caractere. Por exemplo, em Visual Basic ou VBScript (2,0 ou posterior), você pode acessar esses nomes usando o **para cada... Próximas** instruções:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Os itens na coleção não têm propriedades, portanto, itens individuais não podem ser acessados diretamente.

Fins. Os caracteres de ACF, a coleção retorna todas as animações que foram definidas para o caractere, não apenas aquelas que foram recuperadas com o método [**Get**](get-method.md) .

 

 




