---
description: Função D3DXVec2Normalize (D3dx9math.h) – retorna a versão normalizada de um vetor 2D.
ms.assetid: 2796a5d1-cb1c-4093-87f2-a2ad43279d91
title: Função D3DXVec2Normalize (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c366ef54c609f2c896b78510bfbe771260b9ef4cdc38c42d3fe0393e1e2a17dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122580"
---
# <a name="d3dxvec2normalize-function-d3dx9mathh"></a>Função D3DXVec2Normalize (D3dx9math.h)

Retorna a versão normalizada de um vetor 2D.

## <a name="syntax"></a>Sintaxe


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para a [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é o resultado da operação.

</dd> <dt>

*pV* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Ponteiro para a estrutura [**D3DXVECTOR2 de**](d3dxvector2.md) origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Ponteiro para uma [**estrutura D3DXVECTOR2**](d3dxvector2.md) que é a versão normalizada do vetor.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXVec2Normalize** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




