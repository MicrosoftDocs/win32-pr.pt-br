---
description: 'Método ID3DXBaseMesh:: GetVertexBuffer – recupera o buffer de vértice associado à malha.'
ms.assetid: 5caa6ce1-feab-4919-944e-f92fad3ad443
title: 'Método ID3DXBaseMesh:: GetVertexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bc0fc1f47ba3ed27af8f06d1a1f5ea83b884cdbe645d8597cd9513e7ad5c0387
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118846"
---
# <a name="id3dxbasemeshgetvertexbuffer-method"></a>Método ID3DXBaseMesh:: GetVertexBuffer

Recupera o buffer de vértice associado à malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVertexBuffer(
  [out, retval] LPDIRECT3DVERTEXBUFFER9 *ppVB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppVB* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)\***

Endereço de um ponteiro para uma interface [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) , que representa o objeto de buffer de vértice associado à malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
