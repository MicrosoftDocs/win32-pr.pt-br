---
title: função glPolygonStipple (GL. h)
description: A função glPolygonStipple define o padrão de polígono stippling.
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- função glPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f9098ab91af5f258f97e0878ae8cbcb19863ec3bc82765c2664683830539fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614902"
---
# <a name="glpolygonstipple-function"></a>função glPolygonStipple

A função **glPolygonStipple** define o padrão de polígono stippling.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mask* 
</dt> <dd>

Um ponteiro para um padrão de 32x32 Stipple que será desempacotado da memória da mesma maneira que o [**glDrawPixels**](gldrawpixels.md) descompacta pixels.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glPolygonStipple** define o padrão de polígono stippling. Stippling Polygon, como line stippling (consulte [**glLineStipple**](gllinestipple.md)), mascara alguns fragmentos produzidos pela rasterização, criando um padrão. Stippling é independente de anti-aliasing poligonal.

O parâmetro *Mask* é um ponteiro para um padrão de 32x32 Stipple que é armazenado na memória assim como os dados de pixel fornecidos para **glDrawPixels** com *altura* e *largura* iguais a 32, um *formato* de pixel do \_ índice de cores GL e o \_ *tipo* de dados de \_ bitmap GL. Ou seja, o padrão Stipple é representado como uma matriz de 32 bits de índices de cores de 1 bit empacotados em bytes não assinados. Os parâmetros da função [**glPixelStore**](glpixelstore-functions.md) , como GL \_ Unpack \_ swap \_ bytes e GL \_ Unpack \_ LSB \_ First, afetam a montagem dos bits em um padrão Stipple. As operações de transferência de pixel (Shift, deslocamento e mapa de pixel) não são aplicadas à imagem Stipple, no entanto.

O stippling Polygon está habilitado e desabilitado com [**glEnable**](glenable.md) e **glDisable**, usando o \_ polígono GL Polygon \_ STIPPLE. Se habilitado, um fragmento de polígono rasterizado com coordenadas de janela *x*<sub>w</sub> e *y*<sub>w</sub> será enviado para o próximo estágio do OpenGL se e somente se o (*x*<sub>w</sub> mod 32) de bit na linha (*y*<sub>w</sub> mod 32) th do padrão Stipple for um. Quando stippling Polygon é desabilitado, é como se o padrão Stipple fosse todos.

As funções a seguir recuperam informações relacionadas ao **glPolygonStipple**:

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[**glIsEnabled**](glisenabled.md) com o argumento GL \_ Polygon \_ STIPPLE

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





