---
title: Função gluTessEndPolygon (Glu.h)
description: As funções gluTessBeginPolygon e gluTessEndPolygon delimitam uma descrição de polígono. | Função gluTessEndPolygon (Glu.h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- Função gluTessEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65102f1627df682508725d46fc5fa299244e767c318382eacaf3585aa4a471e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061544"
---
# <a name="glutessendpolygon-function"></a>Função gluTessEndPolygon

As [**funções gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitam uma descrição de polígono.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

As [**funções gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitam a definição de um polígono nãoconvex. Dentro de **cada par gluTessBeginPolygon**  /  **gluTessEndPolygon,** inclua uma ou mais chamadas para [**gluTessBeginContour.**](glutessbegincontour.md) Em cada contorno, há zero ou mais chamadas para [**gluTessVertex.**](glutessvertex.md) Os vértices especificam um contorno fechado (o último vértice de cada contorno é vinculado automaticamente ao primeiro).

O *parâmetro de dados de \_ polígono* é um ponteiro para uma estrutura de dados definida pelo programador. Se os retornos de chamada apropriados são especificados (consulte [*gluTessCallback*](glutess.md)), esse ponteiro é retornado para a função ou funções de retorno de chamada, tornando-o uma maneira conveniente de armazenar informações por polígono.

Quando você chama **gluTessEndPolygon**, o polígono é mosaico e os triângulos resultantes são descritos por meio de retornos de chamada. Para ver descrições das funções de retorno de chamada, [*consulte gluTessCallback*](glutess.md).

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

 

 





