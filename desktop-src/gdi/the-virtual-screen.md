---
description: O retângulo delimitador de todos os monitores é a tela virtual. A área de trabalho cobre a tela virtual em vez de um único monitor. A ilustração a seguir mostra uma possível disposição de três monitores.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: A tela virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5516ef0cb5d99124200ab7810e484ea79027cf832a0e8da74833bf709ce5cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037514"
---
# <a name="the-virtual-screen"></a>A tela virtual

O retângulo delimitador de todos os monitores é a *tela virtual*. A área de trabalho cobre a tela virtual em vez de um único monitor. A ilustração a seguir mostra uma possível disposição de três monitores.

![ilustração mostrando três caixas que representam monitores organizados em uma caixa que representa a tela virtual](images/multimon-1.png)

O *monitor primário* contém a origem (0, 0). Isso é para compatibilidade com aplicativos existentes que esperam um monitor com uma origem. No entanto, o monitor primário não precisa estar no canto superior esquerdo da tela virtual. Na Figura 1, é próximo do centro. Quando o monitor primário não está no canto superior esquerdo da tela virtual, partes da tela virtual têm coordenadas negativas. Como a organização dos monitores é definida pelo usuário, todos os aplicativos devem ser projetados para trabalhar com coordenadas negativas. Para obter mais informações, consulte [várias considerações de monitor para programas mais antigos](multiple-monitor-considerations-for-older-programs.md).

As coordenadas da tela virtual são representadas por um valor de 16 bits assinado devido aos valores de 16 bits contidos em muitas mensagens existentes. Assim, os limites da tela virtual são:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



