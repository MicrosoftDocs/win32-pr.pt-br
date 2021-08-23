---
description: Calcula o produto de ponto de um plano e um vetor 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Função D3DXPlaneDot (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4895a94ad50171682a8bd5247694c3b35a56d174b5477f5bbb2a621c1e74fa96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564626"
---
# <a name="d3dxplanedot-function"></a>Função D3DXPlaneDot

Calcula o produto de ponto de um plano e um vetor 4D.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
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

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR4.**](d3dxvector4.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O produto de ponto do plano e o vetor 4D.

## <a name="remarks"></a>Comentários

Dado um plano (a, b, c, d) e um vetor 4D (x, y, z, w) o valor de retorno dessa função é \* x + b y + c z + d \* \* \* w. A **função D3DXPlaneDot** é útil para determinar a relação do plano com uma coordenada homogênea. Por exemplo, essa função pode ser usada para determinar se uma coordenada específica está em um plano específico ou em qual lado de um plano específico está uma coordenada específica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
