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

 

 




