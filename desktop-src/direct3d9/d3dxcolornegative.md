---
description: Cria o valor de cor negativo de um valor de cor.
ms.assetid: 74143126-93f8-49fa-abe3-fd730b644d87
title: Função D3DXColorNegative (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorNegative
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c046702b81ce60f2e50817cb98c04686d9a35e964a141d88fd70dd05654e3067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069326"
---
# <a name="d3dxcolornegative-function"></a>Função D3DXColorNegative

Cria o valor de cor negativo de um valor de cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorNegative(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC
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

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma [**estrutura D3DXCOLOR**](d3dxcolor.md) que é o valor de cor negativo do valor de cor.

## <a name="remarks"></a>Comentários

O canal alfa de entrada é copiado, sem modificação, para o canal alfa de saída.

O valor retornado para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a **função D3DXColorNegative** pode ser usada como um parâmetro para outra função.

Essa função retorna o valor de cor negativa subtraindo 1,0 dos componentes de cor da estrutura [**D3DXCOLOR,**](d3dxcolor.md) conforme mostrado no exemplo a seguir.


```
pOut->r = 1.0f - pC->r;
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

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




