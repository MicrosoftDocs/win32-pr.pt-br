---
title: Sobre o objeto de rede
description: Sobre o objeto de rede
ms.assetid: 367a51d4-2db8-4c9e-82b7-85b2b631c721
keywords:
- Windows Media Player, objeto de rede
- modelo de objeto Windows Media Player, objeto de rede
- modelo de objeto, objeto de rede
- controle de ActiveX de Windows Media Player, objeto de rede
- controle de ActiveX, objeto de rede
- Windows Media Player controle de ActiveX móvel, objeto de rede
- Windows Media Player Celular, objeto de rede
- Objeto de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0378b1cd4469f6141a4ea60021f2d54e5c32b33ae1943624f7c65f70aa2a655f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903286"
---
# <a name="about-the-network-object"></a>Sobre o objeto de rede

O objeto de **rede** rege as propriedades que permitem determinar o quão bem o conteúdo é transmitido pela rede. Por exemplo, você pode descobrir se os pacotes estão sendo perdidos e tomar a ação apropriada. O objeto de **rede** é acessado somente por meio da propriedade **Network** do objeto **Player** . A propriedade **Network** retorna o objeto de **rede** . Você só pode acessar as propriedades do objeto de **rede** depois de tê-lo criado. Por exemplo, para usar a propriedade **Bandwidth** , você deve usar o seguinte código:


```C++
mybandwidth = player.network.bandwidth;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de rede**](network-object.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




