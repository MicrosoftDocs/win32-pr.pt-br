---
description: Computa o produto de ponto de um plano e um vetor 3D. O parâmetro w do vetor é considerado como 0.
ms.assetid: 7aba1e94-6531-4c07-83b0-6100805e8bbd
title: Função D3DXPlaneDotNormal (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 28903fc8ce0073e4014ae6ce75df636222ce32f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785926"
---
# <a name="d3dxplanedotnormal-function"></a>Função D3DXPlaneDotNormal

Computa o produto de ponto de um plano e um vetor 3D. O parâmetro w do vetor é considerado como 0.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXPlaneDotNormal(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Ponteiro para uma estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O produto de ponto do plano e do vetor 3D.

## <a name="remarks"></a>Comentários

Dado um plano (a, b, c, d) e um vetor 3D (x, y, z) o valor retornado dessa função é um \* x + b \* y + c \* z + d \* 0. A função **D3DXPlaneDotNormal** é útil para calcular o ângulo entre o normal do plano e outro normal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> </dl>

 

 
