---
description: Um bloco de estado pode ser usado para capturar somente o estado de vértice (consulte estado de salvamento e restauração de blocos de estado (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Salvando Estados de vértice com um StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105796068"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a>Salvando Estados de vértice com um StateBlock (Direct3D 9)

Um bloco de estado pode ser usado para capturar somente o estado de vértice (consulte [estado de salvamento e restauração de blocos de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)). O estado a seguir é o estado do vértice:

-   Estado de renderização de vértice (consulte [pipeline de vértice: renderizar estado](#vertex-pipeline-render-state)).
-   Estado de amostra de vértice (consulte [pipeline de vértice: estado de amostra](#vertex-pipeline-sampler-state)).
-   Estado de textura de vértice (consulte [pipeline de vértice: estado de textura](#vertex-pipeline-texture-state)).
-   Os segmentos do modo NPatch de [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).
-   Cada luz de [**IDirect3DDevice9:: SetLight**](/windows/desktop/api), bem como se a luz está habilitada com [**IDirect3DDevice9:: clarear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).
-   O sombreador de vértice atual e cada uma das constantes de sombreador de vértice.
-   Para cada fluxo de vértice, armazene o valor de divisor de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   A declaração de vértice atual.

Para capturar o estado de vértice com um bloco de estado, especifique D3DSBT \_ vertexstate ao chamar [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="vertex-pipeline-render-state"></a>Pipeline de vértice: estado de renderização

Os Estados de renderização do dispositivo afetam o comportamento de quase todas as partes do pipeline. Os Estados de renderização são definidos chamando [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

A tabela a seguir inclui todos os Estados de renderização que configuram o estado de vértice:



| Processar Estados                           | Valor padrão          |
|-----------------------------------------|------------------------|
| D3DRS de \_ seleção                         | \_CCW D3DCULL           |
| D3DRS \_ FOGCOLOR                         | 0                      |
| D3DRS \_ FOGTABLEMODE                     | D3DFOG \_ nenhum           |
| D3DRS \_ FOGSTART                         | 0                      |
| D3DRS \_ FOGEND                           | 1                      |
| D3DRS \_ FOGDENSITY                       | 1                      |
| D3DRS \_ RANGEFOGENABLE                   | **FALSE**              |
| \_Ambiente D3DRS                          | 0                      |
| D3DRS \_ COLORVERTEX                      | **TRUE**               |
| D3DRS \_ FOGVERTEXMODE                    | D3DFOG \_ nenhum           |
| Recorte de D3DRS \_                         | **TRUE**               |
| \_Iluminação D3DRS                         | **TRUE**               |
| D3DRS \_ LOCALVIEWER                      | **TRUE**               |
| D3DRS \_ EMISSIVEMATERIALSOURCE           | MATERIAL de D3DMCS \_       |
| D3DRS \_ AMBIENTMATERIALSOURCE            | MATERIAL de D3DMCS \_       |
| D3DRS \_ DiffuseMaterialSource            | D3DMCS \_ COLOR1         |
| D3DRS \_ SPECULARMATERIALSOURCE           | D3DMCS \_ COLOR2         |
| D3DRS \_ VERTEXBLEND                      | D3DVBF \_ desabilitar        |
| D3DRS \_ CLIPPLANEENABLE                  | 0                      |
| Pontos de D3DRS \_                        | Dependente do driver       |
| D3DRS \_ pontos \_ mínimos                   | 1                      |
| D3DRS \_ POINTSPRITEENABLE                | **FALSE**              |
| D3DRS \_ POINTSCALEENABLE                 | **FALSE**              |
| D3DRS \_ POINTSCALE \_ A                    | 1                      |
| D3DRS \_ POINTSCALE \_ B                    | 0                      |
| D3DRS \_ POINTSCALE \_ C                    | 0                      |
| D3DRS \_ MULTISAMPLEANTIALIAS             | **TRUE**               |
| D3DRS \_ MULTISAMPLEMASK                  | 0xFFFFFFFF             |
| D3DRS \_ PATCHEDGESTYLE                   | D3DPATCHEDGE \_ discreto |
| D3DRS \_ pontos \_ máximos                   | 1                      |
| D3DRS \_ INDEXEDVERTEXBLENDENABLE         | **FALSE**              |
| D3DRS \_ TWEENFACTOR                      | 0                      |
| D3DRS \_ POSITIONDEGREE                   | D3DDEGREE \_ cúbico       |
| D3DRS \_ NORMALDEGREE                     | D3DDEGREE \_ linear      |
| D3DRS \_ MINTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ MAXTESSELLATIONLEVEL             | 1                      |
| D3DRS \_ ADAPTIVETESS \_ X                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Y                  | 0                      |
| D3DRS \_ ADAPTIVETESS \_ Z                  | 1                      |
| D3DRS \_ ADAPTIVETESS \_ W                  | 0                      |
| D3DRS \_ ENABLEADAPTIVETESSELLATION "/> | **FALSE**              |



 

## <a name="vertex-pipeline-sampler-state"></a>Pipeline de vértice: estado de amostra

Os Estados de amostra controlam tópicos relacionados à amostragem, como filtragem, divisão e modos de endereço de coordenadas de textura. Use [**IDirect3DDevice9:: Setamostrastate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar o estado de amostra (incluindo aquele usado na unidade Tessellator para mapas de deslocamento de exemplo). Os Estados de amostra foram renomeados com um prefixo "D3DSAMP \_ " para habilitar a detecção de erros de tempo de compilação ao portar do DirectX 8.

A tabela a seguir inclui todos os Estados de amostra que definem o estado do vértice:



| Estados de amostra      | Valor padrão |
|---------------------|---------------|
| D3DSAMP \_ DMAPOFFSET | 256           |



 

## <a name="vertex-pipeline-texture-state"></a>Pipeline de vértice: estado de textura

Os Estados de textura controlam as operações de mesclagem de textura do misturador de várias texturas. Use [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) para configurar Estados de textura. Use [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para associar uma textura a um estágio de amostra.

A tabela a seguir inclui todos os Estados de textura que configuram o estado de vértice:



| Estados de textura                | Valor padrão    |
|-------------------------------|------------------|
| D3DTSS \_ TEXCOORDINDEX         | 0                |
| D3DTSS \_ TEXTURETRANSFORMFLAGS | D3DTTFF \_ desabilitar |



 

D3DTSS \_ TEXCOORDINDEX é um estado de processamento de vértice de função fixo. Se um sombreador de vértice programável for usado, esse Estado será ignorado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estado de salvamento e restauração de blocos de estado](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
