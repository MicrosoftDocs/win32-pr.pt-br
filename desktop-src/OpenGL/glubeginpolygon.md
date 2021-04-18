---
title: função gluBeginPolygon (Glu. h)
description: As funções gluBeginPolygon e gluEndPolygon delimitam uma descrição de polígono. | função gluBeginPolygon (Glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- função gluBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756179"
---
# <a name="glubeginpolygon-function"></a>função gluBeginPolygon

\[A função **gluBeginPolygon** é obsoleta e é fornecida somente para fins de compatibilidade com versões anteriores. A função **gluBeginPolygon** é mapeada para [**GluTessBeginPolygon**](glutessbeginpolygon.md) seguida por [**gluTessBeginContour**](glutessbegincontour.md).\]

As funções **gluBeginPolygon** e [**gluEndPolygon**](gluendpolygon.md) delimitam uma descrição de polígono.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluBeginPolygon(
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

Use **gluBeginPolygon** e **gluEndPolygon** para delimitar a definição de um polígono nonconvex.

1.  Chame **gluBeginPolygon**.
2.  Defina os contornos do polígono chamando [**gluTessVertex**](glutessvertex.md) para cada vértice e [**gluNextContour**](glunextcontour.md) para iniciar cada delimitação nova.
3.  Chame **gluEndPolygon** para sinalizar o fim da definição.

    Quando **gluEndPolygon** é chamado, o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada. Para obter descrições das funções de retorno de chamada, consulte [*gluTessCallback*](glutess.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir descreve um diamante com um buraco triangular:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

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

[**gluNextContour**](glunextcontour.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





