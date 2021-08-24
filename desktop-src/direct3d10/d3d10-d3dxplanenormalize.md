---
description: Função D3DXPlaneNormalize (D3DX10Math. h)-normaliza os coeficientes de plano para que o plano normal tenha comprimento de unidade.
ms.assetid: 52ae36a7-e37b-457a-9832-e62900a85bde
title: Função D3DXPlaneNormalize (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf4429e324a5ce1554c5c37c929625153c74764cb9d03618f633f35ecd416748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754146"
---
# <a name="d3dxplanenormalize-function-d3dx10mathh"></a>Função D3DXPlaneNormalize (D3DX10Math. h)

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

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para o [**D3DXPLANE**](d3d10-d3dxplane.md) que é o resultado da operação.

</dd> <dt>

*PP* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***

Ponteiro para a estrutura de D3DXPLANE de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Ponteiro para uma estrutura D3DXPLANE que representa o normal do plano.

## <a name="remarks"></a>Comentários

Essa função normaliza um plano de forma que \| a, b, c \| = = 1.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, essa função pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
