---
description: Obtenha a matriz de projeção Sprite que é aplicada a todos os sprites.
ms.assetid: aee65a9f-27f9-42d9-98eb-ae90fc18c7f5
title: 'Método ID3DX10Sprite:: GetProjectionTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetProjectionTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eefd526fbe32158505db1edc73b9bbf527ad99be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664116"
---
# <a name="id3dx10spritegetprojectiontransform-method"></a>Método ID3DX10Sprite:: GetProjectionTransform

Obtenha a matriz de projeção Sprite que é aplicada a todos os sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetProjectionTransform(
  [out] D3DXMATRIX *pProjectionTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pProjectionTransform* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para um [**D3DX10MATRIX**](d3d10-d3dxmatrix.md) que será definido como a matriz de projeção do Sprite.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).

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

 

 
