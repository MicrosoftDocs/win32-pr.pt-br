---
description: Combina duas cores.
ms.assetid: deff70c7-2359-48b2-ab40-8c418acf5a07
title: Função D3DXColorModulate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorModulate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cf9b202da786f6ec87ceca9816c2a4fc86776577
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173074"
---
# <a name="d3dxcolormodulate-function"></a>Função D3DXColorModulate

Combina duas cores.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorModulate(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.

</dd> <dt>

 \ \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.

</dd> <dt>

*pC2* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação de mesclagem.

## <a name="remarks"></a>Comentários

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, a função **D3DXColorModulate** pode ser usada como um parâmetro para outra função.

Essa função combina duas cores multiplicando os componentes de cor correspondentes, conforme mostrado no exemplo a seguir.


```
pOut->r = pC1->r * pC2->r;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorLerp**](d3dxcolorlerp.md)
</dt> <dt>

[**D3DXColorNegative**](d3dxcolornegative.md)
</dt> <dt>

[**D3DXColorScale**](d3dxcolorscale.md)
</dt> </dl>

 

 




