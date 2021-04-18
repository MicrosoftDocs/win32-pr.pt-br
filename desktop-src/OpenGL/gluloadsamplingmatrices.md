---
title: função gluLoadSamplingMatrices (Glu. h)
description: A função gluLoadSamplingMatrices carrega as matrizes de amostragem de B-spline racional não uniforme (NURBS) e de remoção.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- função gluLoadSamplingMatrices OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762929"
---
# <a name="gluloadsamplingmatrices-function"></a>função gluLoadSamplingMatrices

A função **gluLoadSamplingMatrices** carrega as matrizes de amostragem de B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)) e de remoção.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Uma matriz modelview (como a partir de uma chamada [**glGetFloatv**](glgetfloatv.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Uma matriz de projeção (como a partir de uma chamada **glGetFloatv** ).

</dd> <dt>

*visor* 
</dt> <dd>

Um visor (como de uma chamada [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluLoadSamplingMatrices** usa *modelMatrix*, *projMatrix* e *viewport* para recalcular a amostragem e a remoção de matrizes armazenadas no *nobj*. A matriz de amostragem determina quão fino uma curva NURBS ou uma superfície deve ser mosaico para satisfazer a tolerância de amostragem (conforme determinado pela \_ propriedade de tolerância de amostragem Glu \_ ). A matriz de remoção é usada para decidir se uma curva ou uma superfície NURBS deve ser reutilizada antes da renderização (quando a propriedade de remoção de GLU \_ está ativada).

A função **gluLoadSamplingMatrices** será necessária somente se a \_ propriedade da matriz de carga automática Glu \_ \_ estiver desativada (consulte [**gluNurbsProperty**](glunurbsproperty.md)). Embora possa ser conveniente deixar a \_ propriedade da matriz de carregamento automático do Glu \_ \_ ativada, isso exige uma viagem de ida e volta ao servidor OpenGL para obter os valores atuais da matriz modelview, da matriz de projeção e do visor.)

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

[**glGetFloatv**](glgetfloatv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





