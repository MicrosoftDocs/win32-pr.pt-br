---
description: Função D3DXMatrixDecompose (D3DX10Math.h) – divide uma matriz de transformação 3D geral em seus componentes escalares, rotacionais e translacionais.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: Função D3DXMatrixDecompose (D3DX10Math.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: be91b4b8ef6b0a18dc7691eb230ae755db31173ab8e42ab8ef0fb105d23630c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498136"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a>Função D3DXMatrixDecompose (D3DX10Math.h)

Divide uma matriz de transformação 3D geral em seus componentes escalares, rotacionais e translacionais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOutScale* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para a saída [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que contém fatores de dimensionamento aplicados ao longo dos eixos x, y e z.

</dd> <dt>

*pOutRotation* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para [**o D3DXQUATERNION**](d3d10-d3dxquaternion.md) que descreve a rotação.

</dd> <dt>

*pOutTranslation* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Ponteiro para o vetor D3DXVECTOR3 que descreve a tradução.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para uma matriz [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) entrada para decompor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
