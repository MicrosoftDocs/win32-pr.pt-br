---
title: Especificando destinos do compilador
description: Aqui, listamos os destinos de vários perfis que o D3DCompile \ Functions e o compilador HLSL suportam.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d020edaabf4c618b1fa911a91bc4cc0e8b37e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481832"
---
# <a name="specifying-compiler-targets"></a>Especificando destinos do compilador

Você precisa especificar o destino do sombreador — conjunto de recursos do sombreador — para compilar ao chamar a função [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)ou [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) . Aqui, listamos os destinos de vários perfis que as funções **D3DCompile \*** e o compilador HLSL suportam.

-   [Níveis de recurso do Direct3D 11,0 e 11,1](#direct3d-110-and-111-feature-levels)
-   [Nível de recurso do Direct3D 10,1](#direct3d-101-feature-level)
-   [Nível de recurso do Direct3D 10,0](#direct3d-100-feature-level)
-   [Níveis de recurso do Direct3D 9,1, 9,2 e 9,3](#direct3d-91-92-and-93-feature-levels)
-   [Modelo de sombreador Direct3D 9 herdado 3,0](#legacy-direct3d-9-shader-model-30)
-   [Modelo de sombreador Direct3D 9 herdado 2,0](#legacy-direct3d-9-shader-model-20)
-   [Modelo de sombreador do Direct3D 9 herdado 1. x](#legacy-direct3d-9-shader-model-1x)
-   [Efeitos herdados](#legacy-effects)
-   [Observações](#notes)
-   [Tópicos relacionados](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Níveis de recurso do Direct3D 11,0 e 11,1

Aqui estão os destinos do sombreador para os quais [os níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 11,0 e 11,1 dão suporte.



| Destino   | Descrição                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 5 \_ 0 | DirectCompute 5,0 ([sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| DS \_ 5 \_ 0 | [Sombreador de domínio](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| GS \_ 5 \_ 0 | [Sombreador de geometria](/previous-versions//bb205146(v=vs.85)) |
| HS \_ 5 \_ 0 | [Sombreador envoltória](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| PS \_ 5 \_ 0 | [Sombreador de pixel](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 5 \_ 0 | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Nível de recurso do Direct3D 10,1

Aqui estão os destinos de sombreador para os quais o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 10,1 dá suporte.



| Destino   | Descrição                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 1 | DirectCompute 4,1 ([sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 1 | [Sombreador de geometria](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 1 | [Sombreador de pixel](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 1 | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Nível de recurso do Direct3D 10,0

Aqui estão os destinos de sombreador para os quais o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 10,0 dá suporte.



| Destino   | Descrição                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| cs \_ 4 \_ 0 | DirectCompute 4,0 ([sombreador de computação](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 0 | [Sombreador de geometria](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 0 | [Sombreador de pixel](/previous-versions//bb205146(v=vs.85))          |
| vs \_ 4 \_ 0 | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Níveis de recurso do Direct3D 9,1, 9,2 e 9,3

Aqui estão os destinos do sombreador que [os níveis de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) do Direct3D 9,1, 9,2 e 9,3 dão suporte.

> [!Note]  
> Ao usar os \* \_ perfis de \_ sombreador HLSL de 4% do \_ nível \_ 9 \_ x, você usa implicitamente os perfis do [Shader Model 2. x](dx-graphics-hlsl-sm2.md) para dar suporte ao hardware compatível com Direct3D 9. Os perfis do modelo de sombreador 2. x dão suporte a um comportamento de controle de fluxo mais limitado que o [sombreador modelo 4. x](dx-graphics-hlsl-sm4.md) e perfis posteriores.

 




| Destino | Descrição | 
|--------|-------------|
| ps_4_0_level_9_1 | [Sombreador de pixel](/previous-versions//bb205146(v=vs.85)) para 9,1 e 9,2 (limites semelhantes a PS_2_0)<ul><li>64 instruções de textura aritméticas e 32</li><li>12 registros temporários</li><li>4 níveis de leituras dependentes</li></ul> | 
| ps_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Sombreador de pixel</a> para 9,3 (limites semelhantes a ps_2_x ² com recursos adicionais do sombreador)<ul><li>512 instruções</li><li>registros temporários de 32</li><li>Controle de fluxo estático (profundidade máxima de 4)</li><li>Controle de fluxo dinâmico (profundidade máxima de 24)</li><li>D3DPS20CAPS_ARBITRARYSWIZZLE</li><li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li><li>D3DPS20CAPS_PREDICATION</li><li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li><li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li></ul> | 
| vs_4_0_level_9_1 | <a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértice</a> para 9,1 e 9,2 (semelhante a VS_2_0)<ul><li>256 instruções</li><li>12 registros temporários</li><li>Controle de fluxo estático (profundidade máxima de 1)</li></ul> | 
| vs_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Sombreador de vértice</a> para 9,3 (semelhante a vs_2_a ² com recursos e instanciação adicionais do sombreador)<ul><li>256 instruções</li><li>registros temporários de 32</li><li>Controle de fluxo estático (profundidade máxima de 4)</li><li>D3DVS20CAPS_PREDICATION</li></ul> | 




 

## <a name="legacy-direct3d-9-shader-model-30"></a>Modelo de sombreador Direct3D 9 herdado 3,0

Aqui estão os alvos do sombreador para o modelo de sombreador do Direct3D 9 herdado 3,0 ³.



| Destino    | Descrição                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 3 \_ 0  | [Sombreador de Pixel](/previous-versions//bb205146(v=vs.85)) 3,0               |
| PS \_ 3 \_ SW | [Sombreador de Pixel](/previous-versions//bb205146(v=vs.85)) 3,0 (software)    |
| vs \_ 3 \_ 0  | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 3,0            |
| vs \_ 3 \_ SW | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 3,0 (software) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Modelo de sombreador Direct3D 9 herdado 2,0

Aqui estão os alvos do sombreador para o modelo de sombreador do Direct3D 9 herdado 2,0 ³.



| Destino    | Descrição                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 2 \_ 0  | [Sombreador de Pixel](/previous-versions//bb205146(v=vs.85)) 2,0             |
| PS \_ 2 \_ a  | [Sombreador de pixel](/previous-versions//bb205146(v=vs.85)) 2a              |
| PS \_ 2 \_ b  | [Sombreador de pixel](/previous-versions//bb205146(v=vs.85)) 2B              |
| PS \_ 2 \_ SW | Software do [pixel shader](/previous-versions//bb205146(v=vs.85)) 2,0    |
| vs \_ 2 \_ 0  | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 2,0          |
| vs \_ 2 \_ a  | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 2a           |
| vs \_ 2 \_ SW | Software de [sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 2,0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Modelo de sombreador do Direct3D 9 herdado 1. x

Aqui estão os alvos do sombreador para o modelo de sombreador do Direct3D 9 herdado 1. x ⁴.



| Destino   | Descrição                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TX \_ 1 \_ 0 | Perfil de sombreador de textura que herdado D3DX9 ⁵ Functions [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) e [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) use |
| vs \_ 1 \_ 1 | [Sombreador de vértice](/previous-versions//bb205146(v=vs.85)) 1,1                                                            |



 

## <a name="legacy-effects"></a>Efeitos herdados

Aqui estão os alvos de efeito para efeitos herdados.



| Destino   | Descrição                               |
|----------|-------------------------------------------|
| FX \_ 2 \_ 0 | Effects (FX) para o Direct3D 9 em D3DX9 ⁵     |
| FX \_ 4 \_ 0 | Effects (FX) para Direct3D 10,0 em D3DX10 ⁵ |
| FX \_ 4 \_ 1 | Effects (FX) para Direct3D 10,1 em D3DX10 ⁵ |
| FX \_ 5 \_ 0 | Effects (FX) para o Direct3D 11 ⁵             |



 

## <a name="notes"></a>Observações

Aqui estão algumas observações que as seções anteriores se referem a:

1.  os dispositivos 10,0 e 10,1 de [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) podem, opcionalmente, dar suporte a DirectCompute. Para verificar o suporte, use [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com o [**\_ recurso D3D11 \_ d3d10 \_ X \_ \_ Opções de hardware**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 requer efetivamente hardware que esteja em conformidade com os requisitos para o modelo de [sombreador do Direct3D 9 herdado 3,0](#legacy-direct3d-9-shader-model-30), mas esse nível de recurso não usa destinos vs \_ 3 \_ 0 ou PS \_ 3 \_ 0.
3.  Use apenas modelos de sombreador Direct3D 9 herdados com a API do Direct3D 9. Em vez disso, use os perfis 9. x com a API Direct3D 10. x e 11. x.
4.  As funções **D3DCompile \*** do sombreador HLSL atuais não dão suporte a sombreadores de pixel herdados 1. x. A última versão do HLSL para dar suporte a esses destinos foi D3DX9 na versão de outubro de 2006 do SDK do DirectX.
5.  Todas as versões do D3DX e do SDK do DirectX foram preteridas. Para obter mais informações, consulte [onde está o SDK do DirectX?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
