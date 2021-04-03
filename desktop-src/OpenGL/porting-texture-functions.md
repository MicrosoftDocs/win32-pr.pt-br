---
title: Portando funções de textura
description: Portando funções de textura
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Portabilidade do íris GL, textura
- portando do íris GL, textura
- portando para OpenGL do íris GL, textura
- Portabilidade OpenGL do íris GL, textura
- textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2cba8b105089553084a93f997517d19cf371e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005744"
---
# <a name="porting-texture-functions"></a>Portando funções de textura

Ao portar funções de textura do íris GL para OpenGL, tenha em mente os seguintes pontos:

-   O OpenGL não mantém tabelas de texturas; Ele usa textura de 1-D e somente textura de 2D. Para reutilizar as texturas do código da íris GL, coloque-as em uma lista de exibição.
-   O OpenGL não gera mipmaps automaticamente. Se você estiver usando mipmaps, deverá primeiro chamar a função [**gluBuild2DMipmaps**](glubuild2dmipmaps.md) .
-   No OpenGL, você usa [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) para ativar e desativar os recursos de texturing.
-   No OpenGL, o tamanho da textura é mais estritamente regulamentado do que no íris GL. O tamanho de uma textura OpenGL deve ser:

    2 *n* + 2 *b*

    onde *n* é um inteiro e *b* é:

    -   0, se a textura não tiver borda
    -   1, se a textura tiver um pixel de borda (texturas OpenGL podem ter bordas de 1 pixel).

A tabela a seguir lista as funções de textura do íris GL e seus equivalentes em OpenGL gerais.



| Função GL de íris | Função OpenGL                                                                                                                                                                                                                                                       | Significado                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Especifica uma imagem de textura 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Seleciona uma função de textura.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Define um ambiente de mapeamento de textura.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Seleciona um ambiente de textura.                                                              |
| **T2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Define as coordenadas de textura atuais.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Controla a geração de coordenadas de textura. Dimensiona uma imagem para um tamanho arbitrário.<br/> |



 

Para obter mais informações sobre o texturing, consulte o *Guia de programação OpenGL*.

Este tópico inclui informações sobre o seguinte.

-   [Convertendo tevdef](translating-tevdef.md)
-   [Convertendo texdef](translating-texdef.md)
-   [Convertendo texgen](translating-texgen.md)

 

 





