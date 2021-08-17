---
description: Método ID3DXMATRIXStack::MultMatrix (D3DX10.h) – determina o produto da matriz atual e a matriz determinada.
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: Método ID3DXMATRIXStack::MultMatrix (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f881e3df820df87ea948893277950bce3ca289b8f9e0dcc6a4d34d46cca463ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736074"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a>Método ID3DXMATRIXStack::MultMatrix (D3DX10.h)

Determina o produto da matriz atual e a matriz determinada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura D3DXMATRIX a ser multiplicada pela matriz atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método multiplica com o direito a matriz determinada para a matriz atual (a transformação é sobre a origem do mundo atual).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz atual e pela matriz determinada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
