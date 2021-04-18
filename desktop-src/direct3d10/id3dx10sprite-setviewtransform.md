---
description: Defina a transformação da exibição que se aplica a todos os sprites.
ms.assetid: 0420b141-46c7-4409-a0c4-67d1e8e02cd4
title: 'Método ID3DX10Sprite:: SetViewTransform (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.SetViewTransform
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 62ec2129d441acaa0719d2e64c02b4cc57370c8b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789275"
---
# <a name="id3dx10spritesetviewtransform-method"></a>Método ID3DX10Sprite:: SetViewTransform

Defina a transformação da exibição que se aplica a todos os sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetViewTransform(
  [in] D3DXMATRIX *pViewTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pViewTransform* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ponteiro para um D3DXMATRIX que contém uma transformação do sprite do espaço do mundo original. Use essa transformação para dimensionar, girar ou transformar o sprite.

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

 

 
