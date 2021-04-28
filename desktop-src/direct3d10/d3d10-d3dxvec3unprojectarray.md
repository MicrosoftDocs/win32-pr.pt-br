---
description: Função D3DXVec3UnprojectArray (D3DX10Math. h)-projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.
ms.assetid: 02db5b32-7fa3-4cde-bd63-0d8b3dfc31e7
title: Função D3DXVec3UnprojectArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3UnprojectArray
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 727744445e952fa0135feff944c768aaba1aba36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103004"
---
# <a name="d3dxvec3unprojectarray-function-d3dx10mathh"></a>Função D3DXVec3UnprojectArray (D3DX10Math. h)

Projeta uma matriz (x, y, z, 0) do espaço da tela no espaço do objeto.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3UnprojectArray(
  _Inout_       D3DXVECTOR3    *pOut,
  _In_          UINT           OutStride,
  _In_    const D3DXVECTOR3    *pV,
  _In_          UINT           VStride,
  _In_    const D3D10_VIEWPORT *pViewport,
  _In_    const D3DXMATRIX     *pProjection,
  _In_    const D3DXMATRIX     *pView,
  _In_    const D3DXMATRIX     *pWorld,
  _In_          UINT           n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*Didistância* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride entre os vetores no fluxo de dados de saída.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para a estrutura de D3DXVECTOR3 de origem.

</dd> <dt>

*VStride* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Stride entre os vetores no fluxo de dados de entrada.

</dd> <dt>

*pViewport* \[ no\]
</dt> <dd>

Tipo: **\* [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport) const**

Ponteiro para um [**\_ visor d3d10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_viewport), que representa o visor.

</dd> <dt>

*pProjection* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , representando a matriz de projeção.

</dd> <dt>

*pView* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura D3DXMATRIX, representando a matriz de exibição.

</dd> <dt>

*pWorld* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma estrutura D3DXMATRIX, representando a matriz mundial.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para uma estrutura D3DXVECTOR3 que é a matriz projetada do espaço da tela para o espaço de objeto.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função [**D3DXVec3Unproject**](d3d10-d3dxvec3unproject.md) pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
