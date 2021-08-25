---
description: Os recursos a seguir foram alterados no Microsoft Direct3D 9. Se você estiver usando esses recursos, consulte as alterações listadas abaixo para ajudá-lo a porportar seu aplicativo para o Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Convertendo em Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf5ec812ede4e9d5d356d36b01bbcfcc7732fdb5946e2a13af90c9d9428fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850526"
---
# <a name="converting-to-direct3d-9"></a>Convertendo em Direct3D 9

Os recursos a seguir foram alterados no Microsoft Direct3D 9. Se você estiver usando esses recursos, consulte as alterações listadas abaixo para ajudá-lo a porportar seu aplicativo para o Direct3D 9.

-   [Alterações de BaseVertexIndex](#basevertexindex-changes)
-   [Alterações de CreateImageSurface](#createimagesurface-changes)
-   [D3DENUM \_ NO \_ WHQL \_ LEVEL Changes](/windows)
-   [Criar alterações de recurso](#create-resource-changes)
-   [Alterações de EnumAdapterModes](#enumadaptermodes-changes)
-   [Alterações get/SetStreamSource \_](#getsetstreamsource-changes)
-   [Alterações de qualidade de multisampling](#multisampling-quality-changes)
-   [Alterações de ResourceManagerDiscardBytes](#resourcemanagerdiscardbytes-changes)
-   [Alterações de SetSoftwareVertexProcessing](#setsoftwarevertexprocessing-changes)
-   [Alterações de amostra de textura](#texture-sampler-changes)
-   [Alterações de declaração de vértice](#vertex-declaration-changes)
-   [Intervalos \_ e \_ alterações swapEffects \_](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>Alterações de BaseVertexIndex

No DirectX 8.x, IDirect3DDevice8::SetIndices exigia um ponteiro para o buffer de índice e um BaseVertexIndex para a posição inicial no buffer de vértice. Um aplicativo que faz o lote de objetos diferentes no buffer de vértice precisava alternar o buffer de índice (ou fazer uma chamada para IDirect3DDevice8::SetIndices) antes de chamar IDirect3DDevice8::D rawIndexedPrimitive.

No Direct3D 9, a posição inicial no buffer de vértice, *BaseVertexIndex,* foi movida para IDirect3DDevice9::D rawIndexedPrimitive e seu tipo de dados foi alterado de um DWORD para um INT.


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a>Alterações de CreateImageSurface

IDirect3DDevice8::CreateImageSurface foi renomeado [**como CreateOffscreenPlainSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface) Um parâmetro adicional que aceita um tipo D3DPOOL foi adicionado. D3DPOOL SCRATCH retornará uma superfície que tem características idênticas a uma superfície criada por \_ IDirect3DDevice8::CreateImageSurface. D3DPOOL \_ DEFAULT é o pool apropriado para uso com [**StretchRect**](/windows/desktop/api) e [**ColorFill.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill)

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ NO \_ WHQL \_ LEVEL Changes

Os aplicativos agora têm que solicitar explicitamente o WHQL (Hardware Quality Labs) do Microsoft Windows porque a resposta leva relativamente tempo (alguns segundos). D3DENUM \_ NO \_ WHQL \_ LEVEL foi removido e D3DENUM \_ WHQL \_ LEVEL foi adicionado.

## <a name="create-resource-changes"></a>Criar alterações de recurso

Um handle foi adicionado a vários métodos e deve ser definido como **NULL.** Os métodos afetados incluem:

-   [**Createtexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**Createvertexbuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>Alterações de EnumAdapterModes

O [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) agora tem um D3DFORMAT.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



O formato dá suporte a um conjunto em expansão de modos de exibição. Para proteger os aplicativos contra a enumeração de formatos que não foram apagados quando o aplicativo é enviado, o aplicativo deve dizer ao Direct3D o formato para os modos de exibição que devem ser enumerados. A matriz resultante de modos de exibição será diferente apenas por largura, altura e taxa de atualização.

O aplicativo especifica um formato de pixel e a enumeração é restrita aos modos de exibição que exatamente corresponderem ao formato. Veja a seguir uma lista dos formatos permitidos:

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

A enumeração é equivalente para versões alfa e nãonalpha do mesmo formato. O Formato retornado sempre será preenchido com o mesmo formato fornecido pelo aplicativo.

Esse método trata 565 e 555 como equivalente e retorna a versão correta no Formato. A diferença entra em vigor somente quando o aplicativo bloqueia o buffer de fundo e há um sinalizador explícito que o aplicativo deve definir para fazer isso.

## <a name="getsetstreamsource-changes"></a>Alterações get/SetStreamSource

Um parâmetro foi adicionado aos métodos [**GetStreamSource**](/windows/desktop/api) e [**SetStreamSource.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) O deslocamento é o número de bytes entre o início do fluxo e o início dos dados de vértice. É medido em bytes. Isso permite que o pipeline seja suportado por deslocamentos de fluxo. Para descobrir se o dispositivo dá suporte a deslocamentos de fluxo, consulte D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Alterações de qualidade de multisampling

Anteriormente, havia apenas a enumeração D3DMULTISAMPLE \_ TYPE. O Direct3D 9 retém essa enumeração e adiciona a ideia de um nível de qualidade para cada elemento da enumeração. O nível de qualidade indica uma troca entre a qualidade visual e o desempenho indicando o número de amostras mascaradas (no sentido de D3DRS \_ MULTISAMPLEMASK).

Um aplicativo deve escolher quantas amostras mascaradas ele precisa e, em seguida, consultar pQualityLevels. Se não for zero, esse valor indicará o número de níveis de qualidade que o aplicativo pode passar para as várias funções de criação por meio de MultiSampleQuality. Como os drivers expõem todos os esquemas multisamplo como níveis de qualidade em D3DMULTISAMPLE NONMASKABLE, você pode enumerar todos os esquemas de multisampling disponíveis por meio desse tipo se o aplicativo não precisar mascarar \_ exemplos.

O bit de caps D3DPRASTERCAPS \_ STRETCHBLTMULTISAMPLE foi retirado. Esse bit usado para significar que o método multisampling não suportava máscaras de gravação e não podia ser alternado entre [**BeginScene**](/windows/desktop/api) e [**EndScene.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) Esses métodos não maskable agora são expostos por meio de D3DMULTISAMPLE \_ NONMASKABLE.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Há um máximo diferente para cada número de amostras maskáveis. Por exemplo, D3DMULTISAMPLE 4 SAMPLES pode ter três níveis de qualidade, enquanto \_ \_ D3DMULTISAMPLE \_ 2 SAMPLES pode ter apenas \_ um. Há no máximo oito níveis de qualidade para cada número de amostras mascaradas (o driver não tem permissão para expressar mais). A qualidade varia de zero a ( \* pQualityLevels - 1).

## <a name="resourcemanagerdiscardbytes-changes"></a>Alterações de ResourceManagerDiscardBytes

ResourceManagerDiscardBytes foi substituído por IDirect3DDevice9::EvictManagedResources. Ele pode despejar todos os recursos, o Direct3D e os recursos do driver.

O gerenciador de recursos agora é consultado quando um recurso (gerenciado ou não gerenciado) falha na criação porque há memória de vídeo insuficiente. O gerente será solicitado automaticamente a liberar recursos suficientes para que a criação seja bem-sucedida. No DirectX 8.0, esse não era um processo automatizado.

## <a name="setsoftwarevertexprocessing-changes"></a>Alterações de SetSoftwareVertexProcessing

Um aplicativo pode criar um dispositivo de modo misto para usar o processamento de vértice de hardware e software.

Para alternar entre os dois modos de processamento de vértice no DirectX 8.x, chame IDirect3DDevice8::SetRenderState. Isso foi substituído por [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) para facilitar os problemas causados por blocos de estado. Esse novo método não é registrado por blocos de estado.

## <a name="texture-sampler-changes"></a>Alterações de amostra de textura

O Direct3D 9 dá suporte a até 16 superfícies de textura em uma passagem usando o modelo de sombreador de pixel 2 0; no entanto, o número de coordenadas de textura permanece limitado \_ a oito. O estado do estágio de textura está associado a superfícies, conjuntos de coordenadas, processamento de vértice e processamento de pixel. Para gerenciar essas diferenças no tempo de compilação, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) foi dividido em dois métodos:

-   IDirect3DDevice9::SetTextureStageState ainda será usado para o estado da coordenada de textura, como modos de wrap e geração de coordenadas de textura.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) foi adicionado e agora será usado para filtragem, peças, fixação, MIPLOD e assim por diante. Isso funcionará para até 16 amostras.

### <a name="settexturestagestate-changes"></a>Alterações de SetTextureStageState

IDirect3DDevice9::SetTextureStageState agora define os seguintes estados:

-   Corrigido o estado de processamento de vértice de função. Esse estado controla a manipulação de coordenadas de textura DE TEXTURA D3DTSS \_ TEXTURETRANSFORMFLAGS e D3DTSS \_ TEXCOORDINDEX. Até oito de cada um pode ser definido (porque oito coordenadas de textura são sempre suportadas). D3DTSS \_ TEXCOORDINDEX é um estado de processamento de vértice de função fixo. Se um sombreador de vértice programável for usado, esse Estado será ignorado.
-   Estado do sombreador do pixel da função fixa (o TextureStageState herdado).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   D3DTSS \_ BUMPENVLOFFSET
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ COLOROP
    -   D3DTSS \_ RESULTARG

    O número de Estados de sombreador de pixel de função fixa que pode ser definido é menor ou igual ao número representado por MaxTextureBlendStages.

O número de amostragens de textura disponíveis para o aplicativo é determinado pela versão do sombreador de pixel, conforme indicado na tabela a seguir.



| Nome                    | Número                                                         |
|-------------------------|----------------------------------------------------------------|
| PS \_ 1 \_ 1 para PS \_ 1 \_ 3    | 4 amostragens de textura                                             |
| PS \_ 1 \_ 4                | 6 amostras de textura                                             |
| PS \_ 2 \_ 0                | 16 classificadores de textura                                            |
| pipeline de função fixa | Exemplos de textura de MaxTextureBlendStages/MaxSimultaneousTextures |



 

Os dispositivos que dão suporte ao mapeamento de deslocamento no Direct3D 9 oferecerão suporte a uma amostra adicional (D3DDMAPSAMPLER), que amostra os mapas de deslocamento na unidade Tessellator.

### <a name="setsamplerstate-changes"></a>Alterações de setsamplestate

IDirect3DDevice9:: setamostrastate define o estado de amostra (incluindo o usado na unidade Tessellator para mapas de deslocamento de exemplo). Elas foram renomeadas com um prefixo D3DSAMP \_ para habilitar a detecção de erros em tempo de compilação ao portar do DirectX 8. x. Os Estados incluem:

-   Endereço de D3DSAMP \_
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   \_BORDERCOLOR D3DSAMP
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   D3DSAMP \_ MIPFILTER
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>Alterações de declaração de vértice

As declarações de vértice agora são dissociadas da criação do sombreador de vértice. As declarações de vértice agora usam uma interface de Component Object Model (COM).

Para o DirectX 8. x, as declarações de vértice são vinculadas a sombreadores de vértice.

-   Para o pipeline de função fixa, chame [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) com o código de FVF (formato de vértice flexível) do buffer de vértice.
-   Para sombreadores de vértice, chame IDirect3DDevice9:: SetVertexShader com um identificador para um sombreador de vértice criado anteriormente. O sombreador inclui uma declaração de vértice.

Para o Direct3D 9, as declarações de vértice são dissociadas de sombreadores de vértice e podem ser usadas com o pipeline de função fixa ou com sombreadores.

-   Para o pipeline de função fixa, não é necessário chamar IDirect3DDevice9:: SetVertexShader. Se, no entanto, você quiser alternar para o pipeline de função fixa e tiver usado anteriormente um sombreador de vértice, chame IDirect3DDevice9:: SetVertexShader (**NULL**). Quando isso for feito, você ainda precisará chamar [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) para declarar o código FVF.
-   Ao usar sombreadores de vértice, chame IDirect3DDevice9:: SetVertexShader com o objeto de sombreador de vértice. Além disso, chame IDirect3DDevice9:: SetFVF para configurar uma declaração de vértice. Isso usa as informações implícitas no FVF. [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) pode ser chamado em vez de IDirect3DDevice9:: SetFVF porque oferece suporte a declarações de vértice que não podem ser expressas com um FVF.

## <a name="intervals-and-swapeffects-changes"></a>Intervalos e alterações SwapEffectss

Várias alterações foram feitas para dar ao usuário mais controle sobre a taxa de atualização do monitor, a taxa de apresentação e o buffer de frente e para o desenho de buffer de fundo. Elas são as seguintes:

-   Um efeito de permuta foi removido, D3DSWAPEFFECT \_ cópia \_ vsync e uma taxa de apresentação, taxa de D3DPRESENT \_ \_ ilimitada.
-   Parâmetros D3DPRESENT renomeados \_ . Tela inteira \_ PresentationInterval para PresentationIntervals.
-   Intervalo D3DPRESENT \_ adicionado \_ imediatamente, o que significa que a apresentação não está sincronizada com a sincronização vertical. Como no DirectX 8. x, o \_ padrão de intervalo D3DPRESENT \_ é definido como zero e é equivalente a D3DPRESENT \_ intervalo \_ um. \_ \_ O padrão de intervalo D3DPRESENT é uma conveniência para inicializar \_ parâmetros de D3DPRESENT para zero.

Para obter uma explicação detalhada dos modos e dos intervalos com suporte, consulte D3DPRESENT.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gráficos do Direct3D 9](dx9-graphics.md)
</dt> </dl>

 

 
