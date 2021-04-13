---
title: função gluTessVertex (Glu. h)
description: A função gluTessVertex especifica um vértice em um polígono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- função gluTessVertex OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499734"
---
# <a name="glutessvertex-function"></a>função gluTessVertex

A função **gluTessVertex** especifica um vértice em um polígono.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*coords* 
</dt> <dd>

O local do vértice.

</dd> <dt>

*data* 
</dt> <dd>

Um ponteiro passado de volta para o programa com o retorno de chamada de vértice (conforme especificado por [*gluTessCallback*](glutess.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluTessVertex** descreve um vértice em um polígono que o usuário está definindo. As chamadas de **gluTessVertex** sucessivas descrevem uma delimitação de fechamento. Por exemplo, para descrever um diamante, chame **gluTessVertex** quatro vezes. Você só pode chamar **gluTessVertex** entre [**gluTessBeginContour**](glutessbegincontour.md) e [**gluTessEndContour**](glutessendcontour.md).

O parâmetro de *dados* normalmente aponta para uma estrutura que contém o local do vértice, bem como outros atributos por vértice, como Color e normal. Esse ponteiro é passado de volta para o programa por meio do \_ retorno de chamada de vértice Glu após o mosaico (consulte [*gluTessCallback*](glutess.md)).

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

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





