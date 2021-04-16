---
description: Localiza o quadro filho de um quadro raiz.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: Função D3DXFrameFind (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764998"
---
# <a name="d3dxframefind-function"></a>Função D3DXFrameFind

Localiza o quadro filho de um quadro raiz.

## <a name="syntax"></a>Sintaxe


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrameRoot* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Ponteiro para o quadro raiz. Consulte [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*Nome* \[ do no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do quadro filho a ser localizado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

Retorna o quadro filho se ele for encontrado ou **NULL** caso contrário. Consulte [**D3DXFRAME**](d3dxframe.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
