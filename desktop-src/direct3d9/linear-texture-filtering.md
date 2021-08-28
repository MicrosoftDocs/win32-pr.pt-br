---
description: O Direct3D usa uma forma de filtragem de textura linear chamada filtragem biline.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtragem de textura linear (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5177af653c74383ef87468dbb43167fa2962cd093410a6a63f85da2233e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628526"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Filtragem de textura linear (Direct3D 9)

O Direct3D usa uma forma de filtragem de textura linear chamada filtragem biline. Assim como a [amostragem de ponto mais próximo (Direct3D 9)](nearest-point-sampling.md), a filtragem de textura bilinear primeiro computa um endereço Texel, que geralmente não é um endereço inteiro. A filtragem bilinear localiza o Texel cujo endereço de inteiro é mais próximo do endereço computado. Além disso, o módulo de renderização do Direct3D computa uma média ponderada dos texels que estão imediatamente acima, abaixo, à esquerda de e à direita do ponto de exemplo mais próximo.

Selecione filtragem de textura bilinear invocando o método [**IDirect3DDevice9:: Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Defina o valor do primeiro parâmetro como o número de índice inteiro (0-7) da textura para a qual você está selecionando um método de filtragem de textura. Pass D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER para o segundo parâmetro para definir o filtro de ampliação, minificação ou mipmapping. Passe D3DTEXF \_ linear no terceiro parâmetro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtragem de textura](texture-filtering.md)
</dt> </dl>

 

 
