---
title: Sobre o objeto DVD
description: Sobre o objeto DVD
ms.assetid: 6c255e9e-d537-4f4f-865c-b7fb26c8e413
keywords:
- Windows Media Player, objeto de DVD
- modelo de objeto Windows Media Player, objeto DVD
- modelo de objeto, objeto de DVD
- controle de ActiveX de Windows Media Player, objeto de DVD
- controle de ActiveX, objeto de DVD
- Windows Media Player controle de ActiveX móvel, objeto de DVD
- Windows Media Player Celular, objeto de DVD
- Objeto de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109587f30e7df0ff49b1cdbe5b45d818decb1a3f50ffe4a4ba9cde53d00833f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583758"
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

 

 




