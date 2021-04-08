---
description: Retorna a versão normalizada de um vetor 4D.
ms.assetid: e12d5dc7-b26f-41dd-b89d-1df9ba23077a
title: Função D3DXVec4Normalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 38d97f337711375d1d414eb78fb317672bc7c5cb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012189"
---
# <a name="d3dxvec4normalize-function-d3dx9mathh"></a>Função D3DXVec4Normalize (D3dx9math. h)

Retorna a versão normalizada de um vetor 4D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Ponteiro para a estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Ponteiro para uma estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é a versão normalizada do vetor.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXVec4Normalize** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




