---
title: Sobre o objeto de configurações
description: Sobre o objeto de configurações
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, objeto de configurações
- Modelo de objeto do Windows Media Player, objeto de configurações
- modelo de objeto, objeto de configurações
- Controle ActiveX do Windows Media Player, objeto Settings
- Controle ActiveX, objeto Settings
- Controle ActiveX móvel do Windows Media Player, objeto de configurações
- Windows Media Player Mobile, objeto de configurações
- Objeto de configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20dae51d42e6c67a59ddc23dca19bc7f4180001
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822344"
---
# <a name="about-the-settings-object"></a><span data-ttu-id="cf991-111">Sobre o objeto de configurações</span><span class="sxs-lookup"><span data-stu-id="cf991-111">About the Settings Object</span></span>

<span data-ttu-id="cf991-112">O objeto de **configurações** governa as configurações do controle, como volume, contagem de reprodução, mudo e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cf991-112">The **Settings** object governs the settings of the control such as volume, play count, mute, and so on.</span></span> <span data-ttu-id="cf991-113">Ele é acessado somente por meio da propriedade **Settings** do objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="cf991-113">It is accessed only through the **Settings** property of the **Player** object.</span></span> <span data-ttu-id="cf991-114">A propriedade **Settings** retorna o objeto **Settings** .</span><span class="sxs-lookup"><span data-stu-id="cf991-114">The **Settings** property returns the **Settings** object.</span></span> <span data-ttu-id="cf991-115">Você só pode acessar as propriedades do objeto de **configurações** depois de criá-lo.</span><span class="sxs-lookup"><span data-stu-id="cf991-115">You can only access the properties of the **Settings** object after you have created it.</span></span> <span data-ttu-id="cf991-116">Por exemplo, para obter o valor da propriedade **volume** , você deve usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="cf991-116">For example, to get the value of the **Volume** property, you must use the following code:</span></span>


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a><span data-ttu-id="cf991-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf991-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf991-118">**Modelo de objeto do Player para linguagens de script**</span><span class="sxs-lookup"><span data-stu-id="cf991-118">**Player Object Model for Scripting Languages**</span></span>](player-object-model-for-scripting-languages.md)
</dt> <dt>

[<span data-ttu-id="cf991-119">**Objeto de configurações**</span><span class="sxs-lookup"><span data-stu-id="cf991-119">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 




