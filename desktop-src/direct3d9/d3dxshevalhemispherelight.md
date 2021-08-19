---
description: Função D3DXSHEvalHemisphereLight (D3dx9math.h) – avalia uma luz que é uma interpolação linear entre duas cores sobre a esfera.
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Função D3DXSHEvalHemisphereLight (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 25f1ae13b800c99d3356147d0ac5aa73a2cf091882822bee4ccbed7e160516b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524231"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a>Função D3DXSHEvalHemisphereLight (D3dx9math.h)

Avalia uma luz que é uma interpolação linear entre duas cores sobre a esfera.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH (avaliação esférica). Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pDir* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para o vetor (x, y, z) de direção do eixo do sistema no qual as funções de base sh são avaliadas. Consulte Observações.

</dd> <dt>

*Superior* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**

A cor do céu.

</dd> <dt>

*Inferior* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**

A cor do chão.

</dd> <dt>

*pROut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente vermelho.

</dd> <dt>

*pGOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente verde.

</dd> <dt>

*pBOut* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A interpolação é feita linearmente entre os dois pontos, não sobre a superfície da esfera (ou seja, se o eixo era (0,0,1) ele é linear em Z, não no ângulo azimuthal). A função de iluminação esférica resultante é normalizada para que um ponto em uma superfície perfeitamente difusa sem sombreamento e um normal apontado na direção *pDir* resulte em radiação de saída com um valor de 1 (se a cor superior fosse branca e a cor inferior fosse preta). Esse é um modelo muito simples em que *Top* representa a intensidade do "céu" e *Bottom* representa a intensidade do "solo".

Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode [](coordinate-systems.md)ser especificada simplesmente com theta, o ângulo sobre o eixo z na direção à direita e, em seguida, o ângulo de z.

![ilustração de uma esfera com raio de unidade](images/spherical-coordinates.png)

As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esféricas (theta, yo) na esfera de unidade. O ângulo de theta varia de 0 a 2 pi, enquanto que o valor varia de 0 a pi.

![equações da relação entre coordenadas cartesianas e esféricas](images/spherical-coordinates-equations.png)

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

 

 
