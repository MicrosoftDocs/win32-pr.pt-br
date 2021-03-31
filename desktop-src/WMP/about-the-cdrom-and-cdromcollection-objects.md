---
title: Sobre os objetos cdrom e cdromCollection
description: Sobre os objetos cdrom e cdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player, objeto de cdrom
- Modelo de objeto do Windows Media Player, objeto cdrom
- modelo de objeto, objeto cdrom
- Controle ActiveX do Windows Media Player, objeto cdrom
- Controle ActiveX, objeto cdrom
- Controle ActiveX móvel do Windows Media Player, objeto cdrom
- Windows Media Player Mobile, objeto de cdrom
- Objeto cdrom
- Windows Media Player, o objeto cdromCollection
- Modelo de objeto do Windows Media Player, objeto cdromCollection
- modelo de objeto, objeto cdromCollection
- Controle ActiveX do Windows Media Player, objeto cdromCollection
- Controle ActiveX, objeto cdromCollection
- Controle ActiveX móvel do Windows Media Player, objeto cdromCollection
- Windows Media Player Mobile, o objeto cdromCollection
- Objeto cdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636202"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a><span data-ttu-id="d71be-119">Sobre os objetos cdrom e cdromCollection</span><span class="sxs-lookup"><span data-stu-id="d71be-119">About the Cdrom and CdromCollection Objects</span></span>

<span data-ttu-id="d71be-120">Os objetos **cdrom** e **cdromCollection** regem a interface para as unidades de CD no seu computador para fins de leitura e reprodução de CDs.</span><span class="sxs-lookup"><span data-stu-id="d71be-120">The **Cdrom** and **CdromCollection** objects govern the interface to the CD drives in your computer for purposes of reading and playing CDs.</span></span>

<span data-ttu-id="d71be-121">O objeto **cdromCollection** é acessado somente por meio da propriedade **cdromCollection** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="d71be-121">The **CdromCollection** object is accessed only through the **cdromCollection** property of the **Player** object.</span></span> <span data-ttu-id="d71be-122">A propriedade **cdromCollection** retorna o objeto **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="d71be-122">The **cdromCollection** property returns the **CdromCollection** object.</span></span> <span data-ttu-id="d71be-123">Você só pode acessar as propriedades do objeto **cdromCollection** depois de criá-lo.</span><span class="sxs-lookup"><span data-stu-id="d71be-123">You can only access the properties of the **CdromCollection** object after you have created it.</span></span> <span data-ttu-id="d71be-124">Por exemplo, para usar a propriedade **Count** , você deve usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="d71be-124">For example, to use the **count** property, you must use the following code:</span></span>


```C++
mycount = player.cdromcollection.count;
```



<span data-ttu-id="d71be-125">Você só pode acessar o objeto **cdrom** por meio do objeto **cdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="d71be-125">You can only access the **Cdrom** object through the **CdromCollection** object.</span></span> <span data-ttu-id="d71be-126">Por exemplo, para ejetar o CD usando o método **EJECT** , você deve primeiro criar o objeto de coleção e, em seguida, um item no objeto.</span><span class="sxs-lookup"><span data-stu-id="d71be-126">For example, to eject the CD by using the **Eject** method, you must first create the collection object and then an item in the object.</span></span> <span data-ttu-id="d71be-127">Para ejetar o CD, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="d71be-127">To eject the CD, use the following code:</span></span>


```C++
player.cdromcollection.item(0).eject();
```



<span data-ttu-id="d71be-128">Em ambos os casos, primeiro você está criando o objeto de coleção (**cdromCollection**) e, em seguida, obtendo um objeto específico dessa coleção.</span><span class="sxs-lookup"><span data-stu-id="d71be-128">In both cases, you are first creating the collection object (**CdromCollection**) and then getting a specific object of that collection.</span></span> <span data-ttu-id="d71be-129">O objeto é o primeiro item da coleção, **Item**(0), que corresponde à primeira unidade de CD.</span><span class="sxs-lookup"><span data-stu-id="d71be-129">The object is the first item in the collection, **Item**(0), which corresponds to the first CD drive.</span></span> <span data-ttu-id="d71be-130">Em seguida, você chama um método, **EJECT**, nesse item.</span><span class="sxs-lookup"><span data-stu-id="d71be-130">You then call a method, **Eject**, on that item.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d71be-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d71be-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d71be-132">**Objeto cdrom**</span><span class="sxs-lookup"><span data-stu-id="d71be-132">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="d71be-133">**Objeto cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="d71be-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="d71be-134">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="d71be-134">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




