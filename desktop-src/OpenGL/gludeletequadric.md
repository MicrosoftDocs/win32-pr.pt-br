---
title: função gluDeleteQuadric (Glu. h)
description: A função gluDeleteQuadric destrói um objeto Quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- função gluDeleteQuadric OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c12bd77d3d8b7f7de641671916bb8a901d29d812dfa4e9af6ef116984a128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519616"
---
# <a name="gludeletequadric-function"></a>função gluDeleteQuadric

A função **gluDeleteQuadric** destrói um objeto Quadric.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*state* 
</dt> <dd>

O objeto Quadric a ser destruído (criado com [**gluNewQuadric**](glunewquadric.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

A função **gluDeleteQuadric** destrói o objeto Quadric e libera a memória que ele usou. Depois de ter chamado **gluDeleteQuadric**, você não poderá usar o *estado* novamente.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





