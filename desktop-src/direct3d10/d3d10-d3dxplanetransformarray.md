---
description: Transforma uma matriz de planos por uma matriz. Os vetores que descrevem cada plano devem ser normalizados.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Função D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012134"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>Função D3DXPlaneTransformArray (D3DX10Math. h)

Transforma uma matriz de planos por uma matriz. Os vetores que descrevem cada plano devem ser normalizados.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para a estrutura [**D3DXPLANE**](d3d10-d3dxplane.md) que contém o plano transformado resultante. Consulte o exemplo.

</dd> <dt>

*Didistância* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O stride de cada plano transformado.

</dd> <dt>

*PP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ponteiro para a estrutura D3DXPLANE de entrada, que contém a matriz de planos para transformar. O vetor (a, b, c) que descreve o plano deve ser normalizado antes que essa função seja chamada. Consulte o exemplo.

</dd> <dt>

*PStride* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O stride de cada plano não transformado.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem, que contém a transpoção inversa dos valores de transformação.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de planos para transformar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para uma estrutura D3DXPLANE, representando o plano transformado. Esse é o mesmo valor retornado no parâmetro pOut para que essa função possa ser usada como um parâmetro para outra função.

## <a name="remarks"></a>Comentários

Este exemplo transforma um plano aplicando uma escala não uniforme.


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



Um plano é descrito por ax + by + cz + DW = 0. O primeiro plano é criado com (a, b, c, d) = (0, 1, 1, 0), que é um plano descrito por y + z = 0. Após o dimensionamento, o novo plano contém (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que mostra o novo plano a ser descrito por 0.353 y + 0.235 z = 0.

O parâmetro pM contém a transpoção inversa da matriz de transformação. A Transpose inversa é exigida por esse método para que o vetor normal do plano transformado também possa ser transformado corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
