---
description: Executa uma interpolação de Catmull-Rom, usando os vetores de 4D especificados.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: Função D3DXVec4CatmullRom (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4CatmullRom
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 8e027272a038f17a77dbeda861d6be909afa2f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930567"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a>Função D3DXVec4CatmullRom (D3DX10Math. h)

Executa uma interpolação de Catmull-Rom, usando os vetores de 4D especificados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4CatmullRom(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV0,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2,
  _In_    const D3DXVECTOR4 *pV3,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para o [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV0* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura de D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura de D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura de D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*pV3* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura de D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para uma estrutura D3DXVECTOR4 que é o resultado da interpolação de Catmull-Rom.

## <a name="remarks"></a>Comentários

Considerando quatro pontos (P1, P2, P3, P4), encontre uma função Q (s) de modo que:


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



O Catmull-Rom spline pode ser derivado do spline Hermite por meio da configuração:


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



onde:

v1 é o conteúdo de pV0.

V2 no conteúdo de pV1.

P3 é o conteúdo de pV2.

P4 é o conteúdo de pV3.

Usando a equação de spline Hermite:


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



e a substituição para v1, v2, T1, T2 produz:


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



Isso pode ser reorganizado como:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
