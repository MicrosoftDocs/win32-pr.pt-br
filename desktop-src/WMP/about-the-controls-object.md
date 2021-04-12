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
# <a name="about-the-controls-object"></a>Sobre o objeto Controls

O objeto **Controls** governa o transporte de conteúdo de mídia digital por meio do controle usando métodos como **Play** e **Stop**. Ele é acessado somente por meio da propriedade **Controls** do objeto **Player** . A propriedade **Controls** retorna o objeto **Controls** . Você só pode acessar as propriedades do objeto **Controls** depois de criá-lo. Por exemplo, para usar o método **Play** , você deve usar o seguinte código:


```C++
player.controls.play();

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto Controls**](controls-object.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




