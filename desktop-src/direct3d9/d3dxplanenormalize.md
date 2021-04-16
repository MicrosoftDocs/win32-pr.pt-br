---
description: Normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Função D3DXPlaneNormalize (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0f0c87028d3b37f785005725e7510f689cf56d61
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761505"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Função D3DXPlaneNormalize (D3dx9math. h)

Normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que é o resultado da operação.

</dd> <dt>

*PP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Ponteiro para a estrutura de [**D3DXPLANE**](d3dxplane.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para uma estrutura [**D3DXPLANE**](d3dxplane.md) que representa o normal do plano.

## <a name="remarks"></a>Comentários

Essa função normaliza um plano de forma que \| a, b, c \| = = 1.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, essa função pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




