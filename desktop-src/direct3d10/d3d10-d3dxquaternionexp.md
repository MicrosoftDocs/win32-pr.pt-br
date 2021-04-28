---
description: Função D3DXQuaternionExp (D3DX10Math. h) – calcula o exponencial.
ms.assetid: bd70c432-ac61-4c38-b10b-3b103e49ead8
title: Função D3DXQuaternionExp (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionExp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7c022b9df4302683a184b4fc8329561b22d341d5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103214"
---
# <a name="d3dxquaternionexp-function-d3dx10mathh"></a>Função D3DXQuaternionExp (D3DX10Math. h)

Calcula o exponencial.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionExp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para a estrutura de D3DXQUATERNION de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para uma estrutura D3DXQUATERNION que é o exponencial.

## <a name="remarks"></a>Comentários

Esse método converte um Quaternion puro em uma unidade Quaternion. D3DXQuaternionExp espera um Quaternion puro, em que w é ignorado no cálculo (w = = 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



em que v é a parte de vetor de um Quaternion.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXQuaternionExp pode ser usada como um parâmetro para outra função.

O método [**D3DXQuaternionSquadSetup**](d3d10-d3dxquaternionsquadsetup.md) também pode ser usado para configurar os pontos de controle de um Quaternion.

Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
