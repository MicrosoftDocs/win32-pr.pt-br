---
description: Retorna um vetor 4D que é composto pelos menores componentes de dois vetores de 4D.
ms.assetid: ae3819a3-a5b6-47c2-b789-3e3f07db9f03
title: Função D3DXVec4Minimize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Minimize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ccd4806bfa368fafa481500d3bd28e0ff55b7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784600"
---
# <a name="d3dxvec4minimize-function"></a>Função D3DXVec4Minimize

Retorna um vetor 4D que é composto pelos menores componentes de dois vetores de 4D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4Minimize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV1,
  _In_    const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*pV1* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.

</dd> <dt>

*pV2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é composta pelos menores componentes dos dois vetores.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXVec4Minimize** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec4Maximize**](d3dxvec4maximize.md)
</dt> </dl>

 

 




