---
description: Função D3DXSHEvalHemisphereLight (D3dx9math. h) – avalia uma luz que é uma interpolação linear entre duas cores na esfera.
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Função D3DXSHEvalHemisphereLight (D3dx9math. h)
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
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a>Função D3DXSHEvalHemisphereLight (D3dx9math. h)

Avalia uma luz que é uma interpolação linear entre duas cores na esfera.

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

*Ordem* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ordem da avaliação harmônica esférica (SH). Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes do Order ². O grau da avaliação é a ordem 1.

</dd> <dt>

*pDir* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH. Consulte Observações.

</dd> <dt>

*Superior* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**

A cor do céu.

</dd> <dt>

*Parte inferior* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**

A cor do solo.

</dd> <dt>

*pROut* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente vermelho.

</dd> <dt>

*pGOut* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente verde.

</dd> <dt>

*pBOut* \[ no\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor SH de saída para o componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

A interpolação é feita linearmente entre os dois pontos, e não a superfície da esfera (ou seja, se o eixo fosse (0, 0, 1) ele é linear em Z, não no ângulo de azimuthal). A função de iluminação esférica resultante é normalizada para que um ponto em uma superfície perfeitamente difusa sem sombreamento e um apontador normal na direção *pDir* resultem em Exit radiante com um valor de 1 (se a cor superior fosse branca e a cor inferior fosse preta). Esse é um modelo muito simples em que *Top* representa a intensidade do "céu" e *inferior* representa a intensidade do "aterramento".

Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na [direção da mão direita](coordinate-systems.md)e Phi, o ângulo de z.

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade. O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[Transferência radiante de computação (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
