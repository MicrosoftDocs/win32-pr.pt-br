---
description: Função D3DXMatrixTransformation2D (D3DX10Math.h) – cria uma matriz de transformação 2D que representa transformações no plano xy. Os argumentos NULL são tratados como transformações de identidade.
ms.assetid: 5b894c3b-a532-458a-bcbc-48fcd5c73c34
title: Função D3DXMatrixTransformation2D (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 754e755b0ee6e03692bf7eabeb4e751284478621f47c912d399eb101adfd98e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754286"
---
# <a name="d3dxmatrixtransformation2d-function-d3dx10mathh"></a>Função D3DXMatrixTransformation2D (D3DX10Math.h)

Cria uma matriz de transformação 2D que representa transformações no plano xy. **Os argumentos NULL** são tratados como transformações de identidade.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixTransformation2D(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR2 *pScalingCenter,
  _In_          FLOAT       ScalingRotation,
  _In_    const D3DXVECTOR2 *pScaling,
  _In_    const D3DXVECTOR2 *pRotationCenter,
  _In_          FLOAT       Rotation,
  _In_    const D3DXVECTOR2 *pTranslation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a [**estrutura D3DXMATRIX**](d3d10-d3dxmatrix.md) que contém o resultado das transformações.

</dd> <dt>

*pScalingCenter* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Ponteiro para um [**D3DXVECTOR2**](d3d10-d3dxvector2.md), um ponto que identifica o centro de dimensionamento. Se esse argumento for **NULL,** uma matriz M <sub>sc</sub> de identidade será aplicada à fórmula em Comentários.

</dd> <dt>

*ScalingRotation* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ponteiro para o fator de rotação de dimensionamento.

</dd> <dt>

*pScaling* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Ponteiro para uma estrutura D3DXVECTOR2, um ponto que identifica a escala. Se esse argumento for **NULL,** uma matriz Ms de identidade será aplicada à fórmula em Comentários.

</dd> <dt>

*pRotationCenter* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Ponteiro para uma estrutura D3DXVECTOR2, um ponto que identifica o centro de rotação. Se esse argumento for **NULL,** uma matriz M <sub>rc</sub> de identidade será aplicada à fórmula em Comentários.

</dd> <dt>

*Rotação* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

O ângulo de rotação em radianos.

</dd> <dt>

*pTranslation* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***

Ponteiro para uma estrutura D3DXVECTOR2, identificando a tradução. Se esse argumento for **NULL,** uma matriz Mt de identidade será aplicada à fórmula em Comentários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que contém a matriz de transformação.

## <a name="remarks"></a>Comentários

Essa função calcula a matriz de transformação com a seguinte fórmula, com a concatenação de matriz avaliada na ordem da esquerda para a direita:

M<sub>out</sub> = (M<sub>sc</sub>)⁻Cada \* (M<sub>sr</sub>)⁻ \* Ms M \* <sub>sr</sub> \* M<sub>sc</sub> \* (M<sub>rc</sub>)⁻Cada M \* <sub>r</sub> M \* <sub>rc</sub> \* Mt

em que:

M<sub>out</sub> = matriz de saída (pOut)

M<sub>sc</sub> = matriz do centro de dimensionamento (pScalingCenter)

M<sub>sr</sub> = matriz de rotação de dimensionamento (pScalingRotation)

Ms = matriz de dimensionamento (pScaling)

M<sub>rc</sub> = centro da matriz de rotação (pRotationCenter)

M<sub>r</sub> = matriz de rotação (Rotação)

Mt = matriz de tradução (pTranslation)

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixTransformation2D pode ser usada como um parâmetro para outra função.

Para transformações 3D, use [**D3DXMatrixTransformation**](d3d10-d3dxmatrixtransformation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
