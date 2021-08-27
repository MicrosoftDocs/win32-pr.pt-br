---
description: Função D3DXQuaternionSquad (D3DX10Math.h) – interpola entre quaterões, usando interpolação quadrática esférica.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: Função D3DXQuaternionSquad (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: acd1c3e816d8f5a88b266a71e7579227be2def3452fbc25307fb4fa899ecacb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070016"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a>Função D3DXQuaternionSquad (D3DX10Math.h)

Interpola entre quaternões, usando interpolação quadrática esférica.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para [**o D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*pA* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*pB* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*pC* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*t* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parâmetro que indica até que ponto interpolar entre os quaterões.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para uma estrutura D3DXQUATERNION que é o resultado da interpolação quadrática esférica.

## <a name="remarks"></a>Comentários

Essa função usa a seguinte sequência de operações de interpolação linear esférica:


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXQuaternionSquad pode ser usada como um parâmetro para outra função.

Use [**D3DXQuaternionNormalize para**](d3d10-d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
