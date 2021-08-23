---
description: Subtrai dois vetores 4D.
ms.assetid: 3bc55b38-818e-40eb-859e-495ee28fc4ae
title: Função D3DXVec4Subtract (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Subtract
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f49299eab666f92b401bb3fee5ac0c828d607a38893f6bfe4a58e826f84b7493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607566"
---
# <a name="d3dxvec4subtract-function"></a>Função D3DXVec4Subtract

Subtrai dois vetores 4D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4Subtract(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem.

</dd> <dt>

*pV2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura [**D3DXVECTOR4 de**](d3dxvector4.md) origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR4**](d3dxvector4.md) que é a diferença de dois vetores.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec4Subtract** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec3Add**](d3dxvec3add.md)
</dt> <dt>

[**D3DXVec3Scale**](d3dxvec3scale.md)
</dt> </dl>

 

 




