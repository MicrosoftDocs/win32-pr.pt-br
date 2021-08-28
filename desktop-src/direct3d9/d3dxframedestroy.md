---
description: Destrói a subárvore de quadros sob a raiz, incluindo a raiz.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: Função D3DXFrameDestroy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e20e878b402ad0b8c4d0a9b721cd9300154305b2a06426564d1639ceddd7a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988476"
---
# <a name="d3dxframedestroy-function"></a>Função D3DXFrameDestroy

Destrói a subárvore de quadros sob a raiz, incluindo a raiz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrameRoot* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Ponteiro para o nó raiz.

</dd> <dt>

*pAlloc* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Interface de alocação usada para desalocar nós da hierarquia de quadros.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




