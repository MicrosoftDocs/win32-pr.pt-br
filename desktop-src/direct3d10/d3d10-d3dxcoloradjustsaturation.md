---
description: Ajusta o valor de saturação de uma cor.
ms.assetid: a7ca64b4-2198-4116-8e9f-79d6c922fd09
title: Função D3DXColorAdjustSaturation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustSaturation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6cfa4dd2af6e4a4ac3772af80ba11b8189405f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930696"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx10mathh"></a>Função D3DXColorAdjustSaturation (D3DX10Math. h)

Ajusta o valor de saturação de uma cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Ponteiro para um [**D3DXCOLOR**](d3d10-d3dxcolor.md) que é o resultado da operação.

</dd> <dt>

*PC* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Ponteiro para uma estrutura de D3DXCOLOR de origem.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor de saturação. Esse parâmetro interpola linearmente entre a cor convertida em escala de cinza e a cor original, pC. Não há limites para o valor de s. Se s for 0, a cor retornada será a cor de escala de cinza. Se s for 1, a cor retornada será a cor original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Essa função retorna um ponteiro para uma estrutura D3DXCOLOR que é o resultado do ajuste de saturação.

## <a name="remarks"></a>Comentários

O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, essa função pode ser usada como um parâmetro para outra função.

Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura D3DXCOLOR entre uma cor não saturada e uma cor, conforme mostrado no exemplo a seguir.


```
//Approximate values for each component's contribution to luminance.
//Based upon the NTSC standard described in ITU-R Recommendation BT.709.
FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;

pOut->r = grey + s * (pC->r - grey);
```



Se s for maior que 0 e menor que 1, a saturação será diminuída. Se s for maior que 1, a saturação será aumentada.

A cor de escala de cinza é calculada como:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
