---
description: Função D3DXQuaternionRotationMatrix (D3dx9math.h) – cria um quatternion de uma matriz de rotação.
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Função D3DXQuaternionRotationMatrix (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3ad57cc34a7b16b15c49195e39004094a33e2a168c7a3ff2f5f7eb77c267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988446"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a>Função D3DXQuaternionRotationMatrix (D3dx9math.h)

Cria um quatrion de uma matriz de rotação.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a [**estrutura D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pM* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Ponteiro para a estrutura [**D3DXMATRIX de origem.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a [**estrutura D3DXQUATERNION**](d3dxquaternion.md) criada de uma matriz de rotação.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXQuaternionRotationMatrix** pode ser usada como um parâmetro para outra função.

Use [**D3DXQuaternionNormalize para**](d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




