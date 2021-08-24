---
title: Função glRasterPos4fv (Gl.h)
description: Especifica a posição de raster para operações de pixel. | Função glRasterPos4fv (Gl.h)
ms.assetid: acbaf057-ae90-4980-830c-e0dfc8080a84
keywords:
- Função glRasterPos4fv OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4fv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fb8e731bd08609c4db3d5e2bdb44269833f610771d6bf6e123067878688e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492256"
---
# <a name="glrasterpos4fv-function"></a>Função glRasterPos4fv

Especifica a posição de raster para operações de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRasterPos4fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*v* 
</dt> <dd>

Um ponteiro para uma matriz de quatro elementos, especificando as coordenadas x, y, z e w para a posição de raster atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O OpenGL mantém uma posição 3D nas coordenadas da janela. Essa posição, chamada de posição raster, é mantida com precisão de subpixel. Ele é usado para posicionar operações de gravação de pixel e bitmap. Consulte [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)e [**glCopyPixels**](glcopypixels.md).

A posição atual do raster consiste em três coordenadas de janela (*x, y, z*), um valor *w* da coordenada de clipe, uma distância da coordenada ocular, um bit válido e coordenadas de textura e dados de cores associados. A *coordenada w* é uma coordenada de clipe, porque *w* não é projetado para coordenadas de janela. A [função glRasterPos4](glrasterpos-functions.md) especifica as coordenadas de objeto *x, y, z* e *w* explicitamente. A função glRasterPos3 especifica as coordenadas de objeto *x, y* e *z* explicitamente, enquanto *w* é definido implicitamente como um. A função glRasterPos2 usa os valores de argumento *para x* e *y* enquanto configura implicitamente *z* e *w* como zero e um.

As coordenadas de objeto apresentadas [por glRasterPos](glrasterpos-functions.md) são tratadas exatamente como aquelas de um [comando glVertex.](glvertex-functions.md) Eles são transformados pela modelview atual e matrizes de projeção e passados para o estágio de recorte. Se o vértice não for eliminado, ele será projetado e dimensionado para coordenadas de janela, que se tornam a nova posição de raster atual e o sinalizador GL \_ CURRENT \_ RASTER \_ POSITION VALID \_ será definido. Se o vértice for eliminado, o bit válido será limpo e a posição atual do raster e as coordenadas de cor e textura associadas serão indefinidas.

A posição atual do raster também inclui alguns dados de cores associados e coordenadas de textura. Se a iluminação estiver habilitada, GL CURRENT RASTER COLOR, no modo RGBA ou GL CURRENT RASTER INDEX, no modo de índice de cores, será definido como a cor produzida pelo cálculo de iluminação \_ \_ \_ \_ \_ \_ (consulte [glLight,](gllight-functions.md) [glLightModel](gllightmodel-functions.md)e [**glShadeModel**](glshademodel.md)). Se a iluminação estiver desabilitada, a cor atual (no modo RGBA, a variável de estado GL CURRENT COLOR) ou o índice de cores (no modo de índice de cores, variável de estado GL CURRENT INDEX) será usado para atualizar a cor atual do \_ \_ \_ \_ raster.

Da mesma forma, o GL CURRENT RASTER TEXTURE COORDS é atualizado como uma função de GL CURRENT TEXTURE COORDS, com base na matriz de textura e nas funções de geração de textura \_ \_ \_ \_ \_ \_ \_ (consulte [glTexGen](gltexgen-functions.md)). Por fim, a distância da origem do sistema de coordenadas ocular para o vértice, como transformado apenas pela matriz modelview, substitui a DISTÂNCIA DE \_ RASTER ATUAL \_ \_ GL.

Inicialmente, a posição atual do raster é (0,0,0,1), a distância atual do raster é 0, o bit válido é definido, a cor RGBA associada é (1,1,1,1), o índice de cores associado é 1 e as coordenadas de textura associadas são (0, 0, 0, 0, 1). No modo RGBA, GL CURRENT RASTER INDEX é sempre 1; no modo de índice de cores, a cor RGBA de raster atual sempre \_ \_ mantém seu valor \_ inicial.

> [!Note]  
> A posição de raster é modificada por [glRasterPos](glrasterpos-functions.md) e por [**glBitmap.**](glbitmap.md)

 

> [!Note]  
> Quando as coordenadas de posição de raster são inválidas, os comandos de desenho baseados na posição de raster são ignorados (ou seja, elas não resultam em alterações no estado OpenGL).

 

As funções a seguir recuperam informações relacionadas [a glRasterPos:](glrasterpos-functions.md)

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ RASTER \_ POSITION  
[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o argumento GL \_ CURRENT \_ RASTER POSITION \_ \_ VALID  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ RASTER \_ DISTANCE  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ RASTER \_ COLOR  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ RASTER \_ INDEX  
[**glGet com**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argumento GL \_ CURRENT \_ RASTER TEXTURE \_ \_ COORDS  
</dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[glLight](gllight-functions.md)
</dt> <dt>

[glLightModel](gllightmodel-functions.md)
</dt> <dt>

[**glShadeModel**](glshademodel.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





