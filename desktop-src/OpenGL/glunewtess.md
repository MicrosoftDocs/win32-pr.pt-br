---
title: função gluNewTess (Glu. h)
description: A função gluNewTess cria um objeto de mosaico.
ms.assetid: dfc9fce8-ecab-493b-85ee-6d7487814186
keywords:
- função gluNewTess OpenGL
topic_type:
- apiref
api_name:
- gluNewTess
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0573ead0cf9b81568c4bf2101e317bef7faf148
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755329"
---
# <a name="glunewtess-function"></a>função gluNewTess

A função **gluNewTess** cria um objeto de mosaico.

## <a name="syntax"></a>Sintaxe


```C++
GLUtesselator* WINAPI gluNewTess(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="remarks"></a>Comentários

A função **gluNewTess** cria e retorna um ponteiro para um novo objeto de mosaico. Consulte este objeto ao chamar funções de mosaico. Um valor de retorno igual a zero significa que não há memória suficiente para alocar para o objeto.

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

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





