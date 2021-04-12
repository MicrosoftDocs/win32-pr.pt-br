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
ms.openlocfilehash: 7a448346bdc5dcfbbca4cf0d55273bdadc2fdcbb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298666"
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

 

 
