---
description: Um bloco de estado pode ser usado para capturar somente o estado de pixel (consulte estado de salvamento e restauração de blocos de estado (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Salvando o estado de pixel com um StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500634"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Salvando o estado de pixel com um StateBlock (Direct3D 9)

Um bloco de estado pode ser usado para capturar somente o estado de pixel (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)). O estado a seguir é o estado de pixel:

-   Estado de renderização de pixel (consulte [pipeline de pixel: renderizar estado](#pixel-pipeline-render-state)).
-   Estado de textura de pixel (consulte [pipeline de pixel: estado de textura](#pixel-pipeline-texture-state)).
-   Estado de amostra de pixel (consulte [pipeline de pixel: estado de amostra](#pixel-pipeline-sampler-state)).
-   O sombreador de pixel atual e cada uma das constantes do sombreador de pixel.

Para capturar o estado de pixel com um bloco de estado, especifique D3DSBT \_ pixelstate ao chamar [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Pipeline de pixel: estado de renderização

Os Estados de renderização do dispositivo afetam o comportamento de quase todas as partes do pipeline. Os Estados de renderização são definidos chamando [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

A tabela a seguir inclui todos os Estados de renderização que configuram o estado de pixel:



| Processar Estados                              | Valor padrão      |
|--------------------------------------------|--------------------|
| D3DRS \_ ZENABLE                             | D3DZB \_ false       |
| D3DRS \_ SPECULARENABLE                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_ sólido     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE \_ GOURAUD  |
| D3DRS \_ ZWRITEENABLE                        | **TRUE**           |
| D3DRS \_ ALPHATESTENABLE                     | **FALSE**          |
| D3DRS \_ LASTPIXEL                           | **TRUE**           |
| D3DRS \_ SRCBLEND                            | D3DBLEND \_ um      |
| D3DRS \_ DESTBLEND                           | D3DBLEND \_ zero     |
| D3DRS \_ ZFUNC                               | D3DCMP \_ LESSEQUAL  |
| D3DRS \_ ALPHAREF                            | 0                  |
| D3DRS \_ ALPHAFUNC                           | D3DCMP \_ sempre     |
| D3DRS \_ DITHERENABLE                        | **FALSE**          |
| D3DRS \_ FOGSTART                            | 0                  |
| D3DRS \_ FOGEND                              | 1                  |
| D3DRS \_ FOGDENSITY                          | 1                  |
| D3DRS \_ ALPHABLENDENABLE                    | **FALSE**          |
| D3DRS \_ DEPTHBIAS                           | 0                  |
| D3DRS \_ STENCILENABLE                       | **FALSE**          |
| D3DRS \_ STENCILFAIL                         | D3DSTENCILOP \_ manter |
| D3DRS \_ STENCILZFAIL                        | D3DSTENCILOP \_ manter |
| D3DRS \_ STENCILPASS                         | D3DSTENCILOP \_ manter |
| D3DRS \_ STENCILFUNC                         | D3DCMP \_ sempre     |
| D3DRS \_ STENCILREF                          | 0                  |
| D3DRS \_ STENCILMASK                         | 0xFFFFFFFF         |
| D3DRS \_ STENCILWRITEMASK                    | 0xFFFFFFFF         |
| D3DRS \_ TEXTUREFACTOR                       | 0xFFFFFFFF         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| D3DRS \_ WRAP3                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| D3DRS \_ WRAP5                               | 0                  |
| D3DRS \_ WRAP6                               | 0                  |
| D3DRS \_ WRAP7                               | 0                  |
| D3DRS \_ WRAP8                               | 0                  |
| D3DRS \_ WRAP9                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| D3DRS \_ WRAP14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ LOCALVIEWER                         | **TRUE**           |
| D3DRS \_ EMISSIVEMATERIALSOURCE              | MATERIAL de D3DMCS \_   |
| D3DRS \_ AMBIENTMATERIALSOURCE               | MATERIAL de D3DMCS \_   |
| D3DRS \_ DiffuseMaterialSource               | D3DMCS \_ COLOR1     |
| D3DRS \_ SPECULARMATERIALSOURCE              | D3DMCS \_ COLOR2     |
| D3DRS \_ COLORWRITEENABLE                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ Adicionar    |
| D3DRS \_ SCISSORTESTENABLE                   | **FALSE**          |
| D3DRS \_ SLOPESCALEDEPTHBIAS                 | 0                  |
| D3DRS \_ ANTIALIASEDLINEENABLE               | **FALSE**          |
| D3DRS \_ TWOSIDEDSTENCILMODE                 | **FALSE**          |
| D3DRS \_ CCW \_ STENCILFAIL                    | D3DSTENCILOP \_ manter |
| D3DRS \_ CCW \_ STENCILZFAIL                   | D3DSTENCILOP \_ manter |
| D3DRS \_ CCW \_ STENCILPASS                    | D3DSTENCILOP \_ manter |
| D3DRS \_ CCW \_ STENCILFUNC                    | D3DCMP \_ sempre     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ BLENDFACTOR                         | 0xFFFFFFFF         |
| D3DRS \_ SRGBWRITEENABLE                     | 0                  |
| D3DRS \_ SEPARATEALPHABLENDENABLE            | **FALSE**          |
| D3DRS \_ SRCBLENDALPHA                       | D3DBLEND \_ um      |
| D3DRS \_ DESTBLENDALPHA                      | D3DBLEND \_ zero     |
| D3DRS \_ BLENDOPALPHA                        | D3DBLENDOP \_ Adicionar    |



 

## <a name="pixel-pipeline-sampler-state"></a>Pipeline de pixel: estado de amostra

Os Estados de amostra controlam tópicos relacionados à amostragem, como filtragem, divisão e modos de endereço de coordenadas de textura. Use [**IDirect3DDevice9:: Setamostrastate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar o estado de amostra (incluindo aquele usado na unidade Tessellator para mapas de deslocamento de exemplo). Os Estados de amostra foram renomeados com um prefixo "D3DSAMP \_ " para habilitar a detecção de erros de tempo de compilação ao portar do DirectX 8.

A tabela a seguir inclui todos os Estados de amostra que configuram o estado de pixel:



| Estados de amostra         | Valor padrão     |
|------------------------|-------------------|
| Endereço de D3DSAMP \_      | \_Encapsulamento de D3DTADDRESS |
| D3DSAMP \_ ADDRESSV      | \_Encapsulamento de D3DTADDRESS |
| D3DSAMP \_ ADDRESSW      | \_Encapsulamento de D3DTADDRESS |
| \_BORDERCOLOR D3DSAMP   | 0x00000000        |
| D3DSAMP \_ MAGFILTER     | Ponto de D3DTEXF \_    |
| D3DSAMP \_ MINFILTER     | Ponto de D3DTEXF \_    |
| D3DSAMP \_ MIPFILTER     | D3DTEXF \_ nenhum     |
| D3DSAMP \_ MIPMAPLODBIAS | 0                 |
| D3DSAMP \_ MAXMIPLEVEL   | 0                 |
| D3DSAMP \_ MAXANISOTROPY | 1                 |
| D3DSAMP \_ SRGBTEXTURE   | 0                 |
| D3DSAMP \_ ELEMENTINDEX  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Pipeline de pixel: estado de textura

Os Estados de textura controlam as operações de mesclagem de textura do misturador de várias texturas. Use [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) para configurar Estados de estágio de textura. Use [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para associar uma textura a um estágio de amostra.

A tabela a seguir inclui todos os Estados de textura que configuram o estado de pixel:



| Estados de textura                | Valor padrão    |
|-------------------------------|------------------|
| D3DTSS \_ COLOROP               | D3DTOP \_ desabilitar  |
| D3DTSS \_ COLORARG1             | \_Textura D3DTA   |
| D3DTSS \_ COLORARG2             | D3DTA \_ atual   |
| D3DTSS \_ ALPHAOP               | D3DTOP \_ desabilitar  |
| D3DTSS \_ ALPHAARG1             | \_Textura D3DTA   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ atual   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ BUMPENVLSCALE         | 0                |
| D3DTSS \_ BUMPENVLOFFSET        | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | D3DTTFF \_ desabilitar |
| D3DTSS \_ COLORARG0             | D3DTA \_ atual   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ atual   |
| D3DTSS \_ RESULTARG             | D3DTA \_ atual   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estado de salvamento e restauração de blocos de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
