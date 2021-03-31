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
# <a name="about-the-settings-object"></a>Sobre o objeto de configurações

O objeto de **configurações** governa as configurações do controle, como volume, contagem de reprodução, mudo e assim por diante. Ele é acessado somente por meio da propriedade **Settings** do objeto **Player** . A propriedade **Settings** retorna o objeto **Settings** . Você só pode acessar as propriedades do objeto de **configurações** depois de criá-lo. Por exemplo, para obter o valor da propriedade **volume** , você deve usar o seguinte código:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Objeto de configurações**](settings-object.md)
</dt> </dl>

 

 




