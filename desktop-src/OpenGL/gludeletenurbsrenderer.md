---
title: Função gluDeleteNdelasRenderer (Glu.h)
description: A função gluDeleteNdelasRenderer destrói um objeto N UNIFORM Rational B-Spline (N UNIFORM B-Spline).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- Função gluDeleteNdelasRenderer OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b114c6d67452468f3b8b92e443580d8d6f06c7df8bc1b6647916c210d204955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613013"
---
# <a name="gludeletenurbsrenderer-function"></a>Função gluDeleteNdelasRenderer

A **função gluDeleteNdelasRenderer** destrói um objeto [N LTDS](using-nurbs-curves-and-surfaces.md)(Racional B-Spline Não Uniforme).

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nobj* 
</dt> <dd>

O objeto N LTDA a ser destruído (criado com **gluNewNheisRenderer**).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A **função gluDeleteNdelasRenderer** destrói o objeto NTLES e libera qualquer memória usada. Depois de chamar **gluDeleteNdelasRenderer**, você não poderá *usar nobj* novamente.

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

[**gluNewNagisRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





