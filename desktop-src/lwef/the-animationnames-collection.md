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
# <a name="the-animationnames-collection"></a><span data-ttu-id="3b9ee-103">A coleção Animationnames</span><span class="sxs-lookup"><span data-stu-id="3b9ee-103">The AnimationNames Collection</span></span>

<span data-ttu-id="3b9ee-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3b9ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3b9ee-105">A coleção [**animationnames**](https://www.bing.com/search?q=**AnimationNames**) é uma coleção especial que contém a lista de nomes de animação compilados para um caractere.</span><span class="sxs-lookup"><span data-stu-id="3b9ee-105">The [**AnimationNames**](https://www.bing.com/search?q=**AnimationNames**) collection is a special collection that contains the list of animation names compiled for a character.</span></span> <span data-ttu-id="3b9ee-106">Você pode usar a coleção para enumerar os nomes das animações de um caractere.</span><span class="sxs-lookup"><span data-stu-id="3b9ee-106">You can use the collection to enumerate the names of the animations for a character.</span></span> <span data-ttu-id="3b9ee-107">Por exemplo, em Visual Basic ou VBScript (2,0 ou posterior), você pode acessar esses nomes usando o **para cada... Próximas** instruções:</span><span class="sxs-lookup"><span data-stu-id="3b9ee-107">For example, in Visual Basic or VBScript (2.0 or later) you can access these names using the **For Each...Next** statements:</span></span>


```
   For Each Animation in Genie.AnimationNames
      Genie.Play Animation
   Next
```



<span data-ttu-id="3b9ee-108">Os itens na coleção não têm propriedades, portanto, itens individuais não podem ser acessados diretamente.</span><span class="sxs-lookup"><span data-stu-id="3b9ee-108">Items in the collection have no properties, so individual items cannot be accessed directly.</span></span>

<span data-ttu-id="3b9ee-109">Fins. Os caracteres de ACF, a coleção retorna todas as animações que foram definidas para o caractere, não apenas aquelas que foram recuperadas com o método [**Get**](get-method.md) .</span><span class="sxs-lookup"><span data-stu-id="3b9ee-109">For .ACF characters, the collection returns all the animations that have been defined for the character, not just the ones that have been retrieved with the [**Get**](get-method.md) method.</span></span>

 

 




