---
title: A coleção Animationnames
description: A coleção Animationnames
ms.assetid: 3b06e497-1d03-43be-8d33-e69ef2972237
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c9ee781b836599ccf9689bfae974fd4cf3af32d75df2070e984ae9b6596f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960656"
---
# <a name="the-animationnames-collection"></a>A coleção Animationnames

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A coleção [**animationnames**](https://www.bing.com/search?q=**AnimationNames**) é uma coleção especial que contém a lista de nomes de animação compilados para um caractere. Você pode usar a coleção para enumerar os nomes das animações de um caractere. por exemplo, em Visual Basic ou VBScript (2,0 ou posterior), você pode acessar esses nomes usando o **para cada... Próximas** instruções:


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



Os itens na coleção não têm propriedades, portanto, itens individuais não podem ser acessados diretamente.

Fins. Os caracteres de ACF, a coleção retorna todas as animações que foram definidas para o caractere, não apenas aquelas que foram recuperadas com o método [**Get**](get-method.md) .

 

 




