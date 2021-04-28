---
description: 'Método ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h) – determina o produto da matriz e da matriz atual.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'Método ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107944"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a>Método ID3DXMATRIXStack:: MultMatrixLocal (D3DX10. h)

Determina o produto da matriz e da matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura D3DXMATRIX a ser multiplicado com a matriz atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método multiplica a matriz específica à matriz atual (a transformação é sobre a origem local do objeto).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Esse método não adiciona um item à pilha, ele substitui a matriz atual pelo produto da matriz especificada e a matriz atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
