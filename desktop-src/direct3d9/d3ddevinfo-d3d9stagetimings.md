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
ms.openlocfilehash: eb4302b86d31c074f58fd003601557864aee152da9e532771336097f4228ea61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676726"
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

 

 
