---
title: Portando operações de pixel
description: Portando operações de pixel
ms.assetid: 57917f33-daf5-4db6-9583-ab596deab91a
keywords:
- Portabilidade do íris GL, pixels
- portando do íris GL, pixels
- portando para OpenGL do íris GL, pixels
- Portabilidade do OpenGL do íris GL, pixels
- pixels, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fd484efa031bd12af59cb729c8fa20b68fe88e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636571"
---
# <a name="porting-pixel-operations"></a>Portando operações de pixel

Ao portar o código que envolve operações de pixel, tenha em mente os seguintes pontos:

-   As operações de pixel lógico não são aplicadas a buffers de cores RGBA. Para obter mais informações, consulte [**glLogicOp**](gllogicop.md).
-   Em geral, a íris GL usa o formato ABGR para pixels, enquanto OpenGL usa RGBA. Você pode alterar o formato com [**glPixelStore**](glpixelstore-functions.md).
-   Ao portar funções do **lrectwrite** , tenha cuidado para observar onde o **lrectwrite** está gravando (por exemplo, ele pode estar gravando no buffer de profundidade).

O OpenGL oferece mais flexibilidade em operações de pixel. A tabela a seguir lista as funções do íris GL para operações de pixel e suas funções OpenGL equivalentes.



| Função GL de íris                                   | Função OpenGL                                                                           | Significado                                                                 |
|----------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| **lrectread**, **rectread**,**readRGB**<br/> | [**glReadPixels**](glreadpixels.md)                                                      | Lê um bloco de pixels do framebuffer.                           |
| **lrectwrite**, **rectwrite**                      | [**glDrawPixels**](gldrawpixels.md)                                                      | Grava um bloco de pixels no framebuffer.                            |
| **rectcopy**                                       | [**glCopyPixels**](glcopypixels.md)                                                      | Copia os pixels no framebuffer.                                       |
| **rectzoom**                                       | [**glPixelZoom**](glpixelzoom.md)                                                        | Especifica fatores de zoom de pixel para **glDrawPixels** e **glCopyPixels**. |
| **cmov**                                           | [glRasterPos](glrasterpos-functions.md)                                                  | Especifica a posição da varredura para as operações de pixel.                         |
| **leitura**                                     | [**glReadBuffer**](glreadbuffer.md)                                                      | Seleciona uma fonte de buffer de cores para pixels.                               |
| **pixmode**                                        | [**glPixelStore**](glpixelstore-functions.md),[**glPixelTransfer**](glpixeltransfer.md) | Define os modos de armazenamento em pixels. Definir modos de transferência de pixel.                      |
| **logicop**                                        | [**glLogicOp**](gllogicop.md)                                                            | Especifica uma operação lógica para gravações de pixel.                         |
|                                                    | [**glEnable**](glenable.md) ( \_ op lógico GL \_ )                                            | Ativa operações lógicas de pixel.                                        |



 

Para obter uma lista completa de possíveis operações lógicas, consulte [**glLogicOp**](gllogicop.md).

Este exemplo de código do íris GL mostra uma gravação de pixel típica:

``` syntax
unsigned long *packedRaster; 
.. 
packedRaster[k] = 0x00000000; 
.. 
lrectwrite(0, 0, xSize, ySize, packedRaster);
```

O código anterior tem esta aparência quando traduzido para OpenGL:

``` syntax
glRasterPos2i( 0, 0); 
glDrawPixels( xSize + 1, ySize + 1, GL_RGBA, GL_UNSIGNED_BYTE, packedRaster);
```

 

 





