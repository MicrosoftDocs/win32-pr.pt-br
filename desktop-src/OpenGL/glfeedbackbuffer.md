---
title: função glFeedbackBuffer (GL. h)
description: A função glFeedbackBuffer controla o modo de comentários.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- função glFeedbackBuffer OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751092"
---
# <a name="glfeedbackbuffer-function"></a>função glFeedbackBuffer

A função **glFeedbackBuffer** controla o modo de comentários.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*size* 
</dt> <dd>

O número máximo de valores que podem ser gravados no *buffer*.

</dd> <dt>

*tipo* 
</dt> <dd>

Uma constante simbólica que descreve as informações que serão retornadas para cada vértice. As seguintes constantes simbólicas são aceitas: GL \_ 2D, GL \_ 3D, Recall \_ 3D \_ Color, GL \_ 3D Color \_ \_ Texture e GL \_ 4D \_ Color \_ Texture.

</dd> <dt>

*completo* 
</dt> <dd>

Retorna os dados de comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* não era um valor aceito.<br/>                                                                                                                                                                           |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tamanho* era negativo.<br/>                                                                                                                                                                                        |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | **glFeedbackBuffer** foi chamado enquanto o modo render tinha \_ comentários GL ou [**glRenderMode**](glrendermode.md) foi chamado com comentários Argument GL \_ antes de **glFeedbackBuffer** ser chamado pelo menos uma vez.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                                                                  |



## <a name="remarks"></a>Comentários

A função **glFeedbackBuffer** controla os comentários. Comentários, como seleção, é um modo OpenGL. O modo é selecionado chamando [**glRenderMode**](glrendermode.md) com os \_ comentários GL. Quando OpenGL está no modo de comentários, nenhum pixel é produzido pela rasterização. Em vez disso, as informações sobre primitivas que teriam sido rasterizadas são voltadas para o aplicativo usando OpenGL.

A função **glFeedbackBuffer** tem três argumentos:

-   *buffer* é um ponteiro para uma matriz de valores de ponto flutuante em que as informações de comentários são colocadas.
-   *tamanho* indica o tamanho da matriz.
-   *Type* é uma constante simbólica que descreve as informações que são voltadas para cada vértice.

Você deve emitir **glFeedbackBuffer** antes que o modo de comentários esteja habilitado (chamando **glRenderMode** com comentários do Argument GL \_ ). Definir \_ comentários GL sem estabelecer o buffer de comentários ou chamar **GlFeedbackBuffer** enquanto OpenGL está no modo de comentários, é um erro.

Retire o OpenGL do modo de comentários chamando [**glRenderMode**](glrendermode.md) com um valor de parâmetro diferente do GL \_ . Quando você faz isso enquanto OpenGL está no modo de comentários, **glRenderMode** retorna o número de entradas colocadas na matriz de comentários. O valor retornado nunca excede o *tamanho*. Se os dados de comentários precisarem de mais espaço que o disponível no *buffer*, **glRenderMode** retornará um valor negativo.

No modo de comentários, cada primitivo que seria rasterizado gera um bloco de valores que são copiados para a matriz de comentários. Se isso fizer com que o número de entradas exceda o máximo, o **glFeedbackBuffer** gravará parcialmente o bloco para preencher a matriz (se houver alguma sala restante) e definir um sinalizador de estouro. Cada bloco começa com um código que indica o tipo primitivo, seguido por valores que descrevem os vértices e os dados associados do primitivo. A função **glFeedbackBuffer** também grava entradas para bitmaps e retângulos de pixel. Os comentários ocorrem após a remoção do polígono e a interpretação [**glPolygonMode**](glpolygonmode.md) dos polígonos, portanto, os polígonos que são retirados não são retornados no buffer de comentários. Isso também pode ocorrer depois que polígonos com mais de três bordas são divididos em triângulos, se a implementação do OpenGL renderiza polígonos executando essa decomposição.

Você pode inserir um marcador no buffer de comentários com [**glPassThrough**](glpassthrough.md).

Veja a seguir a gramática para os blocos de valores gravados no buffer de comentários. Cada primitiva é indicada com um valor de identificação exclusivo seguido por algum número de vértices. As entradas de polígono incluem um valor inteiro indicando quantos vértices seguem. Um vértice é devolvido como um número de valores de ponto flutuante, conforme determinado pelo *tipo*. As cores são realimentadas como quatro valores no modo RGBA e um valor no modo de índice de cor.

feedbacklist < feedbackItem feedbacklist \| feedbackItem

feedbackItem < ponto \| lineSegment \| Polygon \| bitmap \| pixelRectangle \| PassThru

\_vértice do token de ponto do < GL \_

vértice do vértice do \_ token de linha do lineSegment < GL \_ \| \_ \_ \_

símbolo de polígono < GL do polígono \_ \_ n da polispec

polispec < vértice de vértice do vértice de vértice do polispec \|

\_vértice do token de bitmap do bitmap < GL \_

vértice do \_ \_ \_ token \| \_ \_ \_ pixel do pixelRectangle < GL

passThru < GL \_ o \_ valor do token de passagem \_

vértice < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture

valor de valor de < 2D

valor do valor do valor de < 3D

cor do valor do valor de < de valor de 3dColor

3dColorTexture < valor Value valor Color Tex

4dColorTexture < valor valor valor da cor Tex

índice de < de cores RGBA \|

RGBA < valor do valor do valor do valor

valor de < de índice

valor do valor do valor de < de valor de Tex

O parâmetro *Value* é um número de ponto flutuante, e *n* é um inteiro de ponto flutuante fornecendo o número de vértices no polígono. Veja a seguir constantes de ponto flutuante simbólico: \_ token de ponto GL \_ , \_ \_ token de linha gl, token de \_ redefinição de linha GL, token de \_ \_ \_ polígono GL \_ , \_ \_ token de bitmap GL, token \_ \_ de pixel de desenho GL \_ , token de pixel de \_ cópia GL e o \_ \_ \_ token de passagem GL \_ \_ . \_ \_ \_ O token de redefinição de linha GL é retornado sempre que o padrão de Stipple de linha é redefinido. Os dados retornados como um vértice dependem do *tipo* de comentário.

A tabela a seguir fornece a correspondência entre o *tipo* e o número de valores por vértice; *k* é 1 no modo de índice de cor e 4 no modo RGBA.



| Tipo                   | Coordenadas        | Cor | Textura | Número total de valores |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| Cor do GL \_ 3D \_          | *x*, *y*, *z*      | *c*   |         | 3 + *k*                |
| \_Textura de \_ cores \_ 3D GL | *x*, *y*, *z*,     | *c*   | 4       | 7 + *k*                |
| \_Textura de \_ cores GL 4D \_ | *x*, *y*, *z*, *w* | *c*   | 4       | 8 + *k*                |



 

As coordenadas de vértice de comentários estão em coordenadas de janela, exceto *w*, que está em coordenadas de clipe. As cores de comentários serão iluminadas se a iluminação estiver habilitada. As coordenadas de textura de comentários serão geradas se a geração de coordenadas de textura estiver habilitada. Eles são sempre transformados pela matriz de textura.

A função **glFeedbackBuffer** , quando usada em uma lista de exibição, não é compilada na lista de exibição, mas sim executada imediatamente.

A função a seguir recupera informações relacionadas a **glFeedbackBuffer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





