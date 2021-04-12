---
description: Métricas de taxa de transferência para ajudar na compreensão do desempenho de um aplicativo.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Estrutura de D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
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
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172961"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>\_Estrutura D3DDEVINFO D3D9BANDWIDTHTIMINGS

Métricas de taxa de transferência para ajudar na compreensão do desempenho de um aplicativo.

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

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

A largura de banda ou a taxa máxima de transferência de dados da CPU do host para a GPU. Normalmente, essa é a largura de banda do barramento PCI ou AGP que conecta a CPU e a GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Percentual de utilização de memória ao carregar dados da CPU do host para a GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de produtividade do vértice. Este é o número de vértices processados em comparação com a taxa de processamento de vértice máximo teórica.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de taxa de transferência de configuração de triângulo. Este é o número de triângulos que são configurados para rasterização em comparação com a taxa de configuração de triângulo máximo teórica.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentagem de produtividade de preenchimento de pixel. Este é o número de pixels que são preenchidos em comparação com o preenchimento de pixel teórico.

</dd> </dl>

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

 

 
