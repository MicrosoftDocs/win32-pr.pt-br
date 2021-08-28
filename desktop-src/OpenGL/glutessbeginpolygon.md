---
title: Função gluTessBeginPolygon (Glu.h)
description: As funções gluTessBeginPolygon e gluTessEndPolygon delimitam uma descrição de polígono. | Função gluTessBeginPolygon (Glu.h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- Função GluTessBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42566cf8a0674086883e6333a67ac2df03329f6a9bd3bb903ef558af3c430b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777386"
---
# <a name="glutessbeginpolygon-function"></a>Função gluTessBeginPolygon

As **funções gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitam uma descrição de polígono.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*dados de \_ polígono* 
</dt> <dd>

Um ponteiro para uma estrutura de dados de polígono definida pelo programador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As **funções gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitam a definição de um polígono nãoconvex. Dentro de **cada par gluTessBeginPolygon**  /  **gluTessEndPolygon,** inclua uma ou mais chamadas para [**gluTessBeginContour.**](glutessbegincontour.md) Em cada contorno, há zero ou mais chamadas para [**gluTessVertex.**](glutessvertex.md) Os vértices especificam um contorno fechado (o último vértice de cada contorno é vinculado automaticamente ao primeiro).

O *parâmetro de dados de \_ polígono* é um ponteiro para uma estrutura de dados definida pelo programador. Se os retornos de chamada apropriados são especificados (consulte [*gluTessCallback*](glutess.md)), esse ponteiro é retornado para a função ou funções de retorno de chamada, tornando-o uma maneira conveniente de armazenar informações por polígono.

Quando você chama [**gluTessEndPolygon**](glutessendpolygon.md), o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada. Para ver descrições das funções de retorno de chamada, [*consulte gluTessCallback*](glutess.md).

## <a name="examples"></a>Exemplos

O seguinte descreve um quedasateral com um orifício triangular:

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





