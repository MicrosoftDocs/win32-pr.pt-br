---
description: Função D3DXSHDot (D3dx9math.h) – calcula o produto de ponto de dois vetores sh (ataque esférico).
ms.assetid: 71b7480d-ddac-4b02-bca7-d9318823d03e
title: Função D3DXSHDot (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9c852bd93f839d371aa86886cd06769f79fe635986566ed592f8f5313ee8084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731176"
---
# <a name="d3dxshdot-function-d3dx9mathh"></a>Função D3DXSHDot (D3dx9math.h)

Calcula o produto de ponto de dois vetores de SH (ataque esférico).

## <a name="syntax"></a>Sintaxe


```C++
FLOAT D3DXSHDot(
  _In_       UINT  Order,
  _In_ const FLOAT *pA,
  _In_ const FLOAT *pB
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH (avaliação esférica). Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pA* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ponteiro para o primeiro vetor SH.

</dd> <dt>

*pB* \[ Em\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Ponteiro para o segundo vetor SH.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Coeficientes de saída sh.

## <a name="remarks"></a>Comentários

Cada coeficiente da função de base Ylm é armazenado no local de memória lá + m + l, em que:

-   l é o grau da função base.
-   m é o índice de função base para o valor l e intervalos de -l a l, inclusive.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferência de Radiance pré-comutada (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
