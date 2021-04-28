---
description: 'ID3DXMATRIXStack: método op de:P (D3DX10. h) – remove a matriz atual da parte superior da pilha.'
ms.assetid: f4e4ff5d-a7a1-4f87-9b7e-53b9d044ba51
title: 'ID3DXMATRIXStack: método op de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Pop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19c87cbd5fd81100682225aa16256573c7f95be0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107924"
---
# <a name="id3dxmatrixstackpop-method-d3dx10h"></a>ID3DXMATRIXStack: método op de:P (D3DX10. h)

Remove a matriz atual da parte superior da pilha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Pop();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK.

## <a name="remarks"></a>Comentários

Observe que esse método diminui a contagem de itens na pilha em 1, removendo efetivamente a matriz atual da parte superior da pilha e promovendo uma matriz para a parte superior da pilha. Se a contagem atual de itens na pilha for 0, esse método retornará sem executar nenhuma ação. Se a contagem atual de itens na pilha for 1, esse método esvazia a pilha.

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

 

 




