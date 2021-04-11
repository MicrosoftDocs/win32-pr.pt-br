---
title: Sobre os objetos Error e ErrorItem
description: Sobre os objetos Error e ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, objeto de erro
- Modelo de objeto do Windows Media Player, objeto de erro
- modelo de objeto, objeto de erro
- Controle ActiveX do Windows Media Player, objeto de erro
- Controle ActiveX, objeto de erro
- Controle ActiveX móvel do Windows Media Player, objeto de erro
- Windows Media Player Mobile, objeto de erro
- Objeto de erro
- Windows Media Player, objeto ErrorItem
- Modelo de objeto do Windows Media Player, objeto ErrorItem
- modelo de objeto, objeto ErrorItem
- Controle ActiveX do Windows Media Player, objeto ErrorItem
- Controle ActiveX, objeto ErrorItem
- Controle ActiveX móvel do Windows Media Player, objeto ErrorItem
- Windows Media Player Mobile, objeto ErrorItem
- Objeto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292299"
---
# <a name="about-the-error-and-erroritem-objects"></a><span data-ttu-id="86f4c-119">Sobre os objetos Error e ErrorItem</span><span class="sxs-lookup"><span data-stu-id="86f4c-119">About the Error and ErrorItem Objects</span></span>

<span data-ttu-id="86f4c-120">Os objetos **Error** e **ErrorItem** regem os recursos de tratamento de erros do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="86f4c-120">The **Error** and **ErrorItem** objects govern the error-handling capabilities of Windows Media Player.</span></span> <span data-ttu-id="86f4c-121">O objeto de **erro** é obtido do objeto **Player** por meio da propriedade **Error** .</span><span class="sxs-lookup"><span data-stu-id="86f4c-121">The **Error** object is obtained from the **Player** object through the **error** property.</span></span> <span data-ttu-id="86f4c-122">Você pode obter um código específico do objeto de **erro** usando a propriedade **Item** do objeto **Error** para criar o objeto **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="86f4c-122">You can get a specific code from the **Error** object by using the **item** property of the **Error** object to create the **ErrorItem** object.</span></span> <span data-ttu-id="86f4c-123">Por exemplo, para obter o código de erro do primeiro item de erro, digite:</span><span class="sxs-lookup"><span data-stu-id="86f4c-123">For example, to get the error code of the first error item, type:</span></span>


```C++
myerrorcode = player.error.item(0).errorCode;

```



<span data-ttu-id="86f4c-124">Você também pode invocar a ajuda da Web com o objeto de **erro** usando o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="86f4c-124">You can also invoke Web Help with the **Error** object by using the following code:</span></span>


```C++
player.error.webHelp();

```



## <a name="related-topics"></a><span data-ttu-id="86f4c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86f4c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f4c-126">**Objeto Error**</span><span class="sxs-lookup"><span data-stu-id="86f4c-126">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="86f4c-127">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="86f4c-127">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="86f4c-128">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="86f4c-128">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




