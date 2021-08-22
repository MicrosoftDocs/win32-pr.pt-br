---
description: Método ID3DXMATRIXStack::MultMatrixLocal (D3dx9math.h) – determina o produto da matriz determinada e a matriz atual.
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: Método ID3DXMATRIXStack::MultMatrixLocal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08a50f6477be6106ce6eaf82c0111f805ed00472259283429e1f638579c91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120810"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a>Método ID3DXMATRIXStack::MultMatrixLocal (D3dx9math.h)

Determina o produto da matriz determinada e a matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMat* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a [**estrutura D3DXMATRIX**](d3dxmatrix.md) a ser multiplicada pela matriz atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método multiplica à esquerda a matriz determinada para a matriz atual (a transformação é sobre a origem local do objeto).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz determinada e a matriz atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




