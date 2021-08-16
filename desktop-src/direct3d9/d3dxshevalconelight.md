---
description: Função D3DXSHEvalConeLight (D3dx9math.h) – avalia uma luz que é um cone de intensidade constante e retorna dados sh (metal esféricos) espectral.
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Função D3DXSHEvalConeLight (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3904ee079399a2a3b7152e04a0101bfdef6f1eee393822465bf072271749cba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122755"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a>Função D3DXSHEvalConeLight (D3dx9math.h)

Avalia uma luz que é um casque de intensidade constante e retorna dados sh (spherical) espectral.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Ordem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ordem da avaliação de SH. Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive. A avaliação gera coeficientes orderâmicos. O grau da avaliação é Order - 1.

</dd> <dt>

*pDir* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para o vetor (x, y, z) de direção do eixo do sistema no qual as funções de base sh são avaliadas. Consulte Observações.

</dd> <dt>

*Raio* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Raio de cone em radianos.

</dd> <dt>

*RIntensity* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A intensidade vermelha da luz.

</dd> <dt>

*GIntensity* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A intensidade verde da luz.

</dd> <dt>

*BIntensity* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

A intensidade azul da luz.

</dd> <dt>

*pROut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente vermelho.

</dd> <dt>

*pGOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente verde.

</dd> <dt>

*pBOut* \[ out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Ponteiro para o vetor sh de saída para o componente azul.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Avalia uma luz que é um cone de intensidade constante e retorna dados sh espectral. O vetor de saída é calculado para que, se a taxa de intensidade R/G/B for igual a 1, o radiamento de saída de um ponto diretamente sob a luz (orientado na direção do cone em um objeto difuso com um albedo de 1) seria 1,0. Isso calculará três exemplos espectrais; *pROut* será retornado, enquanto *pGOut* e *pBOut* podem ser retornados.

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

 

 
