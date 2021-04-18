---
description: Porcentagem de tempo de processamento de dados do sombreador.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: Estrutura de D3DDEVINFO_D3D9STAGETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781011"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a>\_Estrutura D3DDEVINFO D3D9STAGETIMINGS

Porcentagem de tempo de processamento de dados do sombreador.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**MemoryProcessingPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo no sombreador gasto em acessos à memória.

</dd> <dt>

**ComputationProcessingPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de processamento de tempo (movendo dados em registros ou fazendo operações matemáticas).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter um melhor desempenho, é recomendável uma carga equilibrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
