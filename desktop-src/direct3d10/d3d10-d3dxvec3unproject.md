---
description: Função D3DXVec3Unproject (D3DX10Math.h) – projeta um vetor do espaço da tela no espaço do objeto.
ms.assetid: c96d732d-0594-42b4-bc54-458a313f153e
title: Função D3DXVec3Unproject (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Unproject
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 14f8bb3d75d1a949919d401babb47987fbb88a7cac82f017947f069df4b99e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497857"
---
# <a name="d3dxvec3unproject-function-d3dx10mathh"></a>Função D3DXVec3Unproject (D3DX10Math.h)

Projeta um vetor do espaço da tela no espaço do objeto.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3Unproject(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para [**o D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para a estrutura D3DXVECTOR3 de origem.

</dd> <dt>

*pViewport* \[ Em\]
</dt> <dd>

Tipo: **const [**D3D10 \_ VIEWPORT**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) \***

Ponteiro para um [**\_ VIEWPORT D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o viewport.

</dd> <dt>

*pProjection* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3d10-d3dxmatrix.md) representando a matriz de projeção.

</dd> <dt>

*pView* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.

</dd> <dt>

*pWorld* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura D3DXVECTOR3 que é o vetor projetado do espaço da tela para o espaço do objeto.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXVec3Unproject pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
