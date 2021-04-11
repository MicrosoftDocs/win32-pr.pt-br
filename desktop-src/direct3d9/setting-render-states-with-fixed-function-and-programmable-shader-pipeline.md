---
title: Definir o estado do dispositivo na função fixa, pipelines de sombreador
description: Esta seção fornece as principais diferenças entre a configuração do estado do dispositivo com a função Fixed e o pipeline do sombreador programável.
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2d5c0e0ba9e1ac890468654d348b0f8b316f64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163886"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>Definir o estado do dispositivo na função fixa, pipelines de sombreador

Esta seção fornece as principais diferenças entre a configuração do estado do dispositivo com a função Fixed e o pipeline do sombreador programável.

Aqui estão os Estados do dispositivo que você pode definir apenas para um pipeline de função fixa:

-   Transformação de função fixa e iluminação: [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) com D3DRS \_ shadmode, D3DRS \_ SPECULARENABLE, D3DRS \_ Lighting, D3DRS \_ ambiente, D3DRS \_ COLORVERTEX, \_ D3DRS LOCALVIEWER, D3DRS \_ NORMALIZENORMALS, D3DRS \_ DiffuseMaterialSource, D3DRS \_ SPECULARMATERIALSOURCE, D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE, D3DRS \_ VERTEXBLEND, D3DRS \_ INDEXEDVERTEXBLENDENABLE, D3DRS \_ TWEENFACTOR, [**IDirect3DDevice9:: clareable**](/windows/desktop/api), IDirect3DDevice9 [**:: MultiplyTransform**](/windows/desktop/api), [**IDirect3DDevice9:**](/windows/desktop/api): SetTransform. [**SetFVF:: setleve**](/windows/desktop/api), [**IDirect3DDevice9:: SetMaterial**](/windows/desktop/api), [**IDirect3DDevice9:**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
-   Sombreador de pixel de função fixa: [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) com D3DRS \_ TEXTUREFACTOR, [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   Neblina: [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) com D3DRS \_ FOGENABLE, D3DRS \_ FOGCOLOR, D3DRS \_ FOGTABLEMODE, D3DRS \_ FOGSTART, D3DRS \_ FOGEND, D3DRS \_ FOGDENSITY, D3DRS \_ RANGEFOGENABLE, D3DRS \_ FOGVERTEXMODE

Aqui estão os Estados de renderização de dispositivo que você pode definir com [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para pipelines de sombreador de função fixa e programável:

-   Processar estado de destino: D3DRS \_ COLORWRITEENABLE, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2, D3DRS \_ COLORWRITEENABLE3, D3DRS \_ SRGBWRITEENABLE
-   Estado de profundidade: D3DRS \_ ZENABLE, D3DRS \_ ZWRITEENABLE, D3DRS \_ ZFUNC, D3DRS \_ SLOPESCALEDEPTHBIAS, D3DRS \_ DEPTHBIAS
-   Estado do estêncil: D3DRS \_ STENCILENABLE, D3DRS \_ STENCILFAIL, D3DRS \_ STENCILZFAIL, D3DRS \_ STENCILPASS, D3DRS \_ STENCILFUNC, D3DRS \_ STENCILREF, D3DRS \_ STENCILMASK, D3DRS \_ STENCILWRITEMASK, D3DRS \_ TWOSIDEDSTENCILMODE, D3DRS \_ CCW \_ STENCILFAIL, D3DRS CCW STENCILZFAIL \_ \_ , D3DRS \_ CCW \_ STENCILPASS, D3DRS \_ CCW \_ STENCILFUNC
-   Combinação alfa: D3DRS \_ SRCBLEND, D3DRS \_ DESTBLEND, D3DRS \_ BLENDOP, D3DRS \_ BLENDFACTOR, D3DRS \_ SEPARATEALPHABLENDENABLE, D3DRS \_ SRCBLENDALPHA, D3DRS \_ DESTBLENDALPHA, D3DRS \_ BLENDOPALPHA
-   Teste alfa: D3DRS \_ ALPHATESTENABLE, D3DRS \_ ALPHAREF, D3DRS \_ ALPHAFUNC
-   Estado do rasterizador: D3DRS \_ FillMode, D3DRS \_ LASTPIXEL, D3DRS \_ DITHERENABLE (superfícies de 16 bits)
-   Remoção: D3DRS de \_ seleção
-   Recorte: \_ recorte de D3DRS, D3DRS \_ CLIPPLANEENABLE
-   Tesoura: D3DRS \_ SCISSORTESTENABLE
-   Amostragens de textura: D3DRS \_ WRAP0, D3DRS \_ WRAP1, D3DRS \_ WRAP2, D3DRS \_ WRAP3, D3DRS \_ WRAP4, D3DRS \_ WRAP5, D3DRS \_ WRAP6, D3DRS \_ WRAP7, D3DRS \_ WRAP8, D3DRS \_ WRAP9, D3DRS \_ WRAP10, D3DRS \_ WRAP11, D3DRS \_ WRAP12, D3DRS \_ WRAP13, D3DRS \_ WRAP14, D3DRS \_ WRAP15
-   Suavização de serrilhado: D3DRS \_ MULTISAMPLEANTIALIAS, D3DRS \_ MULTISAMPLEMASK, D3DRS \_ ANTIALIASEDLINEENABLE
-   Ponto Sprite: D3DRS \_ Pointe, D3DRS \_ indica \_ min, D3DRS \_ POINTSPRITEENABLE, D3DRS \_ pontos MAXD3DRS \_ \_ POINTSCALEENABLE, D3DRS \_ POINTSCALE \_ A, D3DRS \_ POINTSCALE \_ B, D3DRS \_ POINTSCALE \_ C
-   N-patches: D3DRS \_ PATCHEDGESTYLE, D3DRS \_ POSITIONDEGREE, D3DRS \_ NORMALDEGREE, D3DRS \_ MINTESSELLATIONLEVEL, D3DRS \_ MAXTESSELLATIONLEVEL, D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z, D3DRS \_ ADAPTIVETESS \_ W, D3DRS \_ ENABLEADAPTIVETESSELLATION

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 
