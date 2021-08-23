---
description: Usa interpolação linear para criar um valor de cor.
ms.assetid: bf7bf2f4-5fb5-44d3-a7e5-7998640d7d49
title: Função D3DXColorLerp (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorLerp
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fa0134ca1c3cf88e0e25f253cca4ebeb16a89b5bdaa982cf4e9e96e85bfb1d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988696"
---
# <a name="d3dxcolorlerp-function"></a>Função D3DXColorLerp

Usa interpolação linear para criar um valor de cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorLerp(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2,
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

*pC1* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura [**D3DXCOLOR de origem.**](d3dxcolor.md)

</dd> <dt>

*pC2* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura [**D3DXCOLOR de origem.**](d3dxcolor.md)

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Parâmetro que interpola linearmente entre as cores, pC1 e pC2, tratando-as como vetores 4D. Não há limites no valor de s.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma [**estrutura D3DXCOLOR**](d3dxcolor.md) que é o resultado da interpolação linear.

## <a name="remarks"></a>Comentários

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a **função D3DXColorLerp** pode ser usada como um parâmetro para outra função.

Essa função interpola os componentes vermelho, verde, azul e alfa de uma estrutura [**D3DXCOLOR**](d3dxcolor.md) entre duas cores, conforme mostrado no exemplo a seguir.


```
   
pOut->r = pC1->r + s * (pC2->r - pC1->r);
```



Se você estiver interpolando linearmente entre as cores A e B e s for 0, a cor resultante será A. Se s for 1, a cor resultante será a cor B.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorModulate**](d3dxcolormodulate.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 
