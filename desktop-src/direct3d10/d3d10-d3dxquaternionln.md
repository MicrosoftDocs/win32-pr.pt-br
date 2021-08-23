---
description: Função D3DXQuaternionLn (D3DX10Math.h) – calcula o logaritmo natural.
ms.assetid: 576cf676-bb42-45ec-8e45-4612a7cdb167
title: Função D3DXQuaternionLn (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionLn
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ec225648d5024951ca51e0533098fee897a66d6770d0c937c0d251842613a9b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991116"
---
# <a name="d3dxquaternionln-function-d3dx10mathh"></a>Função D3DXQuaternionLn (D3DX10Math.h)

Calcula o logaritmo natural.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionLn(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para [**o D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para a estrutura D3DXQUATERNION de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para uma estrutura D3DXQUATERNION que é o logaritmo natural.

## <a name="remarks"></a>Comentários

A função D3DXQuaternionLn funciona apenas para quaternões de unidade.


```
A unit quaternion, is defined by:
Q == (cos(theta), sin(theta) * v) where |v| = 1
The natural logarithm of Q is, ln(Q) = (0, theta * v)
```



O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXQuaternionLn pode ser usada como um parâmetro para outra função.

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

 

 
