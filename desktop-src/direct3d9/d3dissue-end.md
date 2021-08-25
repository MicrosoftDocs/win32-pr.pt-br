---
description: Essa macro cria um valor usado pelo problema para emitir uma extremidade de consulta.
ms.assetid: 9ced932a-5d98-4bf8-aa11-06560f53546d
title: D3DISSUE_END (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DISSUE_END
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: 0c2e7a197612b56eb5ae966da3cd4cc224edd2bd07e3fded3d0b72907f717d5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987246"
---
# <a name="d3dissue_end"></a>D3DISSUE \_ fim

Essa macro cria um valor usado pelo [**problema**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue) para emitir uma extremidade de consulta.

``` syntax
#define D3DISSUE_END (1 << 0)
```

## <a name="parameters"></a>Parâmetros





 

## <a name="remarks"></a>Comentários

Essa macro altera o estado da consulta para não sinalizado.

\_O D3DISSUE end é válido para os seguintes tipos de consulta.

-   D3DQUERYTYPE \_ VCACHE
-   \_RESOURCEMANAGER D3DQUERYTYPE
-   D3DQUERYTYPE \_ VERTEXSTATS
-   \_Evento D3DQUERYTYPE
-   D3DQUERYTYPE \_ oclusão

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**Início do D3DISSUE \_**](d3dissue-begin.md)
</dt> <dt>

[**D3DQUERYTYPE**](./d3dquerytype.md)
</dt> </dl>

 

 
