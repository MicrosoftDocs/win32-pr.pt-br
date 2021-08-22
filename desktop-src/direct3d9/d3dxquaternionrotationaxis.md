---
description: Função D3DXQuaternionRotationAxis (D3dx9math.h) – gira um quatternion sobre um eixo arbitrário.
ms.assetid: 9ff0fe2c-54d6-482c-84e1-f38e3c57d8dd
title: Função D3DXQuaternionRotationAxis (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationAxis
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4879cec21f356399d2f98c7c3286da9ae3994c81fa64911177f287c9f0e216b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524598"
---
# <a name="d3dxquaternionrotationaxis-function-d3dx9mathh"></a>Função D3DXQuaternionRotationAxis (D3dx9math.h)

Gira um quaternion sobre um eixo arbitrário.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionRotationAxis(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXVECTOR3    *pV,
  _In_          FLOAT          Angle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a [**estrutura D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para a [**estrutura D3DXVECTOR3**](d3dxvector3.md) que identifica o eixo sobre o qual girar o quaternão.

</dd> <dt>

*Ângulo* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ângulo de rotação, em radianos. Os ângulos são medidos no sentido horário olhando ao longo do eixo de rotação em direção à origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para uma [**estrutura D3DXQUATERNION**](d3dxquaternion.md) girada em torno do eixo especificado.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXQuaternionRotationAxis** pode ser usada como um parâmetro para outra função.

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

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> <dt>

[**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 
