---
description: Função D3DXVec4CatmullRom (D3DX10Math.h) – executa uma interpolação Catmull-Rom, usando os vetores 4D especificados.
ms.assetid: e3a10989-e25e-46fa-b72e-bade936cacf1
title: Função D3DXVec4CatmullRom (D3DX10Math.h)
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
ms.openlocfilehash: 4d565d1e9b567ff0c3320d6e0ba6023a6c4917720a2a13f32f98164cb7632123
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990546"
---
# <a name="d3dxvec4catmullrom-function-d3dx10mathh"></a>Função D3DXVec4CatmullRom (D3DX10Math.h)

Executa uma Catmull-Rom, usando os vetores 4D especificados.

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para [**o D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV0* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*pV3* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para uma estrutura D3DXVECTOR4 de origem, um vetor de posição.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para uma estrutura D3DXVECTOR4 que é o resultado da interpolação Catmull-Rom dados.

## <a name="remarks"></a>Comentários

Considerando quatro pontos (p1, p2, p3, p4), encontre uma função Q(s) de forma que:


```
Q(s) is a cubic function. 
Q(s) interpolates between p2 and p3 as s ranges from 0 to 1. 
Q(s) is parallel to the line joining p1 to p3 when s is 0. 
Q(s) is parallel to the line joining p2 to p4 when s is 1. 
```



O Catmull-Rom spline pode ser derivado do spline hermite definindo:


```
v1 = p2
v2 = p3
t1 = (p3 - p1) / 2
t2 = (p4 - p2) / 2
```



em que:

v1 é o conteúdo de pV0.

v2 no conteúdo de pV1.

p3 é o conteúdo de pV2.

p4 é o conteúdo de pV3.

Usando a equação de spline hermite:


```
Q(s) = (2s3 - 3s2 + 1)v1 + (-2s3 + 3s2)v2 + (s3 - 2s2 + s)t1 + (s3 - s2)t2
```



e substituir por v1, v2, t1, t2 produz:


```
Q(s) = (2s3 - 3s2 + 1)p2 + (-2s3 + 3s2)p3 + (s3 - 2s2 + s)(p3 - p1) / 2 + (s3 - s2)(p4 - p2) / 2
```



Isso pode ser reorganizar como:


```
Q(s) = [(-s3 + 2s2 - s)p1 + (3s3 - 5s2 + 2)p2 + (-3s3 + 4s2 + s)p3 + (s3 - s2)p4] / 2
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
