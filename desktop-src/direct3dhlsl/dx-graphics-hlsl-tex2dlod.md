---
title: tex2Dlod
description: Amostras de uma textura 2D com mipmaps. O LOD mipmap é especificado em t.w.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9581418eb2a3d8736fcd0e125eaafec11494e6b6d5471cef33f9592475d5ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725674"
---
# <a name="tex2dlod"></a>tex2Dlod

Amostras de uma textura 2D com mipmaps. O LOD mipmap é especificado em t.w.



| RET tex2Dlod (s, t) |
|--------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                   | Descrição                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*&*<br/> | \[no \] estado de amostra.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[na \] coordenada de textura.<br/> |



 

## <a name="return-value"></a>Valor Retornado

O valor dos dados de textura.

## <a name="type-description"></a>Descrição do tipo



| Nome | Entrada/saída | [**Tipo de modelo**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Tipo de componente**](dx-graphics-hlsl-intrinsic-functions.md) | Tamanho |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**objeto**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| RET  | out    | [**vetor**](dx-graphics-hlsl-intrinsic-functions.md) | [**barra**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                       | Com suporte |
|------------------------------------------------------------------------------------|-----------|
| [Modelo do sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) e modelos de sombreador mais altos | sim       |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | não        |



 

## <a name="remarks"></a>Comentários

A partir do Direct3D 10, você pode usar a nova sintaxe HLSL para acessar texturas e outros recursos. Você pode substituir funções de pesquisa de textura de estilo intrínseco, como **tex2Dlod**, por um estilo mais orientado a objeto. Nesse estilo orientado a objeto, as texturas são dissociadas dos exemplos e têm métodos para carregar e obter amostragem.

Para obter uma amostra de uma textura 2D, em vez de usar **tex2Dlod** como neste código:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Use o método [SampleLevel](dx-graphics-hlsl-to-samplelevel.md) de um [**objeto de textura**](dx-graphics-hlsl-to-type.md) como neste código:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Para usar as funções de pesquisa de textura de estilo intrínseco, como **tex2Dlod**, com o [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e superior, use [**D3DCOMPILE habilitar a \_ \_ \_ compatibilidade com versões anteriores**](d3dcompile-constants.md) para compilar. No entanto, se você quiser direcionar o modelo de sombreador 4 e superior (até [ \* \_ 4 \_ 0 \_ nível \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) com o código de estilo orientado a objeto mais recente, migre para a sintaxe HLSL mais recente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

