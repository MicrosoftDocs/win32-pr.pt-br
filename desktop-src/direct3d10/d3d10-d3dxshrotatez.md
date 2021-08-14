---
description: Função D3DXSHRotateZ (D3DX10.h) – gira o vetor sh (ataque esférico) no eixo z pelo ângulo determinado.
ms.assetid: 7c4bec55-4a4c-4f7e-8849-1cac373a2340
title: Função D3DXSHRotateZ (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHRotateZ
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ea15bf7bbcbea68fabf592ec8bad409990038d03fb1f4014f760b92d124408b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990016"
---
# <a name="d3dxshrotatez-function-d3dx10h"></a>Função D3DXSHRotateZ (D3DX10.h)

Gira o vetor sh (ataque esférico) no eixo z pelo ângulo determinado.

## <a name="syntax"></a>Sintaxe


```C++
FLOAT* D3DXSHRotateZ(
  _In_       FLOAT *pOut,
  _In_       UINT  Order,
  _In_       FLOAT Angle,
  _In_ const FLOAT *pIn
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

*Ângulo* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Ângulo de rotação em radianos. A rotação é executada em torno do eixo z.

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

 

 
