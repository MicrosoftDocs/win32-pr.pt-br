---
title: Sobre o objeto DVD
description: Sobre o objeto DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player, objeto de DVD
- Modelo de objeto do Windows Media Player, objeto de DVD
- modelo de objeto, objeto de DVD
- Controle ActiveX do Windows Media Player, objeto DVD
- Controle ActiveX, objeto DVD
- Controle ActiveX móvel do Windows Media Player, objeto DVD
- Windows Media Player Mobile, objeto de DVD
- Objeto de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b9432fa90e409b40f9e1acd3e7686628bca3d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291820"
---
# <a name="about-the-dvd-object"></a>Sobre o objeto DVD

O objeto **DVD** adiciona a funcionalidade específica à mídia de DVD. Em um sentido geral, a mídia de DVD é tratada da mesma forma que outras mídias digitais no Windows Media Player. Por exemplo, as unidades de DVD são enumeradas usando o objeto **cdromCollection** e os títulos e capítulos do DVD são manipulados usando objetos de **lista de reprodução** e objetos de **mídia** . Algumas funcionalidades são específicas de DVD, no entanto, e o objeto **DVD** fornece isso. Por exemplo, o DVD tem um conceito chamado domínio. Para recuperar o domínio atual para mídia de DVD, digite o seguinte:


```C++
mydomain = player.dvd.domain;

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




