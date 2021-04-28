---
description: Função D3DXQuaternionToAxisAngle (D3dx9math. h) – computa o eixo de um Quaternion e o ângulo de rotação.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Função D3DXQuaternionToAxisAngle (D3dx9math. h)
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
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117974"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>Função D3DXQuaternionToAxisAngle (D3dx9math. h)

Computa o eixo de um Quaternion e o ângulo de rotação.

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

*pQ* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> <dt>

*pAxis* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Essa função retorna um ponteiro para uma estrutura [**D3DXVECTOR3**](d3dxvector3.md) que identifica o eixo de rotação do Quaternion.

</dd> <dt>

*pAngle* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Essa função retorna um ponteiro para um valor FLOAT que identifica o ângulo de rotação de Quaternion em radianos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
