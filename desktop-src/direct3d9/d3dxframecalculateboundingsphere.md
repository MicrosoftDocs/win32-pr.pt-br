---
description: Calcula a esfera delimitada de todas as malhas na hierarquia de quadros.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: Função D3DXFrameCalculateBoundingSphere (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a8a4706fcbd421072e2b82cd9e228fe24c35651c17ce4ab0f48e05b946946fb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123212"
---
# <a name="d3dxframecalculateboundingsphere-function"></a>Função D3DXFrameCalculateBoundingSphere

Calcula a esfera delimitada de todas as malhas na hierarquia de quadros.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFrameRoot* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***

Ponteiro para o nó raiz.

</dd> <dt>

*pObjectCenter* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**

Retorna o centro da esfera delimitada.

</dd> <dt>

*pObjectRadius* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Retorna o raio da esfera delimitada.

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

 

 
