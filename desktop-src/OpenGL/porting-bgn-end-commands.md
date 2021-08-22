---
title: Portando comandos BGN/end
description: A íris GL usa o paradigma de início/término, mas tem uma função diferente para cada primitivo de elementos gráficos.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Portabilidade do íris GL, comandos BGN/end
- portando dos comandos íris GL, BGN/end
- portando para OpenGL dos comandos íris GL, BGN/end
- Portabilidade do OpenGL dos comandos íris GL, BGN/end
- funções de desenho, comandos BGN/end
- comandos BGN/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63084b1f05d984fdc19254edaadaca9098d13f974a433f5c6ff7c5d370ec223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485966"
---
# <a name="porting-bgnend-commands"></a>Portando comandos BGN/end

A íris GL usa o paradigma de início/término, mas tem uma função diferente para cada primitivo de elementos gráficos. Por exemplo, você provavelmente usará **bgnpolygon** e **endpolygon** para desenhar polígonos e **bgnline** e **EndLine** para desenhar linhas. No OpenGL, você usa a estrutura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) para ambos. No OpenGL, você desenha a maioria dos objetos geométricos delimitando uma série de funções que especificam vértices, normais, texturas e cores entre pares de chamadas **glBegin** e **glEnd** . Por exemplo:

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

A função **glBegin** usa um único parâmetro que especifica o modo de desenho e, portanto, o primitivo. Aqui está um exemplo de código OpenGL que desenha um polígono e uma linha:

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

Com o OpenGL, você desenha diferentes objetos geométricos especificando parâmetros diferentes para [**glBegin**](glbegin.md). A tabela a seguir lista os parâmetros OpenGL **glBegin** que correspondem às funções do íris GL equivalentes.



| Função GL de íris  | Valor do modo glBegin | Significado                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| **bgnpoint**      | \_pontos GL            | Pontos individuais.                                                                       |
| **bgnline**       | \_faixa de linha gl \_       | Série de segmentos de linha conectados.                                                       |
| **bgnclosedline** | \_loop de linha gl \_        | Série de segmentos de linha conectados, com um segmento adicionado entre o primeiro e o último vértice. |
|                   | \_linhas GL             | Pares de vértices interpretados como segmentos de linha individuais.                               |
| **bgnpolygon**    | polígono do GL \_           | Limite de um polígono convexa simples.                                                     |
|                   | \_TRIângulos GL         | As corridas de vértices interpretadas como triângulos.                                            |
| **bgntmesh**      | \_faixa de triângulo GL \_   | Faixas vinculadas de triângulos.                                                              |
|                   | \_ \_ ventilador do triângulo GL     | Ventiladores vinculados de triângulos.                                                                |
|                   | GL \_ quádruplos             | Quádruplos de vértices interpretados como quadrilaterals.                                    |
| **bgnqstrip**     | extensão do GL \_ Quad \_       | Faixas vinculadas de quadrilaterals.                                                         |



 

Para obter uma discussão detalhada das diferenças entre malhas de triângulo, faixas e ventiladores, confira [triângulos de portabilidade](porting-triangles.md).

Não há nenhum limite para o número de vértices que você pode especificar entre um par [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) .

Além de especificar vértices dentro de um par **glBegin**  /  **glEnd** , você pode especificar uma atual coordenadas atuais, atuais e uma cor atual. A tabela a seguir lista os comandos válidos dentro de um par **glBegin**  /  **glEnd** .



| Função GL de íris        | Função OpenGL                                                      | Significado                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **v2**, **v3**, **v4**  | [glVertex](glvertex-functions.md)                                   | Define as coordenadas do vértice.                         |
| **RGBcolor**, **cpack** | [glColor](glcolor-functions.md)                                     | Define a cor atual.                              |
| **color**               | [glIndex](glindex-functions.md)                                     | Define o índice de cores atual.                        |
| **n3f**                 | [glNormal](glnormal-functions.md)                                   | Define coordenadas de vetor normais.                  |
|                         | [glEvalCoord](glevalcoord-functions.md)                             | Avalia os mapas único e bidimensionais habilitados. |
| **callobj**             | [**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md) | Executa lista (s) de exibição.                        |
| **T2**                  | [glTexCoord](gltexcoord-functions.md)                               | Define coordenadas de textura.                        |
|                         | [glEdgeFlag](gledgeflag-functions.md)                               | Controla bordas de desenho.                          |
| **lmbind**              | [glMaterial](glmaterial-functions.md)                               | Define as propriedades do material.                        |



 

> [!Note]
>
> Se você usar qualquer função OpenGL diferente daquelas listadas na tabela anterior dentro de um par [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) , você obterá resultados imprevisíveis ou possivelmente um erro.

 

 

 




