---
description: Estatísticas de uso de recursos.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Estrutura de D3DDEVINFO_RESOURCEMANAGER (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_RESOURCEMANAGER
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d45d920383e9ed95a9fe50f2ce87bd6cf26d040d45aecc9e7891a5c08f4232cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850276"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>\_Estrutura de RESOURCEMANAGER D3DDEVINFO

Estatísticas de uso de recursos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DDEVINFO_RESOURCEMANAGER {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_RESOURCEMANAGER, *LPD3DDEVINFO_RESOURCEMANAGER;

```



## <a name="members"></a>Membros

<dl> <dt>

**stats**
</dt> <dd>

Tipo: **[ **D3DRESOURCESTATS**](d3dresourcestats.md)**

</dd> <dd>

Matriz de elementos de estatísticas de recursos. Consulte [**D3DRESOURCESTATS**](d3dresourcestats.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

D3DRTYPECOUNT refere-se ao número de enumerações em [**D3DRESOURCETYPE**](./d3dresourcetype.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
