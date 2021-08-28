---
title: Função gluNheisCallback (Glu.h)
description: A função gluNheisCallback define um retorno de chamada para um objeto N UNIFORM Rational B-Spline (N UNIFORM B-Spline).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- Função gluNinasCallback OpenGL
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
ms.openlocfilehash: d1da7ebc999d44911cb345b051213a12865e608db7b7fe66e33eb1bb567ef7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519496"
---
# <a name="glunurbscallback-function"></a>Função gluNinasCallback

A **função gluNinasCallback** define um retorno de chamada para um objeto N UNIFORM Rational B-Spline ([N UNIFORM](using-nurbs-curves-and-surfaces.md)B-Spline ).

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

O objeto N LTDA (criado com [**gluNewNheisRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*Que* 
</dt> <dd>

O retorno de chamada que está sendo definido. O único valor válido é GLU \_ ERROR. O significado de GLU \_ ERROR significa que a função de erro é chamada quando um erro é encontrado. Seu único argumento é do tipo **GLenum** e indica o erro específico que ocorreu. Há 37 erros exclusivos para N LTDA, chamados GLU \_ N GLU N GLUS \_ ERROR1 por meio de GLU N \_ GLUS \_ ERROR37. Cadeias de caracteres que descrevem esses erros podem ser recuperadas [**com gluErrorString**](gluerrorstring.md).

</dd> <dt>

*fn* 
</dt> <dd>

Um ponteiro para a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Use **gluNinasCallback** para definir um retorno de chamada a ser usado por um objeto NALTERS. Se o retorno de chamada especificado já estiver definido, ele será substituído. Se *fn* for **NULL,** qualquer retorno de chamada existente será apagado.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





