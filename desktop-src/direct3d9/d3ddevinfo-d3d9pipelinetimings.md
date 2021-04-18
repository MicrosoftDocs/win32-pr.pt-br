---
description: Porcentagem de tempo de processamento de dados no pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Estrutura de D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
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
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781012"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a>\_Estrutura D3DDEVINFO D3D9PIPELINETIMINGS

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo gasto na execução de sombreadores de vértice.

</dd> <dt>

**PixelProcessingTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo gasto na execução de sombreadores de pixel.

</dd> <dt>

**OtherGPUProcessingTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo gasto fazendo outro processamento.

</dd> <dt>

**GPUIdleTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de tempo não processando nada.

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

 

 
