---
title: Sobre o objeto Controls
description: Sobre o objeto Controls
ms.assetid: 1678c931-af47-42c9-a8a5-b6b775aebda8
keywords:
- Windows Media Player, objeto de controles
- Modelo de objeto do Windows Media Player, objeto de controles
- modelo de objeto, objeto Controls
- Controle ActiveX do Windows Media Player, objeto de controles
- Controle ActiveX, objeto Controls
- Controle ActiveX móvel do Windows Media Player, objeto Controls
- Windows Media Player Mobile, objeto Controls
- Objeto Controls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f064ef65401876dedb4181ba788788f5e5d9676c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363680"
---
# <a name="about-the-controls-object"></a><span data-ttu-id="10527-111">Sobre o objeto Controls</span><span class="sxs-lookup"><span data-stu-id="10527-111">About the Controls Object</span></span>

<span data-ttu-id="10527-112">O objeto **Controls** governa o transporte de conteúdo de mídia digital por meio do controle usando métodos como **Play** e **Stop**.</span><span class="sxs-lookup"><span data-stu-id="10527-112">The **Controls** object governs the transport of digital media content through the control by using methods such as **Play** and **Stop**.</span></span> <span data-ttu-id="10527-113">Ele é acessado somente por meio da propriedade **Controls** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="10527-113">It is accessed only through the **Controls** property of the **Player** object.</span></span> <span data-ttu-id="10527-114">A propriedade **Controls** retorna o objeto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="10527-114">The **Controls** property returns the **Controls** object.</span></span> <span data-ttu-id="10527-115">Você só pode acessar as propriedades do objeto **Controls** depois de criá-lo.</span><span class="sxs-lookup"><span data-stu-id="10527-115">You can only access the properties of the **Controls** object after you have created it.</span></span> <span data-ttu-id="10527-116">Por exemplo, para usar o método **Play** , você deve usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="10527-116">For example, to use the **Play** method, you must use the following code:</span></span>


```C++
player.controls.play();

```



## <a name="related-topics"></a><span data-ttu-id="10527-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10527-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10527-118">**Objeto Controls**</span><span class="sxs-lookup"><span data-stu-id="10527-118">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="10527-119">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="10527-119">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




