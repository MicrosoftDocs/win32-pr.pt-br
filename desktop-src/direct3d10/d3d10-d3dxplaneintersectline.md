---
description: Localiza a interseção entre um plano e uma linha.
ms.assetid: aea1c4e1-f8c0-46df-bb33-2b517396d69e
title: Função D3DXPlaneIntersectLine (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 00d25fcba9e5884cec10da96964ad0f5daa9ed14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802123"
---
# <a name="d3dxplaneintersectline-function-d3dx10mathh"></a>Função D3DXPlaneIntersectLine (D3DX10Math. h)

Localiza a interseção entre um plano e uma linha.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identificando a interseção entre o plano e a linha especificados.

</dd> <dt>

*PP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md)de origem.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura de D3DXVECTOR3 de origem, definindo um ponto de partida de linha.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura de D3DXVECTOR3 de origem, definindo um ponto de extremidade de linha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura D3DXVECTOR3 que é a interseção entre o plano e a linha especificados.

## <a name="remarks"></a>Comentários

Se a linha for paralela ao plano, **NULL** será retornado.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXPlaneIntersectLine pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
