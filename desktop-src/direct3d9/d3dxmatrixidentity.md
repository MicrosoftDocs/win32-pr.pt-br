---
description: Cria uma matriz de identidade.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Função D3DXMatrixIdentity (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce7d891eb446372b749c7085a37e80241c52f1cf862a61b3fc9edeb544776b2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044890"
---
# <a name="d3dxmatrixidentity-function"></a>Função D3DXMatrixIdentity

Cria uma matriz de identidade.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a [**estrutura D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para uma [**estrutura D3DXMATRIX**](d3dxmatrix.md) que é a matriz de identidade.

## <a name="remarks"></a>Comentários

A matriz de identidade é uma matriz na qual todos os coeficientes são 0, exceto os \[ coeficientes 1,1 \] \[ 2,2 \] \[ 3,3 \] \[ 4,4, que são \] definidos como 1. A matriz de identidade é especial porque, quando ela é aplicada aos vértices, elas ficam inalteradas. A matriz de identidade é usada como o ponto de partida para matrizes que modificarão valores de vértice para criar rotações, traduções e quaisquer outras transformações que possam ser representadas por uma matriz 4 x4.

O valor retornado para essa função é o mesmo valor retornado no *parâmetro pOut.* Dessa forma, a **função D3DXMatrixIdentity** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIsIdentity**](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




