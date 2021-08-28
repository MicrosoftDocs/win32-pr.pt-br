---
title: Paletas e o Gerenciador de Paletas
description: O Windows Palette Manager, que faz parte do GDI, tem como alvo especificamente adaptadores de exibição de 8 bits com uma paleta de hardware de 256 entradas de cores.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL no Windows, gerenciador de paleta
- OpenGL em Windows, paletas de hardware
- gerenciador de paletas OpenGL
- paletas de hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58407a5ddafe862caa73edd498c4da529b0ac987880828177d0d0b284601efed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936272"
---
# <a name="palettes-and-the-palette-manager"></a>Paletas e o Gerenciador de Paletas

O Windows Palette Manager, que faz parte do GDI, tem como alvo especificamente adaptadores de exibição de 8 bits com uma paleta de *hardware* de 256 entradas de cores. Os pixels na tela são armazenados como um índice de 8 bits na paleta de hardware. Cada entrada na paleta de hardware geralmente define uma cor de 24 bits (8 cada uma de vermelho, verde e azul).

O Gerenciador de Paleta mantém uma *paleta de sistema* que é uma cópia da paleta de hardware. A paleta do sistema é dividida em duas seções: 20 cores reservadas e as 236 cores restantes, que você pode definir usando o Gerenciador de Paletas.

Uma paleta lógica padrão de 20 cores *é* selecionada e realizada em um contexto de dispositivo. Você pode criar e usar uma nova paleta lógica. Para alterar a paleta do sistema, selecione e realize a paleta lógica que você criou.

Você provavelmente criará uma paleta lógica para especificar as cores que deseja exibir em seu aplicativo OpenGL. Usando determinadas chamadas GDI, você pode substituir temporariamente a maior parte da paleta do sistema por uma paleta lógica. Usando uma paleta lógica, você pode definir cores de pixel para a GDI usando o RGBA ou o modo de índice de cores. O tamanho máximo de uma paleta lógica é de 256 cores para dispositivos de 8 bits e 4.096 cores em um dispositivo de cor verdadeira (16, 24 e 32 bits).

Para obter mais informações sobre os modos RGBA e color-index, consulte [Modo RGBA](rgba-mode-and-windows-palette-management.md) e gerenciamento de paletas Windows e Modos de cores [openGL](opengl-color-modes-and-windows-palette-management.md)e gerenciamento de paleta Windows .

 

 




