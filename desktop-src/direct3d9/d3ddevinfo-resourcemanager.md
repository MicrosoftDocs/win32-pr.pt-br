---
description: Estatísticas de uso de recursos.
ms.assetid: e43de550-2025-4210-a420-e41d14620704
title: Estrutura de D3DDEVINFO_ResourceManager (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_ResourceManager
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bf4e84fa247ca5b2603547efef73ea6b9cbe0aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663978"
---
# <a name="d3ddevinfo_resourcemanager-structure"></a>\_Estrutura de RESOURCEMANAGER D3DDEVINFO

Estatísticas de uso de recursos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_ResourceManager {
  D3DRESOURCESTATS stats[D3DRTYPECOUNT];
} D3DDEVINFO_ResourceManager, *LPD3DDEVINFO_ResourceManager;
```



## <a name="members"></a>Membros

<dl> <dt>

**Estatísticas**
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

 

 
