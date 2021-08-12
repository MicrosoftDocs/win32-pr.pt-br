---
title: função glRasterPos3f (GL. h)
description: Especifica a posição da varredura para operações de pixel. | função glRasterPos3f (GL. h)
ms.assetid: edb3b114-fd65-40f6-8fba-5306b8b89c11
keywords:
- função glRasterPos3f OpenGL
topic_type:
- apiref
api_name:
- glRasterPos3f
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c65c3e0377e57c13b21a36a3142030a64812e5e84d31617796c9617d50822c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614655"
---
# <a name="glrasterpos3f-function"></a>função glRasterPos3f

Especifica a posição da varredura para operações de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glRasterPos3f(
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*x* 
</dt> <dd>

Especifica a coordenada x para a posição de rasterização atual.

</dd> <dt>

*y* 
</dt> <dd>

Especifica a coordenada y da posição de rasterização atual.

</dd> <dt>

*z* 
</dt> <dd>

Especifica a coordenada z para a posição de rasterização atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O OpenGL mantém uma posição de 3D em coordenadas de janela. Essa posição, chamada de posição de rasterização, é mantida com precisão de subpixel. Ele é usado para posicionar operações de gravação de pixel e bitmap. Consulte [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)e [**glCopyPixels**](glcopypixels.md).

A posição de rasterização atual consiste em três coordenadas de janela (*x, y, z*), uma coordenada de clipe *w* , uma distância de coordenadas de olho, um bit válido e coordenadas de textura e de dados de cor associadas. A coordenada *w* é uma coordenada de clipe, porque *w* não é projetado para coordenadas de janelas. A função [glRasterPos4](glrasterpos-functions.md) especifica as coordenadas de objeto *x, y, z* e *w* explicitamente. A função glRasterPos3 especifica as coordenadas de objeto *x, y* e *z* explicitamente, enquanto *w* é definido implicitamente como um. A função glRasterPos2 usa os valores de argumento para *x* e *y* enquanto configura implicitamente *z* e *w* como zero e um.

As coordenadas de objeto apresentadas por [glRasterPos](glrasterpos-functions.md) são tratadas exatamente como as de um comando [glVertex](glvertex-functions.md) . Elas são transformadas pelas matrizes de modelview e projeção atuais e passadas para o estágio de recorte. Se o vértice não for remarcado, ele será projetado e dimensionado para as coordenadas da janela, que se tornarão a nova posição de varredura atual e \_ o \_ sinalizador válido da posição de varredura atual do GL \_ \_ estiver definido. Se o vértice for removido, o bit válido será limpo e a posição atual da varredura e as coordenadas de cor e textura associadas serão indefinidas.

A posição de rasterização atual também inclui alguns dados de cor e coordenadas de textura associados. Se a iluminação estiver habilitada, \_ \_ a cor de rasterização atual do GL \_ , no modo RGBA ou no \_ índice de varredura atual GL \_ \_ , no modo de índice de cor, será definida como a cor produzida pelo cálculo de iluminação (consulte [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)e [**glShadeModel**](glshademodel.md)). Se a iluminação estiver desabilitada, a cor atual (no modo RGBA, a cor atual do estado do GL \_ \_ ) ou o índice de cores (no modo de índice de cor, índice atual GL de variável de estado \_ \_ ) será usado para atualizar a cor de varredura atual.

Da mesma forma, GL \_ \_ CoOrds de textura de rasterização atual \_ \_ é atualizado como uma função de \_ CoOrds de textura atual do GL \_ \_ , com base na matriz de textura e nas funções de geração de textura (consulte [glTexGen](gltexgen-functions.md)). Por fim, a distância da origem do sistema de coordenadas de olho ao vértice, como transformado apenas pela matriz modelview, substitui a \_ distância de varredura atual do GL \_ \_ .

Inicialmente, a posição de rasterização atual é (0, 0, 0, 1), a distância de varredura atual é 0, o bit válido é definido, a cor RGBA associada é (1, 1, 1, 1), o índice de cor associado é 1 e as coordenadas de textura associadas são (0, 0, 0, 1). No modo RGBA, \_ \_ o índice de varredura atual \_ do GL é sempre 1; no modo de índice de cor, a cor RGBA atual sempre mantém seu valor inicial.

> [!Note]  
> A posição da rasterização é modificada por [glRasterPos](glrasterpos-functions.md) e por [**glBitmap**](glbitmap.md).

 

> [!Note]  
> Quando as coordenadas de posição de rasterização são inválidas, os comandos de desenho baseados na posição de rasterização são ignorados (ou seja, eles não resultam em alterações no estado OpenGL).

 

As funções a seguir recuperam informações relacionadas ao [glRasterPos](glrasterpos-functions.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ posição de rasterização atual \_ \_ válida  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL a \_ \_ distância de rasterização atual \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ cor de rasterização atual \_  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) \_ \_ índice de varredura atual glGet com Argument GL \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ \_ textura de rasterização atual \_ \_ CoOrds  
</dl>

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

 

 





