---
title: função gluTessEndContour (Glu. h)
description: As funções gluTessBeginContour e gluTessEndContour delimitam uma descrição de contorno. | função gluTessEndContour (Glu. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- função gluTessEndContour OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0685a4af264dd2d4093fbb754c09d2124ecb2689063b61280bf55337ebb305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777406"
---
# <a name="glutessendcontour-function"></a>função gluTessEndContour

As funções [**gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitam uma descrição de contorno.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As funções [**gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitam a definição de uma delimitação de polígono. Em cada par **gluTessBeginContour** / **gluTessEndContour** , pode haver zero ou mais chamadas para [**gluTessVertex**](glutessvertex.md). Os vértices especificam uma delimitação fechada (o último vértice de cada contorno é automaticamente vinculado ao primeiro). Você pode chamar **gluTessBeginContour** somente entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) e [**gluTessEndPolygon**](glutessendpolygon.md).

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





