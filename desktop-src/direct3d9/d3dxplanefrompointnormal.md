---
description: Função D3DXPlaneFromPointNormal (D3dx9math.h) – constrói um plano de um ponto e um normal.
ms.assetid: af396bbb-09b7-492f-a25f-9c950da7e605
title: Função D3DXPlaneFromPointNormal (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0acf7dd26a2eb261830dbdf1f0e1fff185184a645e469fbe02a5b0032c141e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524913"
---
# <a name="d3dxplanefrompointnormal-function-d3dx9mathh"></a>Função D3DXPlaneFromPointNormal (D3dx9math.h)

Constrói um plano de um ponto e um normal.

## <a name="syntax"></a>Sintaxe


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para a [**estrutura D3DXPLANE**](d3dxplane.md) que é o resultado da operação.

</dd> <dt>

*pPoint* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) definindo o ponto usado para construir o plano.

</dd> <dt>

*pNormal* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para uma [**estrutura D3DXVECTOR3,**](d3dxvector3.md) definindo o normal usado para construir o plano.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***

Ponteiro para a [**estrutura D3DXPLANE**](d3dxplane.md) construída do ponto e do normal.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXPlaneFromPointNormal** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneFromPoints**](d3dxplanefrompoints.md)
</dt> </dl>

 

 




