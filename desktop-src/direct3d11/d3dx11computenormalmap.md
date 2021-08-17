---
title: Função D3DX11ComputeNormalMap (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Observação Em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, ComputeNormalMap.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- Função D3DX11ComputeNormalMap Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747b8b01834126beb12e42d2fa26e15ea99c7471935af8ad74d078d15e9233ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124911"
---
# <a name="d3dx11computenormalmap-function"></a>Função D3DX11ComputeNormalMap

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex,](https://github.com/Microsoft/DirectXTex) **ComputeNormalMap.**

 

Converte um mapa de altura em um mapa normal. Os componentes (x,y,z) de cada normal são mapeados para os canais (r, g,b) da textura de saída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pContext* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ponteiro para uma [**interface ID3D11DeviceContext,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) representando a textura do mapa de altura de origem.

</dd> <dt>

*pSrcTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Ponteiro para uma [**interface ID3D11Texture2D,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) representando a textura do mapa de altura de origem.

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Um ou mais sinalizadores NORMALMAP D3DX \_ que controlam a geração de mapas normais.

</dd> <dt>

*Canal* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Um sinalizador CHANNEL D3DX \_ que especifica a fonte das informações de altura.

</dd> <dt>

*Amplitude* \[ Em\]
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal. Valores mais altos geralmente torna os aumentos mais visíveis, valores mais baixos geralmente torna os aumentos menos visíveis.

</dd> <dt>

*pDestTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Ponteiro para uma [**interface ID3D11Texture2D,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) representando a textura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método calcula o normal usando a diferença central com um tamanho de kernel de 3x3. Os canais RGB no destino contêm componentes polares (x,y,z) do normal. O denominador diferencial central é em código para 2.0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

