---
description: Métricas de taxa de transferência para ajudar a entender o desempenho de um aplicativo.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS estrutura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f9c92a3eae10ef289e53764c7568f826640edf66c3351edaadf3d922515a3eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565026"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>Estrutura D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS

Métricas de taxa de transferência para ajudar a entender o desempenho de um aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

A largura de banda ou a taxa máxima de transferência de dados da CPU do host para a GPU. Normalmente, essa é a largura de banda do barramento PCI ou AGP que conecta a CPU e a GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem utilizada pela memória ao carregar dados da CPU do host para a GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentual de taxa de transferência de vértice. Esse é o número de vértices processados em comparação com a taxa máxima de processamento de vértice teórico.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentual de taxa de transferência de configuração de triângulo. Esse é o número de triângulos que são definidos para rasterização em comparação com a taxa de configuração máxima de triângulo teórico.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentual de taxa de transferência de preenchimento de pixel. Esse é o número de pixels que são preenchidos em comparação com o preenchimento de pixel teórico.

</dd> </dl>

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

 

 
