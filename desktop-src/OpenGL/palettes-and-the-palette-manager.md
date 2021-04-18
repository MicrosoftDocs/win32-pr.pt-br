---
title: Paletas e o Gerenciador de paleta
description: O Gerenciador de paleta do Windows, que faz parte da GDI, destina-se especificamente a adaptadores de vídeo de 8 bits com uma paleta de hardware de 256 entradas de cor.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL no Windows, Gerenciador de paleta
- OpenGL no Windows, paletas de hardware
- Gerenciador de paleta OpenGL
- paletas de hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750787"
---
# <a name="palettes-and-the-palette-manager"></a>Paletas e o Gerenciador de paleta

O Gerenciador de paleta do Windows, que faz parte da GDI, destina-se especificamente a adaptadores de vídeo de 8 bits com uma *paleta de hardware* de 256 entradas de cor. Os pixels na tela são armazenados como um índice de 8 bits na paleta de hardware. Cada entrada na paleta de hardware geralmente define uma cor de 24 bits (8 cada vermelho, verde e azul).

O Gerenciador de paleta mantém uma *paleta do sistema* que é uma cópia da paleta de hardware. A paleta do sistema é dividida em duas seções: 20 cores reservadas e as 236 cores restantes, que você pode definir usando o Gerenciador de paleta.

Uma *paleta lógica* padrão de 20 cores é selecionada e realizada em um contexto de dispositivo. Você pode criar e usar uma nova paleta lógica. Para alterar a paleta do sistema, selecione e perceba a paleta lógica que você criou.

Você provavelmente criará uma paleta lógica para especificar as cores que deseja exibir em seu aplicativo OpenGL. Usando determinadas chamadas GDI, você pode substituir temporariamente a maior parte da paleta do sistema por uma paleta lógica. Usando uma paleta lógica, você pode definir cores de pixel para a GDI usando o modo RGBA ou de índice de cor. O tamanho máximo de uma paleta lógica é de 256 cores para dispositivos de 8 bits e 4.096 cores em um dispositivo de cor real (16, 24 e 32 bits).

Para obter mais informações sobre os modos RGBA e de índice de cor, consulte [modo RGBA e gerenciamento de paleta do Windows](rgba-mode-and-windows-palette-management.md) e [modos de cores OpenGL e gerenciamento de paleta do Windows](opengl-color-modes-and-windows-palette-management.md).

 

 




