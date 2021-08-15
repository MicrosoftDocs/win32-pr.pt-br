---
description: Dimensiona um valor de cor.
ms.assetid: 35e8adee-7ce5-4db5-8276-f0e408748e78
title: Função D3DXColorScale (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorScale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95ae2ea24547f566a6da014f408dbfbce5be3112a61688f69e125e91d6085493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241416"
---
# <a name="d3dxcolorscale-function"></a>Função D3DXColorScale

Dimensiona um valor de cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorScale(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Ponteiro para uma [**estrutura D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.

</dd> <dt>

*pC* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura [**D3DXCOLOR de origem.**](d3dxcolor.md)

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Fator de escala. Ele dimensiona a cor, tratando-a como um vetor 4D. Não há limites no valor de s. Se s for 1, a cor resultante será a cor original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma [**estrutura D3DXCOLOR**](d3dxcolor.md) que é o valor de cor dimensionado.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a **função D3DXColorScale** pode ser usada como um parâmetro para outra função.

Essa função calcula o valor de cor dimensionada multiplicando os componentes de cor da estrutura [**D3DXCOLOR**](d3dxcolor.md) pelo fator de escala especificado, conforme mostrado no exemplo a seguir.


```
pOut->r = pC->r * s;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> </dl>

 

 
