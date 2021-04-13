---
title: função gluProject (Glu. h)
description: A função gluProject mapeia coordenadas de objeto para coordenadas de janela.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- função gluProject OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455582"
---
# <a name="gluproject-function"></a>função gluProject

A função **gluProject** mapeia coordenadas de objeto para coordenadas de janela.

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objx* 
</dt> <dd>

A coordenada x objeto.

</dd> <dt>

*objy* 
</dt> <dd>

A coordenada do objeto y.

</dd> <dt>

*objz* 
</dt> <dd>

A coordenada de objeto z.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

A matriz modelview atual (como a partir de uma chamada [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

A matriz de projeção atual (como a partir de uma chamada **glGetDoublev** ).

</dd> <dt>

*visor* 
</dt> <dd>

O visor atual (como de uma chamada [**glGetIntegerv**](glgetintegerv.md) ).

</dd> <dt>

*winx* 
</dt> <dd>

A coordenada da janela x computada.

</dd> <dt>

*winy* 
</dt> <dd>

A coordenada da janela y computada.

</dd> <dt>

*winz* 
</dt> <dd>

A coordenada de janela z computada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será GL \_ verdadeiro.

Se a função falhar, o valor de retorno será GL \_ false.

## <a name="remarks"></a>Comentários

A função **gluProject** transforma as coordenadas do objeto especificado em coordenadas de janela usando *modelMatrix*, *projMatrix* e *viewport*. O resultado é armazenado em *Winx*, *winy* e *WINZ*.

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

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





