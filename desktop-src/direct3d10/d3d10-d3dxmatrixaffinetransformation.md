---
description: Cria uma matriz de transformação afim 3D. Argumentos nulos são tratados como transformações de identidade.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Função D3DXMatrixAffineTransformation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixAffineTransformation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27fee5a620d75c3930b1bc2f8a85415db1320a47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781145"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>Função D3DXMatrixAffineTransformation (D3DX10Math. h)

Cria uma matriz de transformação afim 3D. Argumentos **nulos** são tratados como transformações de identidade.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixAffineTransformation(
  _In_       D3DXMATRIX     *pOut,
  _In_       FLOAT          Scaling,
  _In_ const D3DXVECTOR3    *pRotationCenter,
  _In_ const D3DXQUATERNION *pRotation,
  _In_ const D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*Dimensionamento* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de dimensionamento.

</dd> <dt>

*pRotationCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), um ponto que identifica o centro da rotação. Se esse argumento for **nulo**, uma matriz <sub>RC</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*protação* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para um [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica a rotação. Se esse argumento for **nulo**, uma matriz <sub>r</sub> de identidade M será aplicada à fórmula em comentários.

</dd> <dt>

*pTranslation* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3 que representa a tradução. Se esse argumento for **nulo**, uma matriz de identidade MT será aplicada à fórmula em comentários.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de transformação afim.

## <a name="remarks"></a>Comentários

Essa função calcula a matriz de transformação afim com a seguinte fórmula, com concatenação de matriz avaliada na ordem da esquerda para a direita:

M<sub>out</sub> = MS \* (M<sub>RC</sub>)-1 \* m<sub>r</sub> \* m<sub>RC</sub> \* MT

onde:

M<sub>out</sub> = matriz de saída (pout)

MS = matriz de dimensionamento (dimensionamento)

M<sub>RC</sub> = centro da matriz de rotação (pRotationCenter)

M<sub>r</sub> = matriz de rotação (protação)

MT = matriz de conversão (pTranslation)

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixAffineTransformation pode ser usada como um parâmetro para outra função.

Para transformações de afinidade 2D, use D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
