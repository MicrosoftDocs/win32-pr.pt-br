---
description: Calcula o produto de ponto de um plano e um vetor 3D. O parâmetro w do vetor é presumido como 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Função D3DXPlaneDotCoord (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30f04ec310ce66dc43073e724b08c358cd8fc6f24f0b3840475a1abc61544503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524923"
---
# <a name="d3dxplanedotcoord-function"></a>Função D3DXPlaneDotCoord

Calcula o produto de ponto de um plano e um vetor 3D. O parâmetro w do vetor é presumido como 1.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pP* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Ponteiro para uma estrutura [**D3DXPLANE de origem.**](d3dxplane.md)

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O produto de ponto do plano e o vetor 3D.

## <a name="remarks"></a>Comentários

Dado um plano (a, b, c, d) e um vetor 3D (x, y, z), o valor de retorno dessa função é \* x + b y + c z + d \* \* \* 1. A **função D3DXPlaneDotCoord** é útil para determinar a relação do plano com uma coordenada no espaço 3D.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
