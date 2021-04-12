---
title: função gluGetTessProperty (Glu. h)
description: A função gluGetTessProperty Obtém uma propriedade de objeto de mosaico.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- função gluGetTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369516"
---
# <a name="glugettessproperty-function"></a>função gluGetTessProperty

A função **gluGetTessProperty** Obtém uma propriedade de objeto de mosaico.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*Onde* 
</dt> <dd>

A propriedade cujo valor deve ser recuperado. Os seguintes valores são válidos: GLU \_ Tess \_ rebobination \_ Rule, glu \_ Tess \_ limite e a \_ \_ tolerância Glu Tess \_ .

</dd> <dt>

*value* 
</dt> <dd>

Um ponteiro para o local onde o valor da propriedade nomeada é gravado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluGetTessProperty** para recuperar as propriedades armazenadas em um objeto de mosaico. Essas propriedades afetam o modo como os objetos de mosaico são interpretados e renderizados. Para obter informações sobre o que são as propriedades e o que elas fazem, consulte [**gluTessProperty**](glutessproperty.md).

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

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





