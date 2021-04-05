---
description: Uma superfície representa uma área linear da memória de vídeo e geralmente reside na memória de vídeo do cartão de vídeo, embora as superfícies possam existir na memória do sistema. As superfícies são gerenciadas pela interface IDirect3DSurface9.
ms.assetid: 17add726-3d95-46bc-8e15-3be0e570c49c
title: Superfícies do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08729cc7252c39ddf71048991a796469f2e8b0b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645624"
---
# <a name="direct3d-surfaces-direct3d-9"></a>Superfícies do Direct3D (Direct3D 9)

Uma superfície representa uma área linear da memória de vídeo e geralmente reside na memória de vídeo do cartão de vídeo, embora as superfícies possam existir na memória do sistema. As superfícies são gerenciadas pela interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .

-   Buffer frontal. Um retângulo de memória que é convertido pelo adaptador gráfico e exibido no monitor. No Direct3D, um aplicativo nunca grava diretamente no buffer frontal.
-   Buffer de fundo. Um retângulo de memória no qual um aplicativo pode gravar diretamente. O buffer de fundo nunca é exibido diretamente no monitor.
-   Invertendo superfícies. O processo de mover o buffer de fundo para o buffer frontal.
-   Cadeia de permuta. Uma coleção de um ou mais buffers de back-end que podem ser exibidos em série para o buffer frontal.

## <a name="getting-a-surface"></a>Obtendo uma superfície

Crie uma superfície chamando qualquer um destes métodos:

-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)

Os formatos de superfície determinam como os dados de cada pixel na memória da superfície são interpretados. O Direct3D usa o membro [D3DFORMAT](d3dformat.md) da [**estrutura \_ desc de D3DSURFACE**](d3dsurface-desc.md) para descrever o formato da superfície. Você pode recuperar o formato de uma superfície existente chamando o método [**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc) .

Depois que uma superfície é criada, você pode obter um ponteiro para ela chamando qualquer um destes métodos:

-   [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface)
-   [**GetFrontBufferData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getfrontbufferdata)
-   [**GetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrendertarget)
-   [**GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
-   [**GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)

A interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) permite que você acesse a memória indiretamente por meio do método [**UpdateSurface**](/windows/desktop/api) . Esse método permite copiar uma região retangular de pixels de uma interface **IDirect3DSurface9** para outra interface **IDirect3DSurface9** . A interface de superfície também tem métodos para acessar diretamente a memória de vídeo. Por exemplo, você pode usar o método [**LockRect**](/windows/desktop/api) para bloquear uma região retangular de memória de exibição. É importante chamar [**UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) depois que você terminar de trabalhar com a região retangular bloqueada na superfície.

## <a name="additional-surface-topics"></a>Tópicos de superfície adicionais

Saiba mais sobre como usar superfícies com qualquer um destes tópicos:

-   [Formatos de superfície (Direct3D 9)](surface-formats.md)
-   [O que é uma cadeia de permuta? (Direct3D 9)](what-is-a-swap-chain-.md)
-   [Largura vs. pitch (Direct3D 9)](width-vs--pitch.md)
-   [Invertendo superfícies (Direct3D 9)](flipping-surfaces.md)
-   [Inversão de página e buffer de fundo (Direct3D 9)](page-flipping-and-back-buffering.md)
-   [Copiando para superfícies (Direct3D 9)](copying-to-surfaces.md)
-   [Copiando superfícies (Direct3D 9)](copying-surfaces.md)
-   [Acessando a memória da superfície diretamente (Direct3D 9)](accessing-surface-memory-directly.md)
-   [Dados de superfície privada (Direct3D 9)](private-surface-data.md)
-   [Controles gama (Direct3D 9)](gamma-controls.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 
