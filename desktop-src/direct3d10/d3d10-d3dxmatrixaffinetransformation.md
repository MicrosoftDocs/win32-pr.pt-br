---
description: Função D3DXMatrixAffineTransformation (D3DX10Math.h) – cria uma matriz de transformação de afinidade 3D. Os argumentos NULL são tratados como transformações de identidade.
ms.assetid: 36044272-a8ce-47db-8f52-30dc680f8174
title: Função D3DXMatrixAffineTransformation (D3DX10Math.h)
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
ms.openlocfilehash: 5c847d537eaa79b266ef785f40806c37e2503b2b9a8a97bf99a678c7dff219de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609516"
---
# <a name="d3dxmatrixaffinetransformation-function-d3dx10mathh"></a>Função D3DXMatrixAffineTransformation (D3DX10Math.h)

Cria uma matriz de transformação de afinidade 3D. **Os argumentos NULL** são tratados como transformações de identidade.

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

*pOut* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para [**o D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*Dimensionamento* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de dimensionamento.

</dd> <dt>

*pRotationCenter* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), um ponto que identifica o centro de rotação. Se esse argumento for **NULL,** uma matriz M <sub>rc</sub> de identidade será aplicada à fórmula em Comentários.

</dd> <dt>

*pRotation* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para um [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que especifica a rotação. Se esse argumento for **NULL,** uma matriz de identidade M <sub>r</sub> será aplicada à fórmula em Comentários.

</dd> <dt>

*pTranslation* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Ponteiro para uma estrutura D3DXVECTOR3 que representa a tradução. Se esse argumento for **NULL,** uma matriz Mt de identidade será aplicada à fórmula em Comentários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de transformação affine.

## <a name="remarks"></a>Comentários

Essa função calcula a matriz de transformação affine com a seguinte fórmula, com a concatenação de matriz avaliada na ordem da esquerda para a direita:

M<sub>out</sub> = Mₛ \* (M<sub>rc</sub>)-1 \* M<sub>r</sub> \* M<sub>rc</sub> \* Mₜ

em que:

M<sub>out</sub> = matriz de saída (pOut)

Ms = matriz de dimensionamento (dimensionamento)

M<sub>rc</sub> = centro da matriz de rotação (pRotationCenter)

M<sub>r</sub> = matriz de rotação (pRotation)

Mt = matriz de tradução (pTranslation)

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXMatrixAffineTransformation pode ser usada como um parâmetro para outra função.

Para transformações de afinidade 2D, use D3DXMatrixAffineTransformation2D.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
