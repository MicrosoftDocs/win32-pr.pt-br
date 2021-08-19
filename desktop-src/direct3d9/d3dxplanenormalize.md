---
description: Função D3DXPlaneNormalize (D3dx9math.h) – Normaliza os coeficientes de plano para que o plano normal tenha comprimento unitário.
ms.assetid: 9c595986-e1f8-4153-ba23-1fa6e583a050
title: Função D3DXPlaneNormalize (D3dx9math.h)
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
ms.openlocfilehash: a8a5a80526e013c85caf59b3a6a3d6c595a3c10a6e29687882c7789765368d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952306"
---
# <a name="d3dxplanenormalize-function-d3dx9mathh"></a>Função D3DXPlaneNormalize (D3dx9math.h)

Normaliza os coeficientes de plano para que o plano normal tenha comprimento unitário.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneNormalize(
  _Inout_       D3DXPLANE *pOut,
  _In_    const D3DXPLANE *pP
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para a [**estrutura D3DXPLANE**](d3dxplane.md) que é o resultado da operação.

</dd> <dt>

*pP* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Ponteiro para a estrutura [**D3DXPLANE de origem.**](d3dxplane.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para uma [**estrutura D3DXPLANE**](d3dxplane.md) que representa o normal do plano.

## <a name="remarks"></a>Comentários

Essa função normaliza um plano para \| que a,b,c \| == 1.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, essa função pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




