---
description: Contém dados para o relatório de pressão de memória.
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: Estrutura D3DMEMORYPRESSURE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5917d1e61817f401106ae14aa5a0f98cd75b0d42
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798480"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>Estrutura D3DMEMORYPRESSURE (D3d9types. h)

Contém dados para o relatório de pressão de memória.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>Membros

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

O número de bytes que foram removidos pelo processo durante a duração da consulta.

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

Tipo: **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

O número total de bytes colocados em segmentos de memória não ideais, devido a espaço inadequado dentro dos segmentos de memória preferenciais.

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

A eficiência geral das alocações de memória que foram colocadas na memória não ideal. O valor é expresso como uma porcentagem. Por exemplo, o valor 95 indica que as alocações colocadas em segmentos de memória não preferenciais são 95% eficiente. Esse número não deve ser considerado uma medida exata.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
