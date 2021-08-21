---
title: Portando funções de matriz e transformação
description: IRIS GL e OpenGL lidam com matrizes e transformações de maneira semelhante.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Portação IRIS GL, matrizes
- portando de IRIS GL, matrizes
- portando para OpenGL de IRIS GL, matrizes
- Portação openGL de IRIS GL, matrizes
- matrizes
- Portação IRIS GL, transformações
- portating from IRIS GL,transformations
- portando para OpenGL do IRIS GL, transformações
- Portação openGL de IRIS GL, transformações
- transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e2dc0ed6b53f3a2ee5ef5310369b734a58cba27481b8b478eef63fdfe5722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132598"
---
# <a name="porting-matrix-and-transformation-functions"></a>Portando funções de matriz e transformação

IRIS GL e OpenGL lidam com matrizes e transformações de maneira semelhante. Mas há várias diferenças a ter em mente ao portar código do IRIS GL:

-   No OpenGL, você está sempre no modo de matriz dupla; não há nenhum modo de matriz única.
-   Ângulos são medidos em graus, em vez de décimos de graus.
-   Chamadas de matriz de projeção, como [**glFrustum**](glfrustum.md) e [**glOrtho,**](glortho.md)agora se multiplicam para a matriz atual, em vez de serem carregadas na matriz atual.
-   A função OpenGL, [**glRotate,**](glrotate.md)é muito diferente da **rotação**. Você pode girar em torno de qualquer eixo arbitrário, em vez de ser restrito aos eixos x, y e z. Por exemplo, você pode traduzir:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    para:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Ao traduzir de **girar** para **glRotate,** você alterna para graus de décimos de graus e substitui 'z' por um vetor para o eixo z.

-   O OpenGL não tem equivalente à **função polarview.** Você pode substituí-lo facilmente por uma tradução e três rotações. Por exemplo, você pode traduzir:

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    para:

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

A tabela a seguir lista as funções de matriz OpenGL e suas funções IRIS GL equivalentes.



| Função IRIS GL              | Função OpenGL                                                                        | Significado                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Define o modo de matriz atual.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Substitui a matriz atual pela matriz de identidade.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Substitui a matriz atual pela matriz especificada.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Pós-multiplica a matriz atual com a matriz especificada (observe que **multmatrix** pré-multiplicado).                                                                            |
| **mapw**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Projeta coordenadas de espaço do mundo para o espaço do objeto (consulte [**também gluProject**](gluproject.md)).                                                                                  |
| **Ortho**                     | [**glOrtho**](glortho.md)                                                             | Multiplica a matriz atual por uma matriz de projeção ortográfica.                                                                                                                |
| **orto2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Define uma matriz de projeção ortográfica bidimensional.                                                                                                                      |
| **Perspectiva**               | [**gluPerspective**](gluperspective.md)                                               | Define uma matriz de projeção de perspectiva.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Define uma região de escolha.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | A pilha de matriz atual é pop-pop, substituindo a matriz atual pela que está abaixo dela.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Esvaia a pilha de matriz atual em um, duplicando a matriz atual.                                                                                                       |
| **girar**,**pod**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Gira o sistema de coordenadas atual pelo ângulo determinado sobre o vetor da origem até o ponto determinado. Observe que **a rotação** girada apenas sobre os eixos x, y e z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Multiplica a matriz atual por uma matriz de dimensionamento.                                                                                                                                 |
| **Traduzir**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Move a origem do sistema de coordenadas para o ponto especificado multiplicando a matriz atual por uma matriz de tradução.                                                              |
| **Janela**                    | [**glFrustum**](glfrustum.md)                                                         | Determinadas coordenadas para planos de recorte, multiplica a matriz atual por uma matriz de perspectiva.                                                                                  |



 

O OpenGL tem três modos de matriz, que são definidos com [**glMatrixMode.**](glmatrixmode.md) A tabela a seguir lista os modos disponíveis como parâmetros para **glMatrixMode.**



| Modo de matriz IRIS GL | Modo OpenGL    | Significado                                  | Profundidade mínima da pilha |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | TEXTURA \_ GL    | Opera na pilha de matriz de textura.    | 2               |
| **MVIEWING**        | GL \_ MODELVIEW  | Opera na pilha de matriz de exibição de modelo. | 32              |
| **MPROJECTION**     | PROJEÇÃO GL \_ | Opera na pilha de matriz de projeção. | 2               |



 

 

 





