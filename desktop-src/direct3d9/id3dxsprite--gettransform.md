---
description: Obtém a transformação de Sprite.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'Método ID3DXSprite:: GetTransform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012116"
---
# <a name="id3dxspritegettransform-method"></a>Método ID3DXSprite:: GetTransform

Obtém a transformação de Sprite.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTransform* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do sprite do espaço do mundo original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




