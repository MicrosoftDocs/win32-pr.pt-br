---
description: Função D3DXMatrixDecompose (D3dx9math. h) – divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: Função D3DXMatrixDecompose (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb6ce07713b4f66f4a85a678b5b28b589f8ae797c5a7b5c578ed136bbb9e3f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460386"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a>Função D3DXMatrixDecompose (D3dx9math. h)

Divide uma matriz de transformação 3D geral em seus componentes escalares, de rotação e de tradução.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOutScale* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para a saída [**D3DXVECTOR3**](d3dxvector3.md) que contém fatores de dimensionamento aplicados ao longo dos eixos x, y e z.

</dd> <dt>

*pOutRotation* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que descreve a rotação.

</dd> <dt>

*pOutTranslation* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para o vetor [**D3DXVECTOR3**](d3dxvector3.md) que descreve a tradução.

</dd> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma matriz [**D3DXMATRIX**](d3dxmatrix.md) de entrada para decompor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




