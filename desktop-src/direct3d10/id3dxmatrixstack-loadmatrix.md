---
description: 'Método ID3DXMATRIXStack:: loadmatrix (D3DX10. h) – carrega a matriz determinada na matriz atual.'
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'Método ID3DXMATRIXStack:: loadmatrix (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107954"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a>Método ID3DXMATRIXStack:: loadmatrix (D3DX10. h)

Carrega a matriz determinada na matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PM* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a estrutura D3DXMATRIX carregada na matriz atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Observe que esse método não adiciona um item à pilha; em vez disso, ele substitui a matriz atual pela matriz fornecida.

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

 

 
