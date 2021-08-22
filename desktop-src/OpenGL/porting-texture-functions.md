---
title: Portando funções de textura
description: Portando funções de textura
ms.assetid: 03e0b0fc-3812-4744-a0f1-3dcb466d679d
keywords:
- Portação IRIS GL, textura
- portando de IRIS GL, textura
- portando para OpenGL de IRIS GL, textura
- Portação openGL de IRIS GL, textura
- textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17cd79aaf8e7e5b90d0f171ddcec4b49b6d15b3615ccc1f5e44a04b3e16fae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339236"
---
# <a name="porting-texture-functions"></a>Portando funções de textura

Ao portar funções de textura IRIS GL para OpenGL, lembre-se dos seguintes pontos:

-   O OpenGL não mantém tabelas de texturas; ele usa apenas textura 1D e textura 2D. Para reutilizar as texturas do código IRIS GL, coloque-as em uma lista de exibição.
-   O OpenGL não gera mipmaps automaticamente. Se você estiver usando mipmaps, primeiro chame [**a função gluBuild2DMipmaps.**](glubuild2dmipmaps.md)
-   No OpenGL, você usa [**glEnable e**](glenable.md) [**glDisable**](gldisable.md) para ativar e desativar recursos de texto.
-   No OpenGL, o tamanho da textura é mais estritamente regulamentado do que no IRIS GL. O tamanho de uma textura OpenGL deve ser:

    2 *n* + 2 *b*

    em *que n* é um inteiro e *b* é:

    -   0, se a textura não tiver borda
    -   1, se a textura tiver um pixel de borda (texturas OpenGL podem ter bordas de 1 pixel.)

A tabela a seguir lista as funções de textura IRIS GL e seus equivalentes gerais do OpenGL.



| Função IRIS GL | Função OpenGL                                                                                                                                                                                                                                                       | Significado                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **textdef2d**    | [**glTexImage2D**](glteximage2d.md)[**glTexParameter**](gltexparameter-functions.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/>                                                                                                           | Especifica uma imagem de textura 2D.                                                              |
| **textbind**     | **glTexImage2DglTexParameter**<br/> **gluBuild2DMipmaps**<br/>                                                                                                                                                                                            | Seleciona uma função de textura.                                                                 |
| **tevdef**       | [**glTexEnv**](gltexenv-functions.md)                                                                                                                                                                                                                                | Define um ambiente de mapeamento de textura.                                                      |
| **tevbind**      | **glTexEnv**[**glTexImage1D**](glteximage1d.md)<br/>                                                                                                                                                                                                           | Seleciona um ambiente de textura.                                                              |
| **t2**           | [**glTexCoord**](gltexcoord-functions.md)                                                                                                                                                                                                                            | Define as coordenadas de textura atuais.                                                       |
| **texgen**       | [**glTexGen**](gltexgen-functions.md)[**glGetTexParameter**](glgettexparameter.md)<br/> [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)<br/> [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)<br/> [**gluScaleImage**](gluscaleimage.md)<br/> | Controla a geração de coordenadas de textura. Dimensiona uma imagem para um tamanho arbitrário.<br/> |



 

Para obter mais informações sobre a texturing, consulte o Guia *de Programação OpenGL*.

Este tópico inclui informações sobre o seguinte.

-   [Traduzindo tevdef](translating-tevdef.md)
-   [Traduzindo o texdef](translating-texdef.md)
-   [Traduzindo o texgen](translating-texgen.md)

 

 





