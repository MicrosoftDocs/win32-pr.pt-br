---
title: Função D3DX11ComputeNormalMap (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Observação em vez de usar essa função, recomendamos que você use a biblioteca DirectXTex, ComputeNormalMap.
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
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173118"
---
# <a name="d3dx11computenormalmap-function"></a>Função D3DX11ComputeNormalMap

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

> [!Note]  
> Em vez de usar essa função, recomendamos que você use a biblioteca [DirectXTex](https://github.com/Microsoft/DirectXTex) , **ComputeNormalMap**.

 

Converte um mapa de altura em um mapa normal. Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.

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

*pContext* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ponteiro para uma interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) , representando a textura de mapa de altura de origem.

</dd> <dt>

*pSrcTexture* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Ponteiro para uma interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , representando a textura de mapa de altura de origem.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Um ou mais \_ sinalizadores D3DX NormalMap que controlam a geração de mapas normais.

</dd> <dt>

*Canal* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Um \_ sinalizador de canal D3DX especificando a fonte de informações de altura.

</dd> <dt>

*Amplitude* \[ no\]
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

Multiplicador de valor constante que aumenta (ou diminui) os valores no mapa normal. Valores mais altos geralmente tornam os choques mais visíveis, os valores mais baixos geralmente tornam os choques menos visíveis.

</dd> <dt>

*pDestTexture* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Ponteiro para uma interface [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , representando a textura de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser o seguinte valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método computa o normal usando a diferença central com um tamanho de kernel de 3x3. Os canais RGB no destino contêm componentes com tendência (x, y, z) do normal. O denominador diferencial central está codificado para 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

