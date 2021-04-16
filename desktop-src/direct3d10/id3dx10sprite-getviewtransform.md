---
description: Obter a transformação de exibição que se aplica a todos os sprites.
ms.assetid: eba45c08-64cc-4119-83d4-50351fe21bea
title: 'Método ID3DX10Sprite:: GetViewTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 699a46e48545d58058fb1f2db2955b4a4f403a53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761618"
---
# <a name="id3dx10spritegetviewtransform-method"></a>Método ID3DX10Sprite:: GetViewTransform

Obter a transformação de exibição que se aplica a todos os sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetViewTransform(
  [out] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pViewTransform* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para um [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que será definido como a transformação do sprite do espaço do mundo original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
