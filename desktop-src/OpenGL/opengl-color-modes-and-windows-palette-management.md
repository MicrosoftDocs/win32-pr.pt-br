---
title: modos de cor OpenGL e gerenciamento de paleta de Windows
description: a implementação da Microsoft do OpenGL no Windows dá suporte a dois modos de dados de pixel de cores RGBA e de índice de cor. Windows fornecem duas maneiras análogas de lidar com a cor verdadeira da cor e o gerenciamento da paleta.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL em Windows, modos de cor
- OpenGL no Windows, gerenciamento de paleta
- gerenciamento de paleta OpenGL
- modos de cor OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf91ebb45e99368596cb48cb625f0eb6de025e6664144f104f6a9c17951a1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144129"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>modos de cor OpenGL e gerenciamento de paleta de Windows

a implementação da Microsoft do OpenGL no Windows dá suporte a dois modos de dados de pixel colorido: os modos RGBA e de índice de cor. Windows fornecem duas maneiras análogas de lidar com cores: verdadeiro e gerenciamento de paleta.

Os dispositivos true-color, capazes de aceitar 16, 24 ou mais informações de cores por pixel, podem exibir dezenas de milhares, dezenas de milhões ou mais cores simultaneamente. No entanto, as complexidades surgem quando um aplicativo tem que gerenciar RGBA ou o modo de índice de cor em um dispositivo de tipo de paleta. Os dispositivos de tipo de paleta, como uma exibição VGA de cor de 256, são limitados no número de cores que eles podem exibir simultaneamente. Os aplicativos devem lidar com vários detalhes complicados para usar com êxito os dispositivos de tipo de paleta. Como os programas de modo de índice de cor não usam uma paleta de hardware, eles são mais difíceis de usar com dispositivos de cor verdadeira do que programas usando o modo RGBA.

 

 




