---
title: função glBitmap (GL. h)
description: A função glBitmap desenha um bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- função glBitmap OpenGL
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
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009474"
---
# <a name="glbitmap-function"></a>função glBitmap

A função **glBitmap** desenha um bitmap.

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

O local *x* da origem na imagem de bitmap. A origem é medida do canto inferior esquerdo do bitmap, com direções para a direita e para cima sendo os eixos positivos.

</dd> <dt>

*yorig* 
</dt> <dd>

A localização *y* da origem na imagem de bitmap. A origem é medida do canto inferior esquerdo do bitmap, com direções para a direita e para cima sendo os eixos positivos.

</dd> <dt>

*xmove* 
</dt> <dd>

O deslocamento *x* a ser adicionado à posição de varredura atual após o bitmap ser desenhado.

</dd> <dt>

*ymove* 
</dt> <dd>

O deslocamento *y* a ser adicionado à posição de varredura atual após o bitmap ser desenhado.

</dd> <dt>

*bitmap* 
</dt> <dd>

O endereço da imagem de bitmap.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *largura* ou a *altura* é negativa.<br/>                                                                                           |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Um bitmap é uma imagem binária. Quando desenhado, o bitmap é posicionado em relação à posição atual da rasterização e os pixels de framebuffer correspondentes ao 1s no bitmap são gravados usando a cor ou índice de rasterização atual. Os pixels do buffer de quadros correspondentes a zeros no bitmap não são modificados.

A imagem de bitmap é interpretada como dados de imagem para a função [**glDrawPixels**](gldrawpixels.md) , com *largura* e *altura* correspondentes aos argumentos de largura e altura dessa função, e com o *tipo* definido como bitmap GL \_ e o *formato* definido como o índice de \_ cores GL \_ . Os modos que você especifica usando [**glPixelStore**](glpixelstore-functions.md) afetam a interpretação de dados de imagem de bitmap; os modos que você especificar usando [**glPixelTransfer**](glpixeltransfer.md) não.

Se a posição atual da rasterização for inválida, **glBitmap** será ignorado. Caso contrário, o canto inferior esquerdo da imagem de bitmap será posicionado nas seguintes coordenadas da janela:

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?

*y*<sub>l</sub>  =  *y*<sub>r</sub> *y*?

Nessas coordenadas, (*x*<sub>r</sub> , *y*<sub>r</sub> ) é a posição da rasterização e (*x*? , *y*? ) é a origem do bitmap. Os fragmentos são então gerados para cada pixel correspondente a um 1 na imagem de bitmap. Esses fragmentos são gerados usando a coordenada *z* de rasterização atual, o índice de cor ou cor e as coordenadas de textura de rasterização atuais. Eles são tratados como se tivessem sido gerados por um ponto, uma linha ou um polígono, incluindo o mapeamento de textura, fogging e todas as operações por fragmento, como os testes alfa e Depth.

Depois que o bitmap tiver sido desenhado, as coordenadas *x* e *y* da posição de rasterização atual serão compensadas por *xmove* e *ymove*. Nenhuma alteração é feita na coordenada *z* da posição atual de rasterização ou nas coordenadas de cor de rasterização, índice ou textura atuais.

As funções a seguir recuperam informações relacionadas à função **glBitmap** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento \_ GL \_ posição de rasterização atual \_

 

**glGet** com o argumento \_ GL \_ cor de rasterização atual \_

 

 \_ \_ índice de varredura atual glGet com Argument GL \_

 

**glGet** com Argument GL \_ \_ textura de rasterização atual \_ \_ CoOrds

 

**glGet** com Argument GL \_ \_ posição de rasterização atual \_ \_ válida

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

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





