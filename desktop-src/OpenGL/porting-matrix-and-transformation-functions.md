---
title: Portando funções de matriz e transformação
description: A íris GL e o OpenGL lidam com as matrizes e as transformações de maneira semelhante.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Portabilidade do íris GL, matrizes
- portando do íris GL, matrizes
- portando para OpenGL do íris GL, matrizes
- Portabilidade OpenGL do íris GL, matrizes
- matrizes
- Portabilidade do íris GL, transformações
- portando do íris GL, transformações
- portando para OpenGL do íris GL, transformações
- Portabilidade do OpenGL do íris GL, transformações
- transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292443"
---
# <a name="porting-matrix-and-transformation-functions"></a>Portando funções de matriz e transformação

A íris GL e o OpenGL lidam com as matrizes e as transformações de maneira semelhante. Mas há várias diferenças a serem consideradas ao portar o código do íris GL:

-   No OpenGL, você está sempre no modo de matriz dupla; Não há um modo de matriz única.
-   Os ângulos são medidos em graus, em vez de décimos de graus.
-   As chamadas de matriz de projeção, como [**glFrustum**](glfrustum.md) e [**glOrtho**](glortho.md), agora são multiplicadas na matriz atual, em vez de serem carregadas na matriz atual.
-   A função OpenGL, [**glRotate**](glrotate.md), é muito diferente da **rotação**. Você pode girar em qualquer eixo arbitrário, em vez de ser confinado nos eixos x, y e z. Por exemplo, você pode traduzir:

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    para:

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    Ao converter de **Rotate** para **glRotate** , você muda para graus de décimos de graus e substitui ' z ' por um vetor para o eixo z.

-   O OpenGL não tem equivalente à função **polarview** . Você pode substituí-lo facilmente por uma tradução e três rotações. Por exemplo, você pode traduzir:

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

    

A tabela a seguir lista as funções de matriz OpenGL e suas funções de íris GL equivalentes.



| Função GL de íris              | Função OpenGL                                                                        | Significado                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **mmode**                     | [**glMatrixMode**](glmatrixmode.md)                                                   | Define o modo de matriz atual.                                                                                                                                                      |
|                               | [**glLoadIdentity**](glloadidentity.md)                                               | Substitui a matriz atual pela matriz de identidade.                                                                                                                              |
| **loadmatrix**                | [**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)<br/> | Substitui a matriz atual pela matriz especificada.                                                                                                                             |
| **multmatrix**                | [**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)<br/> | Pós-multiplica a matriz atual pela matriz especificada (Observe que **multmatrix** pré-multiplicado).                                                                            |
| **mapw**, **mapw2**           | [**gluUnProject**](gluunproject.md)                                                   | Projetos coordenadas de espaço do mundo para espaço de objeto (consulte também [**gluProject**](gluproject.md)).                                                                                  |
| **ortho**                     | [**glOrtho**](glortho.md)                                                             | Multiplica a matriz atual por uma matriz de projeção ortográfica.                                                                                                                |
| **ortho2**                    | [**gluOrtho2D**](gluortho2d.md)                                                       | Define uma matriz de projeção ortográfica bidimensional.                                                                                                                      |
| **perspectiva**               | [**gluPerspective**](gluperspective.md)                                               | Define uma matriz de projeção em perspectiva.                                                                                                                                       |
| **picksize**                  | [**gluPickMatrix**](glupickmatrix.md)                                                 | Define uma região de separação.                                                                                                                                                      |
| **popmatrix**                 | [**glPopMatrix**](glpopmatrix.md)                                                     | Exibe a pilha de matriz atual, substituindo a matriz atual pela outra abaixo dela.                                                                                                 |
| **pushmatrix**                | [**glPushMatrix**](glpushmatrix.md)                                                   | Envia por push a pilha da matriz atual por uma, duplicando a matriz atual.                                                                                                       |
| **girar**,**corrompidos**<br/> | [**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)<br/>                 | Gira o sistema de coordenadas atual pelo ângulo fornecido sobre o vetor da origem por meio de um determinado ponto. Observe que **girar** girado apenas sobre os eixos x-, y-e z. |
| **scale**                     | [**glScaled**](glscale.md),[**glScalef**](glscale.md)<br/>                     | Multiplica a matriz atual por uma matriz de dimensionamento.                                                                                                                                 |
| **Traduzir**                 | [**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)<br/>     | Move a origem do sistema de coordenadas para o ponto especificado, multiplicando a matriz atual por uma matriz de conversão.                                                              |
| **Window**                    | [**glFrustum**](glfrustum.md)                                                         | As coordenadas fornecidas para os planos de recorte, multiplicam a matriz atual por uma matriz de perspectiva.                                                                                  |



 

O OpenGL tem três modos de matriz, que são definidos com [**glMatrixMode**](glmatrixmode.md). A tabela a seguir lista os modos disponíveis como parâmetros para **glMatrixMode**.



| Modo de matriz do íris GL | Modo OpenGL    | Significado                                  | Profundidade mínima da pilha |
|---------------------|----------------|------------------------------------------|-----------------|
| **MTEXTURE**        | \_textura GL    | Opera na pilha da matriz de textura.    | 2               |
| **MVIEWING**        | \_MODELVIEW GL  | Opera na pilha de matrizes de exibição de modelo. | 32              |
| **MPROJECTION**     | \_projeção GL | Opera na pilha matriz de projeção. | 2               |



 

 

 





