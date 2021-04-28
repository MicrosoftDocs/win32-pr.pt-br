---
description: Função D3DXQuaternionExp (D3dx9math. h) – calcula o exponencial.
ms.assetid: 648aeaf1-ead3-4b21-819f-cd2a70881a13
title: Função D3DXQuaternionExp (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30e48e21e2dc6af487f1fb076af3b3f2df57f9f3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094094"
---
# <a name="d3dxquaternionexp-function-d3dx9mathh"></a>Função D3DXQuaternionExp (D3dx9math. h)

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

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Ponteiro para a estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o exponencial.

## <a name="remarks"></a>Comentários

Esse método converte um Quaternion puro em uma unidade Quaternion. **D3DXQuaternionExp** espera um Quaternion puro, em que w é ignorado no cálculo (w = = 0).


```
Given a pure quaternion defined by:
q = (0, theta * v); 
    
This method calculates the exponential result.
exp(Q) = (cos(theta), sin(theta) * v)
```



em que v é a parte de vetor de um Quaternion.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXQuaternionExp** pode ser usada como um parâmetro para outra função.

O método [**D3DXQuaternionSquadSetup**](d3dxquaternionsquadsetup.md) também pode ser usado para configurar os pontos de controle de um Quaternion.

Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionLn**](d3dxquaternionln.md)
</dt> <dt>

[**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
</dt> </dl>

 

 




