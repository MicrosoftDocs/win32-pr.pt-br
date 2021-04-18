---
title: função gluNurbsCallback (Glu. h)
description: A função gluNurbsCallback define um retorno de chamada para um objeto B-spline racional não uniforme (NURBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- função gluNurbsCallback OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778532"
---
# <a name="glunurbscallback-function"></a>função gluNurbsCallback

A função **gluNurbsCallback** define um retorno de chamada para um objeto B-spline racional não uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto NURBS (criado com [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*Onde* 
</dt> <dd>

O retorno de chamada que está sendo definido. O único valor válido é GLU \_ Error. O significado do \_ erro Glu significa que a função Error é chamada quando um erro é encontrado. Seu único argumento é do tipo **GLenum** e indica o erro específico que ocorreu. Há 37 erros exclusivos para NURBS, denominados GLU \_ NURBS \_ ERROR1 por meio de Glu \_ NURBS \_ ERROR37. As cadeias de caracteres que descrevem esses erros podem ser recuperadas com [**gluErrorString**](gluerrorstring.md).

</dd> <dt>

*fn* 
</dt> <dd>

Um ponteiro para a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluNurbsCallback** para definir um retorno de chamada a ser usado por um objeto NURBS. Se o retorno de chamada especificado já estiver definido, ele será substituído. Se *FN* for **NULL**, qualquer retorno de chamada existente será apagado.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





