---
description: Função D3DXPlaneFromPoints (D3dx9math.h) – constrói um plano de três pontos.
ms.assetid: 13d5ce6b-0046-441b-b826-f34f4fe16979
title: Função D3DXPlaneFromPoints (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPoints
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 313273ab791fe63fa85440a5bfe3fdffe41726f15c2d6a8d0343408fdf7d67f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524933"
---
# <a name="d3dxplanefrompoints-function-d3dx9mathh"></a>Função D3DXPlaneFromPoints (D3dx9math.h)

Constrói um plano de três pontos.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneFromPoints(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2,
  _In_    const D3DXVECTOR3 *pV3
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para a [**estrutura D3DXPLANE**](d3dxplane.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) definindo um dos pontos usados para construir o plano.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) definindo um dos pontos usados para construir o plano.

</dd> <dt>

*pV3* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) definindo um dos pontos usados para construir o plano.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para a [**estrutura D3DXPLANE**](d3dxplane.md) construída a partir dos pontos determinados.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXPlaneFromPoints** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneFromPointNormal**](d3dxplanefrompointnormal.md)
</dt> </dl>

 

 




