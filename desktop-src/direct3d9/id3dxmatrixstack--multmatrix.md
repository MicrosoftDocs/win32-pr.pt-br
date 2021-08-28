---
description: 'Método ID3DXMATRIXStack:: MultMatrix (D3dx9math. h) – determina o produto da matriz atual e a matriz especificada.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'Método ID3DXMATRIXStack:: MultMatrix (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9d0808f1b23475b823ea43f55d93f8dacb01e4e491957fa34100110946fa72e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856456"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>Método ID3DXMATRIXStack:: MultMatrix (D3dx9math. h)

Determina o produto da matriz atual e a matriz especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMat* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) a ser multiplicado com a matriz atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método multiplica a matriz específica à matriz atual (a transformação é sobre a origem do mundo atual).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz atual e pela matriz especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




