---
description: Função D3DXVec3Project (D3dx9math.h) – projeta um vetor 3D do espaço do objeto no espaço da tela.
ms.assetid: b012771d-052f-4bf9-b39c-387d8a63fa59
title: Função D3DXVec3Project (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Project
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1bb0d7b962dd4595ec9246c036d4ff9e459e062f366b6e62f46cce1a5a3ebab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803808"
---
# <a name="d3dxvec3project-function-d3dx9mathh"></a>Função D3DXVec3Project (D3dx9math.h)

Projeta um vetor 3D do espaço do objeto no espaço da tela.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR3* D3DXVec3Project(
  _Inout_       D3DXVECTOR3  *pOut,
  _In_    const D3DXVECTOR3  *pV,
  _In_    const D3DVIEWPORT9 *pViewport,
  _In_    const D3DXMATRIX   *pProjection,
  _In_    const D3DXMATRIX   *pView,
  _In_    const D3DXMATRIX   *pWorld
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para a [**estrutura D3DXVECTOR3**](d3dxvector3.md) que é o resultado da operação.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a estrutura [**D3DXVECTOR3 de**](d3dxvector3.md) origem.

</dd> <dt>

*pViewport* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DVIEWPORT9**](d3dviewport9.md) \***

Ponteiro para uma [**estrutura D3DVIEWPORT9,**](d3dviewport9.md) representando o viewport.

</dd> <dt>

*pProjection* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3dxmatrix.md) representando a matriz de projeção.

</dd> <dt>

*pView* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3dxmatrix.md) representando a matriz de exibição.

</dd> <dt>

*pWorld* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para uma [**estrutura D3DXMATRIX,**](d3dxmatrix.md) representando a matriz mundial.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR3**](d3dxvector3.md) que é o vetor projetado do espaço do objeto para o espaço da tela.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec3Project** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Unproject**](d3dxvec3unproject.md)
</dt> </dl>

 

 




