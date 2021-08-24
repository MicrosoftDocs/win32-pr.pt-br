---
description: Uma lista dos recursos disponíveis no Direct3D 10 está aqui. Esta página lista os recursos do Direct3D 9 que não têm mais suporte no Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Recursos preterido (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ce1750e6d8f98785bf87fb92169e56f0b4ca4e8a6dfdd34c6174a8c3087eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852766"
---
# <a name="deprecated-features-direct3d-10"></a>Recursos preterido (Direct3D 10)

Uma lista dos recursos disponíveis no Direct3D 10 está [aqui.](d3d10-graphics-programming-guide-api-features.md) Esta página lista os recursos do Direct3D 9 que não têm mais suporte no Direct3D 10.

As maiores alterações de recursos no Direct3D 10 são:

- O Direct3D 10 não dá mais suporte à transformação de função fixa e ao pipeline de iluminação.
- O Direct3D 10 não dá mais suporte ao blender de textura de função fixa (às vezes chamado de sombreador de pixel de função fixa).
- O Direct3D 10 implementa novas regras de rasterização, que são mais simples e mais limpas do que as regras GDI herdada implementadas no Direct3D 9. Por exemplo, não há mais suporte para o controle de último pixel para linhas.

Aqui está uma lista completa dos recursos no Direct3D 9 que foram preterido no Direct3D 10.

- **Combinação alfa.** A combinação alfa agora é programada independentemente da combinação de cores. O Direct3D 10 adiciona uma alternância alfa-blend-enable que está habilitada por padrão. Consulte [Objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obter mais informações.
- **Teste alfa.** O teste alfa é um comportamento de pixel de função fixa para Direct3D 9. O teste alfa é movido para sombreadores de pixel programáveis para Direct3D 10 e superior. Para obter informações sobre como emular a funcionalidade de teste alfa do Direct3D 9 no Direct3D 10 e superior, consulte o exemplo FixedFuncEMU no SDK do DirectX para junho [de 2010.](https://www.microsoft.com/download/en/details.aspx?id=6812)
- **Opções do modo Blend**. BOTHSRCALPHA foi removido do D3D10 BLEND, pois é \_ redundante com BOTHINVSRCALPHA. Confira [**D3D10 \_ BLEND**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) para obter mais informações.
- **Bloquear formatos de compactação**. Não há distinção entre alfa pré-multiplicado ou alfa não pré-multiplicado no Direct3D 10. Esses formatos direct3D 9 são mapeados para esses formatos direct3D 10: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2, DXT3  | BC2\*       |
    | DXT4, DXT5  | BC3\*       |

    

     

    Consulte [Compactação de bloco (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) para obter informações adicionais.

-   **Planos de clipe**. Em vez de usar planos de clipe, o Direct3D 10 implementa distâncias de corte e distâncias de replicação, com até oito componentes cada em até dois elementos de atributos de vértice. Consulte [Semantics (DirectX HLSL) para](../direct3dhlsl/dx-graphics-hlsl-semantics.md) obter informações adicionais. [A amostra FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação de planos de clipe no Direct3D 10.
-   **Dithering**. O Direct3D 10 não dá suporte à escrita de dados dithered em um destino de renderização.
-   **Pipeline de iluminação e transformação de função fixa em não disponível.** Em vez disso, você deve usar sombreadores. Consulte [Estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Blender de textura de função fixa (também chamado de sombreador de pixel de função fixa).** Em vez disso, você deve usar sombreadores. Consulte [Estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Os modos de preenchimento** foram alterados. O Direct3D 10 implementa os modos de preenchimento sólidos e de wireframe. O ponto D3DFILLMODE foi removido, use um sombreador de geometria para emular o modo de ponto, se necessário. [A amostra FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação de ponto D3DFILLMODE no Direct3D 10. Consulte [**D3D10 \_ FILL \_ MODE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) and [Shader Stages (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Formatar .** O hardware pode usar formatos expostos pela API. Os formatos de Luminance não são mais implementados.
-   **Filtragem de Mipmap.** Removeu a opção para selecionar o modo sem filtro. Em vez disso, use uma textura com apenas um único mipmap ou de definir o estado do amostrador MaxLOD como 0. Consulte [Objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obter informações adicionais.
-   **Paletas**. Em vez disso, os aplicativos devem usar uma leitura de textura dependente.
-   **Modelos de sombreador de pixel e vértice:** 1 \_ x, 2 \_ x e 3 \_ 0. O Direct3D 10 dá suporte ao modelo de sombreador 4. Consulte [Modelo de sombreador 4 para](../direct3dhlsl/dx-graphics-hlsl-sm4.md) obter informações adicionais.
-   **Sprites de ponto.** Em vez disso, use um sombreador de geometria. Consulte [Estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Regras de rasterização**. As regras de rasterização de linha GDI herdada são substituídas por regras mais simples e mais limpas. Não há mais suporte para o controle de último pixel para linhas. Consulte [Regras de rasterização (Direct3D 10) para](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) obter informações adicionais.
-   **Modos de sombrear**. D3DSHADEMODE (que suporta sombreamento simples/gouraud/phong) foi removido. O Direct3D 10 implementa dois modificadores de interpolação para saídas de sombreador de vértice. Consulte [Exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) para ver um exemplo de como emular os modos gouraud e sombreado simples do Direct3D 9 no Direct3D 10.
-   **instrução texldp.** Um aplicativo deve implementar uma carga de textura projetada com instruções HLSL extras. Consulte [Referência para HLSL para](../direct3dhlsl/dx-graphics-hlsl-reference.md) obter informações adicionais. [A amostra FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação de texldp no Direct3D 10.
-   **Não há mais suporte** para o estado de estágio de textura TCI (D3DTSS \_ TEXCOORDINDEX).
-   **Ventiladores de triângulo.** Um aplicativo deve converter triângulos-ventiladores existentes em listas de triângulos ou faixas de triângulo. Para emular alguns comportamentos usando DrawPrimitive em APIs mais antigas, tente usar DrawIndexed no Direct3D 10. Consulte [Topologias primitivas (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) para obter informações adicionais.
-   **W buffering**. O suporte a hardware não é garantido; É recomendável que um aplicativo use buffers de profundidade de alta precisão. Consulte [Configurando Depth-Stencil (Direct3D 10) para](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) obter informações adicionais.
-   **Modos de quebra (quebra** de coordenadas de textura). A quebra de endereço de textura (como wrap, espelho, fixação etc.) ainda existe. Consulte [**D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) e MODO DE ENDEREÇO DE [**TEXTURA D3D10 \_ \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos da API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
