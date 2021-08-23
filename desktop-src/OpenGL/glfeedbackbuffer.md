---
title: Função glFeedbackBuffer (Gl.h)
description: A função glFeedbackBuffer controla o modo de comentários.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- Função glFeedbackBuffer OpenGL
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
ms.openlocfilehash: 76e51a08dac2bbf55509d4964218fc4b844581c797220294464b84c05de5e05b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580196"
---
# <a name="glfeedbackbuffer-function"></a>Função glFeedbackBuffer

A **função glFeedbackBuffer** controla o modo de comentários.

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

Uma constante simbólica que descreve as informações que serão retornadas para cada vértice. As seguintes constantes simbólicas são aceitas: GL \_ 2D, GL \_ 3D, GL \_ 3D \_ COLOR, GL \_ 3D COLOR TEXTURE e \_ GL \_ \_ 4D \_ COLOR \_ TEXTURE.

</dd> <dt>

*Buffer* 
</dt> <dd>

Retorna os dados de comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* não era um valor aceito.<br/>                                                                                                                                                                           |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *size* era negativo.<br/>                                                                                                                                                                                        |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | **glFeedbackBuffer** foi chamado enquanto o modo de renderização era GL FEEDBACK ou glRenderMode foi chamado com o argumento GL FEEDBACK antes \_ [](glrendermode.md) \_ de **glFeedbackBuffer** ter sido chamado pelo menos uma vez.<br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                                                                  |



## <a name="remarks"></a>Comentários

A **função glFeedbackBuffer** controla os comentários. Comentários, como seleção, são um modo OpenGL. O modo é selecionado chamando [**glRenderMode com**](glrendermode.md) GL \_ FEEDBACK. Quando o OpenGL está no modo de comentários, nenhum pixel é produzido pela rasterização. Em vez disso, as informações sobre primitivos que teriam sido rasterizados são alimentadas novamente para o aplicativo usando OpenGL.

A **função glFeedbackBuffer** tem três argumentos:

-   *buffer* é um ponteiro para uma matriz de valores de ponto flutuante na qual as informações de comentários são colocadas.
-   *size* indica o tamanho da matriz.
-   *type* é uma constante simbólica que descreve as informações que são alimentadas de volta para cada vértice.

Você deve emitir **glFeedbackBuffer** antes que o modo de comentários seja habilitado (chamando **glRenderMode** com o argumento GL \_ FEEDBACK). Configurar o GL FEEDBACK sem estabelecer o buffer de comentários ou chamar \_ **glFeedbackBuffer** enquanto o OpenGL estiver no modo de comentários, é um erro.

Tire o OpenGL do modo de comentários chamando [**glRenderMode com**](glrendermode.md) um valor de parâmetro diferente de GL \_ FEEDBACK. Quando você faz isso enquanto o OpenGL está no modo de comentários, **glRenderMode** retorna o número de entradas colocadas na matriz de comentários. O valor retornado nunca excede o *tamanho*. Se os dados de comentários exigirem mais espaço do que estava disponível no *buffer,* **glRenderMode** retornará um valor negativo.

No modo de comentários, cada primitivo que seria rasterizado gera um bloco de valores copiados para a matriz de comentários. Se isso faria com que o número de entradas excedesse o máximo, **glFeedbackBuffer** grava parcialmente o bloco para preencher a matriz (se houver espaço) e define um sinalizador de estouro. Cada bloco começa com um código que indica o tipo primitivo, seguido por valores que descrevem os vértices e os dados associados do primitivo. A **função glFeedbackBuffer** também grava entradas para bitmaps e retângulos de pixel. Os comentários ocorrem após a redução de polígono e a interpretação [**glPolygonMode**](glpolygonmode.md) de polígonos, portanto, polígonos que são eliminados não são retornados no buffer de comentários. Isso também pode ocorrer depois que polígonos com mais de três bordas são divididos em triângulos, se a implementação do OpenGL renderiza polígonos executando essa decomposição.

Você pode inserir um marcador no buffer de comentários com [**glPassThrough.**](glpassthrough.md)

A seguir está a gramática para os blocos de valores gravados no buffer de comentários. Cada primitivo é indicado com um valor de identificação exclusivo seguido por algum número de vértices. Entradas de polígono incluem um valor inteiro que indica quantos vértices seguem. Um vértice é alimentado de volta como um número de valores de ponto flutuante, conforme determinado pelo *tipo*. As cores são alimentadas novamente como quatro valores no modo RGBA e um valor no modo de índice de cores.

feedbackList < feedbackItem feedbackList \| feedbackItem

feedbackItem < linha de bitmap de \| \| polígono de polígono \| \| pixelRectangle \| passThru

vértice < \_ TOKEN GL POINT \_

vértice lineSegment < \_ \_ vértice GL LINE TOKEN vtex \| GL LINE RESET \_ \_ \_ TOKEN

polygon < GL \_ POLYGON \_ TOKEN n polySpec

polySpec < vértice de \| vértice polySpec

bitmap < \_ vértice GL BITMAP \_ TOKEN

vértice pixelRectangle < TOKEN DE PIXEL DE DESENHO GL \_ \_ \_ \| COPY \_ \_ \_

passThru < valor DE \_ \_ TOKEN DE PASSAGEM GL \_

vértice < \| 2d \| 3d \| 3dColor 3dColorTexture \| 4dColorTexture

Valor de < 2d

Valor do valor < 3d

3dColor < de valor de valor

3dColorTexture < valor value color tex

4dColorTexture < valor value value color tex

color < índice \| rgba

rgba < valor do valor

index < valor

valor < valor de valor de tex

O *parâmetro* value é um número de ponto flutuante e *n* é um inteiro de ponto flutuante que dá o número de vértices no polígono. A seguir estão constantes de ponto flutuante simbólico: GL \_ POINT \_ TOKEN, GL \_ LINE \_ TOKEN, GL LINE RESET \_ \_ \_ TOKEN, GL \_ POLYGON \_ TOKEN, GL \_ BITMAP \_ TOKEN, GL DRAW PIXEL \_ TOKEN, GL COPY PIXEL TOKEN e \_ \_ GL PASS THROUGH \_ \_ \_ \_ \_ \_ TOKEN. GL \_ LINE RESET TOKEN é retornado sempre que o padrão de apple de linha é \_ \_ redefinido. Os dados retornados como um vértice dependem do tipo de *comentários*.

A tabela a seguir fornece a correspondência entre *o tipo* e o número de valores por vértice; *k* é 1 no modo de índice de cores e 4 no modo RGBA.



| Tipo                   | Coordenadas        | Color | Textura | Número total de valores |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2D                 | *x*, *y*           |       |         | 2                      |
| GL \_ 3D                 | *x*, *y*, *z*      |       |         | 3                      |
| COR \_ 3D GL \_          | *x*, *y*, *z*      | *K*   |         | 3 + *k*                |
| TEXTURA DE \_ COR 3D GL \_ \_ | *x*, *y*, *z*,     | *K*   | 4       | 7 + *k*                |
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

 

 





