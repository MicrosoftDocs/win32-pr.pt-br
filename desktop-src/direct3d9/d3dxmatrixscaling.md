---
description: Função D3DXMatrixScaling (D3dx9math. h) – compila uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Função D3DXMatrixScaling (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ccd4cc6207bb211259833d163793c3499b51a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118064"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a>Função D3DXMatrixScaling (D3dx9math. h)

Cria uma matriz que é dimensionada ao longo do eixo x, do eixo y e do eixo z.

## <a name="syntax"></a>Sintaxe


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.

</dd> <dt>

*SX* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de dimensionamento aplicado ao longo do eixo x.

</dd> <dt>

*Sy* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de dimensionamento aplicado ao longo do eixo y.

</dd> <dt>

*sz* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Fator de dimensionamento aplicado ao longo do eixo z.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ponteiro para o [**D3DXMATRIX**](d3dxmatrix.md)de transformação de dimensionamento.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* . Dessa forma, a função **D3DXMatrixScaling** pode ser usada como um parâmetro para outra função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
