---
description: Função D3DXPlaneTransformArray (D3DX10Math.h) – transforma uma matriz de planos por uma matriz. Os vetores que descrevem cada plano devem ser normalizados.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Função D3DXPlaneTransformArray (D3DX10Math.h)
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
ms.openlocfilehash: 04cda233d777f05dec44b4fc93537cc33b0369d14d95c104773f0f33ef03498d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070036"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a>Função D3DXPlaneTransformArray (D3DX10Math.h)

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

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para a [**estrutura D3DXPLANE**](d3d10-d3dxplane.md) que contém o plano transformado resultante. Consulte Exemplo.

</dd> <dt>

*OutStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O passo de cada plano transformado.

</dd> <dt>

*pP* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ponteiro para a estrutura D3DXPLANE de entrada, que contém a matriz de planos a transformar. O vetor (a, b, c) que descreve o plano deve ser normalizado antes que essa função seja chamada. Consulte Exemplo.

</dd> <dt>

*PStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O passo de cada plano não transformado.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origem, que contém a transposição inversa dos valores de transformação.

</dd> <dt>

*n* \[ em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de planos a transformar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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



Um plano é descrito por ax + por + cz + dw = 0. O primeiro plano é criado com (a,b,c,d) = (0,1,1,0), que é um plano descrito por y + z = 0. Após o dimensionamento, o novo plano conterá (a,b,c,d) = (0, 0,353f, 0,235f, 0), que mostra o novo plano a ser descrito por 0,353y + 0,235z = 0.

O parâmetro pM contém a transposição inversa da matriz de transformação. A transposição inversa é exigida por esse método para que o vetor normal do plano transformado também possa ser transformado corretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
