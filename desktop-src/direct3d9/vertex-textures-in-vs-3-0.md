---
description: O modelo de sombreador de vértice 3.0 dá suporte à lookup de textura no sombreador de vértice usando a instrução de carregamento de textura texldl - vs.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Texturas de vértice vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4cbd4aa1e1830d29656fea2bc7b028191bee158eede119c9a47ae2457d10e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519438"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Texturas de vértice \_ em \_ versus 3 0 (DirectX HLSL)

O modelo de sombreador de vértice 3.0 dá suporte à lookup de textura no sombreador de vértice usando a instrução de carregamento [de textura texldl](../direct3dhlsl/texldl---vs.md) - vs. O mecanismo de vértice contém quatro estágios de amostra de textura, [chamados D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 e D3DVERTEXTEXTURESAMPLER3. Eles são diferentes do exemplo de mapa de deslocamento e dos amostradores de textura no mecanismo de pixel.

Para amostrar texturas definidas nesses quatro estágios, você pode usar o mecanismo de vértice e programar as fases com o [**método CheckDeviceFormat.**](/windows/desktop/api) Definir texturas nesses estágios usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), com o índice de estágio [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) até D3DVERTEXTEXTURESAMPLER3. Um novo registro foi introduzido no sombreador de vértice, o registro de amostra (como em ps 2 0), que representa o exemplo de textura \_ \_ de vértice. Esse registro precisa ser definido no sombreador antes de usá-lo.

Um aplicativo pode consultar se há suporte para um formato como uma textura de vértice chamando [**CheckDeviceFormat**](/windows/desktop/api) com [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE](d3dusage-query.md).

> [!Note]  
> Esse é um sinalizador de consulta para que ele não seja aceito em nenhuma função Createxxx. Uma textura de vértice criada no pool padrão pode ser definida como uma textura de pixel e vice-versa. No entanto, para usar o processamento de vértice de software, a textura do vértice deve ser criada no pool de rascunho (não importa se é um dispositivo de modo misto ou um dispositivo de processamento de vértice de software).

 

A funcionalidade é idêntica às texturas de pixel, exceto pelo seguinte:

-   Não há suporte para filtragem de textura anisodora, portanto, D3DSAMP MAXNESESOALTY é ignorado e \_ D3DTEXF ANIS TEXTURE não pode ser definido para lupa ou minificar para esses \_ estágios.
-   A taxa de informações de alteração não está disponível, portanto, o aplicativo precisa calcular o nível de detalhes e fornecer essas informações como um parâmetro para [o texldl – vs](../direct3dhlsl/texldl---vs.md).

As restrições incluem:

-   Assim como nos sombreadores de pixel, se há suporte para texturas multielemento, D3DSAMP ELEMENTINDEX é usado para descobrir de qual elemento \_ amostrar.
-   O estado D3DSAMP \_ DMAPOFFSET é ignorado para esses estágios.
-   Use [**CheckDeviceFormat**](/windows/desktop/api) com [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE"](d3dusage-query.md) para consultar uma textura para ver se ela pode ser usada como uma textura de vértice.
-   VertexTextureFilterCaps indica que tipo de filtros são permitidos nos amostradores de textura de vértice. [D3DPTFILTERCAPS \_ MINFANISFILTER e](d3dptfiltercaps.md) D3DPTFILTERCAPS \_ MAGFANISFILTER NÃO são permitidos.

## <a name="sampling-stage-registers"></a>Registros de estágio de amostragem

Um registro de estágio de amostragem identifica uma unidade de amostragem que pode ser usada em instruções de carregamento de textura. Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico da amostragem fornecido em [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).

Cada amostra identifica exclusivamente uma única superfície de textura que é definida como o sampler correspondente usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). No entanto, a mesma superfície de textura pode ser definida em vários exemplos.

Em tempo de desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.

Como o vs 3 0 dá suporte a quatro amostras, até quatro superfícies de textura podem ser lidas em uma única passagem \_ \_ de sombreador. Um registro de amostra pode aparecer apenas como um argumento na instrução de carregamento de textura: [texldl - vs](../direct3dhlsl/texldl---vs.md).

Em versus 3 0, se você usar um exemplo, ele deverá ser declarado no início do programa de sombreador, usando o \_ \_ [samplerType dcl \_ (sm3 – vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) (como em ps \_ 2 \_ 0).

## <a name="software-processing"></a>Processamento de software

Esse recurso terá suporte no processamento de vértice de software. Os tipos de filtro específicos com suporte podem ser verificados chamando [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) e verificando VertexTextureFilterCaps. Todos os formatos de textura publicados terão suporte como texturas de vértice no processamento de vértice de software.

Os aplicativos podem verificar se há suporte para um formato de textura específico no modo de processamento de vértice de software chamando [**CheckDeviceFormat**](/windows/desktop/api) e fornecendo (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) como uso. Todos os formatos têm suporte para processamento de vértice de software. O pool de rascunhos é necessário para o processamento de vértice de software.

## <a name="api-changes"></a>Alterações na API


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 
