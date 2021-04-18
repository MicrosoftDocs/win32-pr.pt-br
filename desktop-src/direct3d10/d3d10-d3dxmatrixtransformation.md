---
description: Cria uma matriz de transformação. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 99c75ce9-3683-4753-b635-760eb8aaf46e
title: Função D3DXMatrixTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: db1d88ad04e4aaa51232cfdba3168779805b22c3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812403"
---
# <a name="d3dxmatrixtransformation-function-d3dx10mathh"></a>Função D3DXMatrixTransformation (D3DX10Math. h)

Cria uma matriz de transformação. Argumentos **nulos** são tratados como transformações de identidade.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixTransformation(
  _Inout_       D3DXMATRIX     *pOut,
  _In_    const D3DXVECTOR3    *pScalingCenter,
  _In_    const D3DXQUATERNION *pScalingRotation,
  _In_    const D3DXVECTOR3    *pScaling,
  _In_    const D3DXVECTOR3    *pRotationCenter,
  _In_    const D3DXQUATERNION *pRotation,
  _In_    const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*pScalingCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), identificando o ponto central de dimensionamento. Se esse argumento for **nulo**, uma matriz <sub>SC</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*pScalingRotation* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para um [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica a rotação de escala. Se esse argumento for **nulo**, uma matriz <sub>Sr</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*pScaling* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3, o vetor de dimensionamento. Se esse argumento for **nulo**, uma matriz MS de identidade será aplicada à fórmula em comentários.

</dd> <dt>

*pRotationCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3, um ponto que identifica o centro da rotação. Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*protação* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION que especifica a rotação. Se esse argumento for **nulo**, uma matriz <sub>r</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*pTranslation* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3, representando a tradução. Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que é a matriz de transformação.

## <a name="remarks"></a>Comentários

Essa função calcula a matriz de transformação com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:

M<sub>out</sub> = (m<sub>SC</sub>) ⁻ ¹ \* (m<sub>Sr</sub>) ⁻ ¹ \* MS \* m<sub>Sr</sub> \* m<sub>SC</sub> \* (m<sub>RC</sub>) ⁻ ¹ \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

onde:

M<sub>out</sub> = matriz de saída (pout)

M<sub>SC</sub> = matriz do centro de dimensionamento (pScalingCenter)

M<sub>Sr</sub> = matriz de rotação de escala (pScalingRotation)

MS = matriz de dimensionamento (pScaling)

M<sub>RC</sub> = centro da matriz de rotação (pRotationCenter)

M<sub>r</sub> = matriz de rotação (protação)

MT = matriz de conversão (pTranslation)

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixTransformation pode ser usada como um parâmetro para outra função.

Para transformações 2D, use [**D3DXMatrixTransformation2D**](d3d10-d3dxmatrixtransformation2d.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
