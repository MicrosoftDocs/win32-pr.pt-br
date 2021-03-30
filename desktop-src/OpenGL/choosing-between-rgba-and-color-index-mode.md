---
title: Escolhendo entre o modo RGBA e Color-Index
description: Em geral, use o modo RGBA para seus aplicativos OpenGL; Ele fornece mais flexibilidade do que o modo de índice de cor para efeitos como sombreamento, iluminação, mapeamento de cores, neblina, antialiasing e mistura.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL no Windows, modo RGBA
- OpenGL no Windows, modo de índice de cor
- Modo RGBA OpenGL
- modo de índice de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635876"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Escolhendo entre o modo RGBA e Color-Index

Em geral, use o modo RGBA para seus aplicativos OpenGL; Ele fornece mais flexibilidade do que o modo de índice de cor para efeitos como sombreamento, iluminação, mapeamento de cores, neblina, antialiasing e mistura.

Considere o uso do modo de índice de cor nos seguintes casos:

-   Se você tiver um número limitado de bitplanes disponíveis; o modo de índice de cor pode produzir sombreamento menos baixo que o modo RGBA.
-   Se você não estiver preocupado com o uso de cores "reais"; por exemplo, usar várias cores em um mapa Topographic para designar elevações relativas.
-   Quando você está portando um aplicativo existente que usa o modo de índice de cor extensivamente.
-   Quando você quiser usar a animação de mapa de cores e efeitos em seu aplicativo. (Isso não é possível em dispositivos true-color.)

 

 




