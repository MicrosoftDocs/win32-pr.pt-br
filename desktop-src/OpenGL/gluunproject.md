---
title: função gluUnProject (Glu. h)
description: A função gluUnProject mapeia as coordenadas de janela para as coordenadas de objeto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- função gluUnProject OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761879"
---
# <a name="gluunproject-function"></a>função gluUnProject

A função **gluUnProject** mapeia as coordenadas de janela para as coordenadas de objeto.

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*winx* 
</dt> <dd>

A coordenada x da janela a ser mapeada.

</dd> <dt>

*winy* 
</dt> <dd>

A coordenada da janela y a ser mapeada.

</dd> <dt>

*winz* 
</dt> <dd>

A coordenada da janela z a ser mapeada.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

A matriz modelview (como de uma chamada [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

A matriz de projeção (como a partir de uma chamada **glGetDoublev** ).

</dd> <dt>

*visor* 
</dt> <dd>

O visor (como de uma chamada [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> <dt>

*objx* 
</dt> <dd>

A coordenada de objeto x computada.

</dd> <dt>

*objy* 
</dt> <dd>

A coordenada de objeto y computada.

</dd> <dt>

*objz* 
</dt> <dd>

A coordenada de objeto z computada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro.

Se a função falhar, o valor de retorno será GL \_ false.

## <a name="remarks"></a>Comentários

A função **gluUnProject** mapeia as coordenadas de janela especificadas em coordenadas de objeto usando *modelMatrix*, *projMatrix* e *viewport*. O resultado é armazenado em *objx*, *objy* e *objz*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>GLU. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetDoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluProject**](gluproject.md)
</dt> </dl>

 

 





