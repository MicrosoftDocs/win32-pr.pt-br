---
description: Função D3DXColorAdjustSaturation (D3dx9math. h) – ajusta o valor de saturação de uma cor.
ms.assetid: 1f66c3b4-2f02-4993-80c6-c484180c2459
title: Função D3DXColorAdjustSaturation (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 878cdd83a04f594da3133eda314486af96ac3d56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115864"
---
# <a name="d3dxcoloradjustsaturation-function-d3dx9mathh"></a>Função D3DXColorAdjustSaturation (D3dx9math. h)

Ajusta o valor de saturação de uma cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorAdjustSaturation(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC,
  _In_          FLOAT     s
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado da operação.

</dd> <dt>

*PC* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](d3dxcolor.md) \***

Ponteiro para uma estrutura de [**D3DXCOLOR**](d3dxcolor.md) de origem.

</dd> <dt>

*s* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor de saturação. Esse parâmetro interpola linearmente entre a cor convertida em escala de cinza e a cor original, pC. Não há limites para o valor de s. Se s for 0, a cor retornada será a cor de escala de cinza. Se s for 1, a cor retornada será a cor original.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Essa função retorna um ponteiro para uma estrutura [**D3DXCOLOR**](d3dxcolor.md) que é o resultado do ajuste de saturação.

## <a name="remarks"></a>Comentários

O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, essa função pode ser usada como um parâmetro para outra função.

Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura [**D3DXCOLOR**](d3dxcolor.md) entre uma cor não saturada e uma cor, conforme mostrado no exemplo a seguir.


```
    // Approximate values for each component's contribution to luminance.
    // Based upon the NTSC standard described in ITU-R Recommendation BT.709.
    FLOAT grey = pC->r * 0.2125f + pC->g * 0.7154f + pC->b * 0.0721f;
    
    pOut->r = grey + s * (pC->r - grey);
```



Se s for maior que 0 e menor que 1, a saturação será diminuída. Se s for maior que 1, a saturação será aumentada.

A cor de escala de cinza é calculada como:


```
r = g = b = 0.2125*r + 0.7154*g + 0.0721*b
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXColorAdjustContrast**](d3dxcoloradjustcontrast.md)
</dt> </dl>

 

 
