---
title: Função glBitmap (Gl.h)
description: A função glBitmap desenha um bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- Função glBitmap OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da90b8e592f8cd9d1702c7810990042b3929ef40e70814e8fb7d3326d902cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082226"
---
# <a name="glbitmap-function"></a>Função glBitmap

A **função glBitmap** desenha um bitmap.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*width* 
</dt> <dd>

A largura de pixel da imagem de bitmap.

</dd> <dt>

*altura* 
</dt> <dd>

A altura de pixel da imagem de bitmap.

</dd> <dt>

*xorig* 
</dt> <dd>

O *local x* da origem na imagem de bitmap. A origem é medida do canto inferior esquerdo do bitmap, com as direções para a direita e para cima sendo os eixos positivos.

</dd> <dt>

*yorig* 
</dt> <dd>

O *local y* da origem na imagem de bitmap. A origem é medida do canto inferior esquerdo do bitmap, com as direções para a direita e para cima sendo os eixos positivos.

</dd> <dt>

*xmove* 
</dt> <dd>

O *deslocamento x* a ser adicionado à posição de raster atual depois que o bitmap é desenhado.

</dd> <dt>

*ymove* 
</dt> <dd>

O *deslocamento y* a ser adicionado à posição de raster atual depois que o bitmap é desenhado.

</dd> <dt>

*bitmap* 
</dt> <dd>

O endereço da imagem de bitmap.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *largura* ou *altura* é negativa.<br/>                                                                                           |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Um bitmap é uma imagem binária. Quando desenhado, o bitmap é posicionado em relação à posição de raster atual e os pixels de framebuffer correspondentes a 1s no bitmap são gravados usando a cor ou o índice de raster atual. Os pixels de buffer de quadro correspondentes a zeros no bitmap não são modificados.

A imagem de bitmap é interpretada como dados de imagem para  a  função [**glDrawPixels,**](gldrawpixels.md) com largura  e altura correspondentes aos argumentos de largura e altura dessa função e com o tipo definido como GL BITMAP e formato definido como \_ GL COLOR  \_ \_ INDEX. Os modos especificados usando [**glPixelStore afetam**](glpixelstore-functions.md) a interpretação de dados de imagem de bitmap; os modos que você especifica [**usando glPixelTransfer**](glpixeltransfer.md) não especificam.

Se a posição atual do raster for inválida, **glBitmap** será ignorado. Caso contrário, o canto inferior esquerdo da imagem de bitmap será posicionado nas seguintes coordenadas de janela:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?

Nessas coordenadas, (*x*<sub>r</sub> , *y*<sub>r</sub> ) é a posição de raster e (*x*? , *y*? ) é a origem do bitmap. Os fragmentos são gerados para cada pixel correspondente a um 1 na imagem de bitmap. Esses fragmentos são gerados usando o raster *z*-coordinate, color ou color index atual e as coordenadas de textura raster atuais. Em seguida, eles são tratados como se tivessem sido gerados por um ponto, linha ou polígono, incluindo mapeamento de textura, desaqueamento e todas as operações por fragmento, como teste alfa e profundidade.

Depois que o bitmap tiver sido desenhado, as coordenadas *x* e *y* da posição de raster atual serão deslocadas por *xmove* *e ymove.* Nenhuma alteração é feita na *coordenada z* da posição atual do raster ou nas coordenadas de cor, índice ou textura atuais.

As funções a seguir recuperam informações relacionadas à **função glBitmap:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ CURRENT \_ RASTER \_ POSITION

 

**glGet** com o argumento GL \_ CURRENT \_ RASTER \_ COLOR

 

**glGet** com o argumento GL \_ CURRENT \_ RASTER \_ INDEX

 

**glGet com** argumento GL \_ CURRENT \_ RASTER TEXTURE \_ \_ COORDS

 

**glGet com** o argumento GL \_ CURRENT \_ RASTER POSITION \_ \_ VALID

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





