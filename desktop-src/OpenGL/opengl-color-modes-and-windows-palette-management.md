---
title: Modos de cor OpenGL e gerenciamento de paleta do Windows
description: A implementação da Microsoft do OpenGL no Windows dá suporte a dois modos de dados de pixel de cores RGBA e de índice de cor. O Windows fornece duas maneiras análogas de lidar com cores true color e gerenciamento de paleta.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL no Windows, modos de cor
- OpenGL no Windows, gerenciamento de paleta
- gerenciamento de paleta OpenGL
- modos de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292063"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modos de cor OpenGL e gerenciamento de paleta do Windows

A implementação da Microsoft do OpenGL no Windows dá suporte a dois modos de dados de pixel colorido: os modos RGBA e de índice de cor. O Windows fornece duas maneiras análogas de lidar com cores: verdadeiro e gerenciamento de paleta.

Os dispositivos true-color, capazes de aceitar 16, 24 ou mais informações de cores por pixel, podem exibir dezenas de milhares, dezenas de milhões ou mais cores simultaneamente. No entanto, as complexidades surgem quando um aplicativo tem que gerenciar RGBA ou o modo de índice de cor em um dispositivo de tipo de paleta. Os dispositivos de tipo de paleta, como uma exibição VGA de cor de 256, são limitados no número de cores que eles podem exibir simultaneamente. Os aplicativos devem lidar com vários detalhes complicados para usar com êxito os dispositivos de tipo de paleta. Como os programas de modo de índice de cor não usam uma paleta de hardware, eles são mais difíceis de usar com dispositivos de cor verdadeira do que programas usando o modo RGBA.

 

 




