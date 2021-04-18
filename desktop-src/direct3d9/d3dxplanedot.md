---
description: Computa o produto de ponto de um plano e um vetor 4D.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: Função D3DXPlaneDot (D3dx9math. h)
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
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793943"
---
# <a name="d3dxplanedot-function"></a>Função D3DXPlaneDot

Computa o produto de ponto de um plano e um vetor 4D.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
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

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O produto de ponto do plano e do vetor 4D.

## <a name="remarks"></a>Comentários

Dado um plano (a, b, c, d) e um vetor de 4D (x, y, z, w) o valor de retorno dessa função é um \* x + b \* y + c \* z + d \* w. A função **D3DXPlaneDot** é útil para determinar a relação do plano com uma coordenada homogênea. Por exemplo, essa função pode ser usada para determinar se uma coordenada específica está em um plano específico, ou em qual lado de um plano específico está em uma coordenada específica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
