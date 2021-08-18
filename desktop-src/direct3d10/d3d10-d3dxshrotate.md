---
description: Função D3DXSHRotate (D3DX10.h) – gira o vetor sh (ataque esférico) pela matriz determinada.
ms.assetid: 22ed379a-ce08-46df-9cc1-8d5fde87c179
title: Função D3DXSHRotate (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotate
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0ff63f6ad2fbbb75baaa32c4754a4cee3437ba34fe6dbd3b0412464deaf8fd71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990776"
---
# <a name="d3dxshrotate-function-d3dx10h"></a>Função D3DXSHRotate (D3DX10.h)

Gira o vetor sh (metal esférico) pela matriz determinada.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHRotate(
  _In_       FLOAT      *pOut,
  _In_       UINT       Order,
  _In_ const D3DXMATRIX *pMatrix,
  _In_ const FLOAT      *pIn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para coeficientes de saída sh (spherical) . A avaliação gera coeficientes orderâmicos. Esse ponteiro não deve ser alias com pIn. Consulte Observações.

</dd> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pMatrix* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ponteiro para a matriz de rotação. A sub-matriz de rotação deve ser ortogonal, com uma unidade determinante.

</dd> <dt>

*pIn* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ponteiro para coeficientes SH girados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para coeficientes de saída sh.

## <a name="remarks"></a>Comentários

Cada coeficiente da função de base Ylm é armazenado no local de memória lá + m + l, em que:

-   l é o grau da função base.
-   m é o índice de função base para o valor l e intervalos de -l a l, inclusive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
