---
title: Função gluTessBeginContour (Glu.h)
description: As funções gluTessBeginContour e gluTessEndContour delimitam uma descrição de contorno. | Função gluTessBeginContour (Glu.h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- Função gluTessBeginContour OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc46eb3aa1be6b37c9276bcfd1c2b951162722689b0d0affc358a71119736f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937467"
---
# <a name="glutessbegincontour-function"></a>Função gluTessBeginContour

As **funções gluTessBeginContour** e [**gluTessEndContour**](glutessendcontour.md) delimitam uma descrição de contorno.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluTessBeginContour(
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

As **funções gluTessBeginContour** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitam a definição de um polígono. Dentro de **cada par gluTessBeginContour** / **gluTessEndPolygon,** pode haver zero ou mais chamadas para [**gluTessVertex.**](glutessvertex.md) Os vértices especificam um contorno fechado (o último vértice de cada contorno é vinculado automaticamente ao primeiro). Você pode chamar **gluTessBeginContour** somente entre [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon**.

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

 

 





