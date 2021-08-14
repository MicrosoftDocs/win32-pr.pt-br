---
description: O modelo de sombreador de vértice 3,0 dá suporte à pesquisa de textura no sombreador de vértice usando a instrução texldl-vs de carregamento de textura.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Texturas de vértice no vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4cbd4aa1e1830d29656fea2bc7b028191bee158eede119c9a47ae2457d10e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519438"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Texturas de vértice no vs \_ 3 \_ 0 (DirectX HLSL)

O modelo de sombreador de vértice 3,0 dá suporte à pesquisa de textura no sombreador de vértice usando a instrução [texldl-vs](../direct3dhlsl/texldl---vs.md) de carregamento de textura. O mecanismo de vértice contém quatro estágios de amostra de textura, chamados [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md), D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 e D3DVERTEXTEXTURESAMPLER3. Eles são diferentes dos exemplos de amostra e textura de mapa de deslocamento no mecanismo de pixel.

Para exemplos de texturas definidas nesses quatro estágios, você pode usar o mecanismo de vértice e programar os estágios com o método [**CheckDeviceFormat**](/windows/desktop/api) . Defina texturas nesses estágios usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture), com o índice de estágio [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) por meio de D3DVERTEXTEXTURESAMPLER3. Um novo registro foi introduzido no sombreador de vértice, o registro de amostra (como no PS \_ 2 \_ 0), que representa a amostra de textura de vértice. Esse registro precisa ser definido no sombreador antes de usá-lo.

Um aplicativo pode consultar se há suporte para um formato como uma textura de vértice chamando [**CheckDeviceFormat**](/windows/desktop/api) com [D3DUSAGE de \_ consulta \_ VERTEXTEXTURE](d3dusage-query.md).

> [!Note]  
> Esse é um sinalizador de consulta para que não seja aceito em nenhuma função Createxxx. Uma textura de vértice criada no pool padrão pode ser definida como uma textura de pixel e vice-versa. No entanto, para usar o processamento de vértice de software, a textura de vértice deve ser criada no pool transitório (não importa se é um dispositivo de modo misto ou um dispositivo de processamento de vértice de software).

 

A funcionalidade é idêntica às texturas de pixel, exceto para o seguinte:

-   Não há suporte para a filtragem de textura anisotropic, portanto, D3DSAMP \_ MAXANISOTROPY é ignorado e D3DTEXF \_ anisotropic não pode ser definido para a ampliação ou reduzir para esses estágios.
-   A taxa de informações de alteração não está disponível, portanto, o aplicativo precisa calcular o nível de detalhes e fornecer essas informações como um parâmetro para [texldl-vs](../direct3dhlsl/texldl---vs.md).

As restrições incluem:

-   Como em sombreadores de pixel, se as texturas de Multielemento tiverem suporte, D3DSAMP \_ ELEMENTINDEX será usado para descobrir a qual elemento criar amostra.
-   O estado D3DSAMP \_ DMAPOFFSET é ignorado para esses estágios.
-   Use [**CheckDeviceFormat**](/windows/desktop/api) com [D3DUSAGE \_ Query \_ VERTEXTEXTURE "](d3dusage-query.md) para consultar uma textura para ver se ela pode ser usada como uma textura de vértice.
-   VertexTextureFilterCaps indica que tipo de filtros são permitidos nos exemplos de textura de vértice. [D3DPTFILTERCAPS \_ MINFANISOTROPIC](d3dptfiltercaps.md) e D3DPTFILTERCAPS \_ MAGFANISOTROPIC não são permitidos.

## <a name="sampling-stage-registers"></a>Registros de estágio de amostragem

Um registro de estágio de amostragem identifica uma unidade de amostragem que pode ser usada em instruções de carregamento de textura. Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico de amostragem fornecido em [**Setsamplestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate).

Cada amostra identifica exclusivamente uma superfície de textura única que é definida como a amostra correspondente usando [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). No entanto, a mesma superfície de textura pode ser definida em vários exemplos.

No momento do desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.

Como o vs \_ 3 \_ 0 dá suporte a quatro amostragens, até quatro superfícies de textura podem ser lidas em uma única passagem de sombreador. Um registro de amostra pode aparecer apenas como um argumento na instrução de carga de textura: [texldl-vs](../direct3dhlsl/texldl---vs.md).

No vs \_ 3 \_ 0, se você usar uma amostra, ela deverá ser declarada no início do programa do sombreador, usando o [ \_ SampleType de DCL (SM3-vs ASM)](../direct3dhlsl/dcl-samplertype---vs.md) (como no PS \_ 2 \_ 0).

## <a name="software-processing"></a>Processamento de software

Esse recurso terá suporte no processamento de vértice de software. Os tipos de filtro específicos com suporte podem ser verificados chamando [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) e verificando VertexTextureFilterCaps. Todos os formatos de textura publicados terão suporte como texturas de vértice no processamento de vértice de software.

Os aplicativos podem verificar se há suporte para um formato de textura específico no modo de processamento de vértice de software chamando [**CheckDeviceFormat**](/windows/desktop/api) e fornecendo (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md)) como uso. Todos os formatos têm suporte para o processamento de vértice de software. O pool transitório é necessário para o processamento de vértice de software.

## <a name="api-changes"></a>Alterações de API


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

 

 
