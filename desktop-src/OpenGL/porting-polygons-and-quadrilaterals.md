---
title: Como portar polígonos e Quadrilaterals
description: Tenha os seguintes pontos em mente ao portar polígonos e quadrilaterals
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Portabilidade do íris GL, quadrilaterals
- portando do íris GL, quadrilaterals
- portando para OpenGL do íris GL, quadrilaterals
- Portabilidade OpenGL do íris GL, quadrilaterals
- funções de desenho, quadrilaterals
- quadrilaterals
- Portabilidade do íris GL, polígonos
- portando do íris GL, polígonos
- portando para OpenGL do íris GL, polígonos
- Portabilidade OpenGL do íris GL, polígonos
- funções de desenho, polígonos
- polígonos, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636569"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Como portar polígonos e Quadrilaterals

Tenha os seguintes pontos em mente ao portar polígonos e quadrilaterals:

-   Não há equivalente direto para **côncavo**(**true**). Em vez disso, você pode usar as rotinas de mosaico na GLU, descritas em [polígonos do inclusão](tessellating-polygons.md).
-   Os modos de polígono são definidos de forma diferente.
-   Essas funções de desenho de polígono não têm equivalentes diretos em OpenGL: The **Polyline** Family of rotinas; a família de rotinas **polf** ; **PMV**, **Laos** e **PCLOS**; **rpmv** e **rpdr**; **splf**; e **spclos**.

Se o código do íris GL usar essas funções, você terá que reescrever o código usando [**glBegin**](glbegin.md)(polígono do GL \_ ).

A tabela a seguir lista as funções de desenho de polígono do íris GL e suas funções OpenGL equivalentes.



| Função GL de íris         | Função OpenGL                                                    | Significado                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) (polígono do GL \_ )[**glEnd**](glend.md)   | Os vértices definem o limite de um polígono convexa simples.    |
|                          | **glBegin**(GL \_ quádruplos)**glEnd**<br/>                       | Interpreta os quádruplos de vértices como quadrilaterals.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) (GL \_ Quad \_ strip)**glEnd**<br/> | Interpreta vértices como faixas vinculadas de quadrilaterals. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **polimodo**             | [**glPolygonMode**](glpolygonmode.md)                             | Define o modo de desenho do polígono.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Desenha um retângulo.                                      |
| **sboxsboxf**<br/> |                                                                    | Desenha um retângulo alinhado à tela.                       |



 

??

## <a name="porting-polygon-modes"></a>Modos de polígono de portabilidade

A função OpenGL [**glPolygonMode**](glpolygonmode.md) permite especificar qual lado de um polígono (na parte posterior ou frontal) ao qual o modo se aplica. Sua sintaxe é:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

onde a face é uma de:



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| frente do GL \_            | modo que se aplica a polígonos front-face                |
| GL \_ regressivo             | modo que se aplica a polígonos traseiros                 |
| GL \_ frontal \_ e \_ posterior | modo que se aplica a polígonos frente e verso |



 

O \_ modo de frente e de trás do GL \_ \_ é equivalente à função de **polimodo** do íris GL. A tabela a seguir lista os modos de polígono do íris GL e seus modos OpenGL equivalentes.



| Modo GL de íris | Modo OpenGL | Significado                                       |
|--------------|-------------|-----------------------------------------------|
| ponto de PYM \_   | \_ponto GL   | Desenha vértices como pontos.                     |
| PYM \_ linha    | \_linha GL    | Desenha bordas de limite como segmentos de linha.        |
| preenchimento de PYM \_    | preenchimento do GL \_    | Desenha o interior do polígono cheio.                |
| PYM \_ vazado  |             | Preenche somente os pixels interiores nos limites. |



 

## <a name="porting-polygon-stipples"></a>Stipples polígono de porta

Ao portar stipples Polygon do íris GL, tenha os seguintes pontos em mente:

-   O OpenGL não usa tabelas para polígono stipples; apenas um padrão Stipple é mantido. Você pode usar listas de exibição para armazenar diferentes padrões de Stipple.
-   O tamanho do bitmap Stipple do polígono do OpenGL é sempre um padrão de 32 bits.
-   A codificação Stipple é afetada por [**glPixelStore**](glpixelstore-functions.md).

Para obter mais informações sobre como portar stipples Polygon, consulte [portando operações de pixel](porting-pixel-operations.md).

A tabela a seguir lista as funções Stipple de polígono do íris GL e suas funções OpenGL equivalentes.



| Função GL de íris | Função OpenGL                                    | Significado                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Define o padrão Stipple.                             |
| **setpattern**   |                                                    | O OpenGL mantém apenas um padrão Stipple de polígono.        |
| **GetPattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Retorna o bitmap Stipple (usado para retornar um índice). |



 

No OpenGL, você habilita e desabilita o polígono stippling ao passar \_ \_ o Polygon do GL STIPPLE como um parâmetro para [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).

O exemplo de código OpenGL a seguir demonstra o polígono stippling:


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a>Portando polígonos mosaico

No íris GL, você usa o **côncavo**(**true**) e, em seguida, **bgnpolygon** para desenhar polígonos côncavos. O OpenGL GLU inclui funções que você pode usar para desenhar polígonos côncavos.

**Para desenhar um polígono côncavo com OpenGL**

1.  Crie um objeto de mosaico.
2.  Defina retornos de chamada que serão usados para processar os triângulos gerados pelo Tessellator.
3.  Especifique o polígono côncavo a ser mosaico.

A tabela a seguir lista as funções OpenGL para desenhar polígonos mosaico.



| Função OpenGL GLU                        | Significado                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Cria um novo objeto de mosaico.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Exclui um objeto de mosaico.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Inicia a especificação do polígono.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Especifica um vértice de polígono em uma delimitação.                           |
| [**gluNextContour**](glunextcontour.md)   | Indica que a próxima série de vértices descreve uma nova delimitação. |
| [**gluEndPolygon**](gluendpolygon.md)     | Encerra a especificação do polígono.                                    |



 

 

 





