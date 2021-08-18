---
description: Função D3DXQuaternionSlerp (D3DX10Math.h) – interpola entre dois quatérnions, usando interpolação linear esférica.
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: Função D3DXQuaternionSlerp (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eca33eeb67f0c527efe7d0db8b8f17fe901d29dcbe3f2ef3b493463e01d34661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990966"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a>Função D3DXQuaternionSlerp (D3DX10Math.h)

Interpola entre dois quatérnios usando interpolação linear esférica.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
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

*pQ2* \[ Em\]
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

Ponteiro para uma estrutura D3DXQUATERNION que é o resultado da interpolação.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXQuaternionSlerp pode ser usada como um parâmetro para outra função.

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

 

 
