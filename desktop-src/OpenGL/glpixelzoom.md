---
title: função glPixelZoom (GL. h)
description: A função glPixelZoom especifica os fatores de zoom de pixel.
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- função glPixelZoom OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105755575"
---
# <a name="glpixelzoom-function"></a>função glPixelZoom

A função **glPixelZoom** especifica os fatores de zoom de pixel.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*xfactor* 
</dt> <dd>

O fator de zoom *x* para operações de gravação de pixel.

</dd> <dt>

*yfactor* 
</dt> <dd>

O fator de zoom *y* para operações de gravação de pixel.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glPixelZoom** especifica valores para os fatores de zoom *x* e *y* . Durante a execução de [**glDrawPixels**](gldrawpixels.md) ou [**glCopyPixels**](glcopypixels.md), if (*x*<sub>r</sub> ,*y*<sub>r</sub> ) é a posição atual da varredura e um determinado elemento está na coluna *n* th e *m* th do retângulo de pixel, em seguida, os pixels cujos centros estão no retângulo com os cantos em

![Equação mostrando os locais em que os pixels são candidatos para substituição.](images/pix05.png)

são candidatos para substituição. Qualquer pixel cujo centro esteja na borda inferior ou esquerda dessa região retangular também será modificado.

Os fatores de zoom de pixel não se limitam a valores positivos. Fatores de zoom negativos refletem a imagem resultante sobre a posição de rasterização atual.

As funções a seguir recuperam informações relacionadas ao **glPixelZoom**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL de \_ zoom \_ X

**glGet** com Argument GL \_ zoom \_ Y

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





