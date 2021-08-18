---
description: Função D3DXQuaternionToAxisAngle (D3dx9math.h) – calcula o eixo e o ângulo de rotação de um quatternion.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Função D3DXQuaternionToAxisAngle (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8b22b0a4c094a47e412172807c42cf25dc3c89342cf8e7e4ece9e731d9014bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731284"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>Função D3DXQuaternionToAxisAngle (D3dx9math.h)

Calcula o eixo de um quaterna e o ângulo de rotação.

## <a name="syntax"></a>Sintaxe


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pQ* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para a estrutura [**D3DXQUATERNION de origem.**](d3dxquaternion.md)

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Essa função retorna um ponteiro para uma [**estrutura D3DXVECTOR3**](d3dxvector3.md) que identifica o eixo de rotação do quaterna.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Essa função retorna um ponteiro para um valor FLOAT que identifica o ângulo de rotação do quaternão em radianos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Use [**D3DXQuaternionNormalize para**](d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
