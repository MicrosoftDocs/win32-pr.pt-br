---
description: Porcentagem de tempo de processamento de dados no pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4d938fd2e1ca0f52d2ea7787f54b430a84907ad5f04f066bc90f0867825745a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676736"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>Estrutura D3DDEVINFO \_ D3D9PIPELINETIMINGS

Porcentagem de tempo de processamento de dados no pipeline.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**VertexProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo gasto executando sombreadores de vértice.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo gasto executando sombreadores de pixel.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo gasto fazendo outro processamento.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo para não processar nada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para melhorar o desempenho, recomenda-se uma carga balanceada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
