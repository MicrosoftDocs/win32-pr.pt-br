---
description: Dada uma hierarquia de quadros, registra todas as matrizes nomeadas no mixer de animação.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: Função D3DXFrameRegisterNamedMatrices (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a98d70bbb9c112c5edabaa6b4c4c9d0cb26e0349d72d17ed9ea48226f4cc032e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731716"
---
# <a name="d3dxframeregisternamedmatrices-function"></a>Função D3DXFrameRegisterNamedMatrices

Dada uma hierarquia de quadros, registra todas as matrizes nomeadas no mixer de animação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrameRoot* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**

O nó de nível superior na hierarquia de quadros.

</dd> <dt>

*pAnimController* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Ponteiro para o objeto do controlador de animação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de animação](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




