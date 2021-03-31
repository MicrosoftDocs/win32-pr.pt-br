---
title: função glGetPolygonStipple (GL. h)
description: A função glGetPolygonStipple retorna o padrão de polígono Stipple.
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- função glGetPolygonStipple OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824238"
---
# <a name="glgetpolygonstipple-function"></a>função glGetPolygonStipple

A função **glGetPolygonStipple** retorna o padrão de polígono Stipple.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mascara* 
</dt> <dd>

Retorna o padrão Stipple.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetPolygonStipple** retorna um padrão de Stipple de polígono de 32x32 por meio do parâmetro *Mask* . O padrão é empacotado na memória como se [**glReadPixels**](glreadpixels.md) com *altura* e *largura* de 32, *tipo* de \_ bitmap GL e *formato* do índice de cores GL ser \_ \_ chamado, e o padrão Stipple fosse armazenado em um buffer de índice de cores 32x32 interno. Ao contrário de **glReadPixels**, no entanto, as operações de transferência de pixels (Shift, deslocamento e mapa de pixel) não são aplicadas à imagem Stipple retornada.

Se um erro for gerado, nenhuma alteração será feita no conteúdo da *máscara*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





