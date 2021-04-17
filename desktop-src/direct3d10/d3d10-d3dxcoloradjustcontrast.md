---
description: Ajusta o valor de contraste de uma cor.
ms.assetid: c111d3c7-19c6-4a6b-af0d-a9e1bc0bb7d9
title: Função D3DXColorAdjustContrast (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdjustContrast
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 24586b2a8d2206d6818e00af9ea86e4c5e9758fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748895"
---
# <a name="d3dxcoloradjustcontrast-function-d3dx10mathh"></a>Função D3DXColorAdjustContrast (D3DX10Math. h)

Ajusta o valor de contraste de uma cor.

## <a name="syntax"></a>Sintaxe


```C++
D3DXCOLOR* D3DXColorAdjustContrast(
  _In_       D3DXCOLOR *pOut,
  _In_ const D3DXCOLOR *pC,
  _In_       FLOAT     c
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pout* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

\[ponteiro de entrada \] para um [**D3DXCOLOR**](d3d10-d3dxcolor.md) que é o resultado da operação.

</dd> <dt>

*PC* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXCOLOR**](../direct3d9/d3dxcolor.md) \***

Ponteiro para uma estrutura de D3DXCOLOR de origem.

</dd> <dt>

*c* \[ em\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Valor de contraste. Esse parâmetro interpola linearmente entre 50% de cinza e a cor, pC. Não há nenhum limite no valor de c. Se esse parâmetro for zero, a cor retornada será de 50% de cinza. Se esse parâmetro for 1, a cor retornada será a cor original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)\***

Essa função retorna um ponteiro para uma estrutura D3DXCOLOR que é o resultado do ajuste de contraste.

## <a name="remarks"></a>Comentários

O canal alfa de entrada é copiado, não modificado, para o canal alfa de saída.

O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut. Dessa forma, essa função pode ser usada como um parâmetro para outra função.

Essa função interpola os componentes de cor vermelho, verde e azul de uma estrutura D3DXCOLOR entre 50% de cinza e um valor de contraste especificado, conforme mostrado no exemplo a seguir.


```
pOut->r = 0.5f + c * (pC->r - 0.5f);
```



Se c for maior que 0 e menor que 1, o contraste será diminuído. Se c for maior que 1, o contraste será aumentado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
