---
description: 'Método ID3DXBaseMesh:: GetIndexBuffer – recupera os dados em um buffer de índice.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: 'Método ID3DXBaseMesh:: GetIndexBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115424"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a>Método ID3DXBaseMesh:: GetIndexBuffer

Recupera os dados em um buffer de índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIB* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***

Endereço de um ponteiro para uma interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , representando o objeto de buffer de índice associado à malha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
