---
description: Transforma um plano por uma matriz. A matriz de entrada é a transpoção inversa da transformação real.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Função D3DXPlaneTransform (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298768"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a>Função D3DXPlaneTransform (D3DX10Math. h)

Transforma um plano por uma matriz. A matriz de entrada é a transpoção inversa da transformação real.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md) que contém o plano transformado resultante. Confira o exemplo.

</dd> <dt>

*PP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ponteiro para a estrutura D3DXPLANE de entrada, que contém o plano que será transformado. O vetor (a, b, c) que descreve o plano deve ser normalizado antes que essa função seja chamada. Confira o exemplo.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem, que contém os valores de transformação. Essa matriz deve conter a transpoção inversa dos valores de transformação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para uma estrutura D3DXPLANE, representando o plano transformado. Esse é o mesmo valor retornado no parâmetro pOut para que essa função possa ser usada como um parâmetro para outra função.

## <a name="remarks"></a>Comentários

### <a name="examples"></a>Exemplos

Este exemplo transforma um plano aplicando uma escala não uniforme.


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
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

 

 
