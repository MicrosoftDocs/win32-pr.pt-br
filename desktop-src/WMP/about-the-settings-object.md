---
title: sobre o objeto Configurações
description: sobre o objeto Configurações
ms.assetid: 941463e6-7928-438e-824e-e5e281421a4a
keywords:
- Windows Media Player, Configurações objeto
- modelo de objeto Windows Media Player, Configurações objeto
- modelo de objeto, objeto Configurações
- Windows Media Player ActiveX controle, Configurações objeto
- controle de ActiveX, Configurações objeto
- Windows Media Player controle de ActiveX móvel, Configurações objeto
- Windows Media Player celular, Configurações objeto
- objeto Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74b8bd9db946a2915486647fa5831158198bef6115a34b6bb9fb81177f433de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583668"
---
# <a name="about-the-settings-object"></a>sobre o objeto Configurações

o objeto **Configurações** governa as configurações do controle, como volume, contagem de reprodução, mudo e assim por diante. ele é acessado somente por meio da propriedade **Configurações** do objeto **Player** . a propriedade **Configurações** retorna o objeto **Configurações** . você só pode acessar as propriedades do objeto **Configurações** depois de tê-lo criado. Por exemplo, para obter o valor da propriedade **volume** , você deve usar o seguinte código:


```C++
myvolume = player.settings.volume;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> <dt>

[**Configurações Objeto**](settings-object.md)
</dt> </dl>

 

 




