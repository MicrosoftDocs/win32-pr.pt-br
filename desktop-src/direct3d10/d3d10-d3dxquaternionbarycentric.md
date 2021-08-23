---
description: Função D3DXQuaternionBaryCentric (D3DX10Math.h) – retorna um quaternion em coordenadas centradas em barras.
ms.assetid: 0a8d8d5a-f486-4457-86e9-27e76eaf1bc4
title: Função D3DXQuaternionBaryCentric (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionBaryCentric
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6a51a0606ae45be79c26d062c64ab5710a658436371ca146f81c2183c34ca85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991146"
---
# <a name="d3dxquaternionbarycentric-function-d3dx10mathh"></a>Função D3DXQuaternionBaryCentric (D3DX10Math.h)

Retorna um quaterão em coordenadas centradas em barras.

## <a name="syntax"></a>Sintaxe


```C++
D3DXQUATERNION* D3DXQuaternionBaryCentric(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_    const D3DXQUATERNION *pQ3,
  _In_          FLOAT          f,
  _In_          FLOAT          g
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para [**o D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.

</dd> <dt>

*pQ1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*pQ2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*pQ3* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Ponteiro para uma estrutura D3DXQUATERNION de origem.

</dd> <dt>

*f* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> <dt>

*g* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de ponderação. Consulte Observações.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***

Ponteiro para uma estrutura D3DXQUATERNION em coordenadas centradas em barras.

## <a name="remarks"></a>Comentários

Para calcular as coordenadas centradas em barras, a função D3DXQuaternionBaryCentric implementa a seguinte série de operações de interpolação linear esférica:


```
Slerp(Slerp(Q1, Q2, f+g), Slerp(Q1, Q3, f+g), g/(f+g))
```



O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função D3DXQuaternionBaryCentric pode ser usada como um parâmetro para outra função.

Use [**D3DXQuaternionNormalize para**](d3d10-d3dxquaternionnormalize.md) qualquer entrada de quatérnion que ainda não tenha sido normalizada.

As coordenadas barycentric definem um ponto dentro de um triângulo em termos dos vértices do triângulo. Para obter uma descrição mais detalhada das coordenadas centradas em barras, consulte Descrição de [coordenadas barycentric da Mathworld.](https://mathworld.wolfram.com/BarycentricCoordinates.html)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
