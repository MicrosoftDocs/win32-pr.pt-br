---
description: Executa uma interpolação linear entre dois vetores 2D.
ms.assetid: f8e9e6be-9696-4a4a-a6c8-c021985decaa
title: Função D3DXVec2Lerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Lerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c93040b3ab4c27c937947bfe1bd50f439dd70e84c6b90fb3931f7055b94b0def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749606"
---
# <a name="d3dxvec2lerp-function"></a>Função D3DXVec2Lerp

Executa uma interpolação linear entre dois vetores 2D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2Lerp(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV1,
  _In_    const D3DXVECTOR2 *pV2,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parâmetro que interpola linearmente entre os vetores.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da interpolação linear.

## <a name="remarks"></a>Comentários

Essa função executa a interpolação linear com base na seguinte fórmula: V1 + s(V2-V1).

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec2Lerp** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
