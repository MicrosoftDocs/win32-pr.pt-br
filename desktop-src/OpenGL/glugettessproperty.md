---
title: Função gluGetTessProperty (Glu.h)
description: A função gluGetTessProperty obtém uma propriedade de objeto de mosaico.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- Função gluGetTessProperty OpenGL
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
ms.openlocfilehash: d12e7ca8099197b663893b1edcf04dd8fa98348fe4f6d3d324b54f33904e026a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554236"
---
# <a name="glugettessproperty-function"></a>Função gluGetTessProperty

A **função gluGetTessProperty** obtém uma propriedade de objeto de mosaico.

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

*Tess* 
</dt> <dd>

O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*Que* 
</dt> <dd>

A propriedade cujo valor deve ser recuperado. Os seguintes valores são válidos: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS \_ BOUNDARY ONLY e GLU TESS \_ \_ \_ TOLERANCE.

</dd> <dt>

*value* 
</dt> <dd>

Um ponteiro para o local em que o valor da propriedade nomeada é gravado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluGetTessProperty** para recuperar propriedades armazenadas em um objeto de mosaico. Essas propriedades afetam a maneira como os objetos de mosaico são interpretados e renderizados. Para obter informações sobre o que são as propriedades e o que elas fazem, consulte [**gluTessProperty**](glutessproperty.md).

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

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





