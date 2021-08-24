---
description: Função D3DX10ComputeNormalMap – converte um mapa de altura em um mapa normal. Os componentes (x,y,z) de cada normal são mapeados para os canais (r, g,b) da textura de saída.
ms.assetid: 535033dd-f078-4d56-8e5d-cdda80ef5992
title: Função D3DX10ComputeNormalMap (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ComputeNormalMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b719e1b40c3e8cd04ca0750e69c68bbd4a0a59394c3334818f091900606311af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634776"
---
# <a name="d3dx10computenormalmap-function"></a>Função D3DX10ComputeNormalMap

Converte um mapa de altura em um mapa normal. Os componentes (x,y,z) de cada normal são mapeados para os canais (r, g,b) da textura de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10ComputeNormalMap(
  _In_ ID3D10Texture2D *pSrcTexture,
  _In_ UINT            Flags,
  _In_ UINT            Channel,
  _In_ FLOAT           Amplitude,
  _In_ ID3D10Texture2D *pDestTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrcTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Ponteiro para uma interface ID3D10Texture2D, que representa a textura do mapa de altura de origem.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um ou mais sinalizadores NORMALMAP D3DX \_ que controlam a geração de mapas normais.

</dd> <dt>

*Canal* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um sinalizador CHANNEL D3DX \_ que especifica a fonte das informações de altura.

</dd> <dt>

*Amplitude* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal. Valores mais altos geralmente torna os aumentos mais visíveis, valores mais baixos geralmente torna os aumentos menos visíveis.

</dd> <dt>

*pDestTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***

Ponteiro para uma interface ID3D10Texture2D, representando a textura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método calcula o normal usando a diferença central com um tamanho de kernel de 3x3. Os canais RGB no destino contêm componentes polares (x,y,z) do normal. O denominador diferencial central é em código para 2.0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de textura no D3DX 10](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
