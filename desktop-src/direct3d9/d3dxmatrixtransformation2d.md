---
description: Função D3DXMatrixTransformation2D (D3dx9math. h) – compila uma matriz de transformação 2D que representa as transformações no plano XY. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 671d3d67-b474-4fc1-9913-d21f05d66d9a
title: Função D3DXMatrixTransformation2D (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation2D
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 754ea3124f5c2433e459331d4ebc7727a9c2519a982d1def09c7e16e794e6ae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750096"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx9mathh"></a>Função D3DXMatrixTransformation2D (D3dx9math. h)

Cria uma matriz de transformação 2D que representa as transformações no plano XY. Argumentos **nulos** são tratados como transformações de identidade.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       pScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que contém o resultado das transformações.

</dd> <dt>

*pScalingCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica o centro de dimensionamento. Se esse argumento for **nulo**, uma matriz <sub>SC</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*pScalingRotation* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O fator de rotação de dimensionamento.

</dd> <dt>

*pScaling* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica a escala. Se esse argumento for **nulo**, uma matriz MS de identidade será aplicada à fórmula em comentários.

</dd> <dt>

*pRotationCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , um ponto que identifica o centro de rotação. Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*Rotação* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

O ângulo de rotação em radianos.

</dd> <dt>

*pTranslation* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2**](d3dxvector2.md) , identificando a tradução. Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que contém a matriz de transformação.

## <a name="remarks"></a>Comentários

Essa função calcula a matriz de transformação com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

em que:

M <sub>out</sub> = matriz de saída (*pout*)

M <sub>SC</sub> = matriz do centro de dimensionamento (*pScalingCenter*)

M <sub>Sr</sub> = matriz de rotação de escala (*pScalingRotation*)

MS = matriz de dimensionamento (*pScaling*)

M <sub>RC</sub> = centro da matriz de rotação (*pRotationCenter*)

M <sub>r</sub> = matriz de rotação (*rotação*)

MT = matriz de conversão (*pTranslation*)

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função **D3DXMatrixTransformation2D** pode ser usada como um parâmetro para outra função.

Para transformações 3D, use [**D3DXMatrixTransformation**](d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixAffineTransformation2D**](d3dxmatrixaffinetransformation2d.md)
</dt> <dt>

[Transformações (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
