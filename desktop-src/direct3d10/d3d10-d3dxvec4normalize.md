---
description: Função D3DXVec4Normalize (D3DX10Math. h) – retorna a versão normalizada de um vetor 4D.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: Função D3DXVec4Normalize (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 1577ff3109c2cc3ca547f68f7841ecebb2f03569
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102904"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a>Função D3DXVec4Normalize (D3DX10Math. h)

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

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para o [**D3DXVECTOR4**](d3d10-d3dxvector4.md) que é o resultado da operação.

</dd> <dt>

*VP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***

Ponteiro para a estrutura de D3DXVECTOR4 de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***

Ponteiro para uma estrutura D3DXVECTOR4 que é a versão normalizada do vetor.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXVec4Normalize pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
