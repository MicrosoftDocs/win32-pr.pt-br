---
title: Sobre o objeto de rede
description: Sobre o objeto de rede
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player, objeto de rede
- Modelo de objeto do Windows Media Player, objeto de rede
- modelo de objeto, objeto de rede
- Controle ActiveX do Windows Media Player, objeto de rede
- Controle ActiveX, objeto de rede
- Controle ActiveX móvel do Windows Media Player, objeto de rede
- Windows Media Player Mobile, objeto de rede
- Objeto de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f3ff892a4d5b078956c9d126d0efaa844031d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635002"
---
# <a name="about-the-network-object"></a><span data-ttu-id="72257-111">Sobre o objeto de rede</span><span class="sxs-lookup"><span data-stu-id="72257-111">About the Network Object</span></span>

<span data-ttu-id="72257-112">O objeto de **rede** rege as propriedades que permitem determinar o quão bem o conteúdo é transmitido pela rede.</span><span class="sxs-lookup"><span data-stu-id="72257-112">The **Network** object governs the properties that allow you to determine how well the content is streaming through the network.</span></span> <span data-ttu-id="72257-113">Por exemplo, você pode descobrir se os pacotes estão sendo perdidos e tomar a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="72257-113">For example, you can find out whether packets are being lost and take appropriate action.</span></span> <span data-ttu-id="72257-114">O objeto de **rede** é acessado somente por meio da propriedade **Network** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="72257-114">The **Network** object is accessed only through the **network** property of the **Player** object.</span></span> <span data-ttu-id="72257-115">A propriedade **Network** retorna o objeto de **rede** .</span><span class="sxs-lookup"><span data-stu-id="72257-115">The **network** property returns the **Network** object.</span></span> <span data-ttu-id="72257-116">Você só pode acessar as propriedades do objeto de **rede** depois de tê-lo criado.</span><span class="sxs-lookup"><span data-stu-id="72257-116">You can only access the properties of the **Network** object after you have created it.</span></span> <span data-ttu-id="72257-117">Por exemplo, para usar a propriedade **Bandwidth** , você deve usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="72257-117">For example, to use the **Bandwidth** property, you must use the following code:</span></span>


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a><span data-ttu-id="72257-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72257-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72257-119">**Objeto de rede**</span><span class="sxs-lookup"><span data-stu-id="72257-119">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="72257-120">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="72257-120">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




