---
description: Uma lista dos recursos disponíveis no Direct3D 10 está aqui. Esta página lista os recursos do Direct3D 9 que não têm mais suporte no Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Recursos preteridos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bb06738f046b92290d35cff180f3879f4fa737
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335540"
---
# <a name="deprecated-features-direct3d-10"></a>Recursos preteridos (Direct3D 10)

Uma lista dos recursos disponíveis no Direct3D 10 está [aqui](d3d10-graphics-programming-guide-api-features.md). Esta página lista os recursos do Direct3D 9 que não têm mais suporte no Direct3D 10.

As maiores alterações de recursos no Direct3D 10 são:

- O Direct3D 10 não dá mais suporte ao pipeline de transformação e iluminação de função fixa.
- O Direct3D 10 não dá mais suporte ao misturador de textura de função fixa (às vezes chamado de sombreador de pixel de função fixa).
- O Direct3D 10 implementa novas regras de rasterização, que são mais simples e limpas do que as regras GDI herdadas que são implementadas no Direct3D 9. Por exemplo, não há mais suporte para o controle de último pixel para linhas.

Aqui está uma lista completa dos recursos do Direct3D 9 que foram preteridos no Direct3D 10.

- **Combinação alfa**. A mistura alfa agora é programada independentemente da mistura de cores. O Direct3D 10 adiciona uma alternância alfa-Blend-Enable, que é habilitada por padrão. Consulte [objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obter mais informações.
- **Teste alfa**. O teste alfa é um comportamento de pixel de função fixa para o Direct3D 9. O teste alfa é movido para os sombreadores de pixel programáveis para o Direct3D 10 e superior. Para obter informações sobre como emular a funcionalidade de teste do Direct3D 9 Alpha no Direct3D 10 e superior, consulte o exemplo FixedFuncEMU no [SDK do DirectX para junho de 2010](https://www.microsoft.com/download/en/details.aspx?id=6812).
- **Opções do modo Blend**. BOTHSRCALPHA foi removido do BLEND D3D10, pois é \_ redundante com BOTHINVSRCALPHA. Confira [**D3D10 \_ BLEND**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) para obter mais informações.
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
-   **Blender de textura de função fixa (também chamado de sombreador de pixel de função fixa).** Em vez disso, você deve usar sombreadores. Confira [estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   Os **modos de preenchimento** foram alterados. O Direct3D 10 implementa os modos de preenchimento sólido e delineado. O ponto de D3DFILLMODE foi removido, use um sombreador de geometria para emular o modo de ponto, se necessário. O [exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação do ponto de D3DFILLMODE no Direct3D 10. Consulte [**\_ \_ modo de preenchimento d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) e [estágios de sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Formatos**. O hardware pode usar formatos expostos pela API. Os formatos de luminância não são mais implementados.
-   **Filtragem de mipmap**. Removida a opção para selecionar nenhum modo de filtro. Em vez disso, use uma textura com apenas um único mipmap ou defina o estado da amostra MaxLOD como 0. Consulte [objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obter informações adicionais.
-   **Paletas**. Os aplicativos devem usar uma textura dependente de leitura em vez disso.
-   **Modelos de sombreador de pixel e Vertex**: 1 \_ x, 2 \_ x e 3 \_ 0. O Direct3D 10 dá suporte ao modelo de sombreador 4. Consulte o [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) para obter informações adicionais.
-   **Sprites de ponto**. Em vez disso, use um sombreador de geometria. Consulte [Estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Regras de rasterização**. As regras de rasterização de linha GDI herdada são substituídas por regras mais simples e mais limpas. Não há mais suporte para o controle de último pixel para linhas. Consulte [Regras de rasterização (Direct3D 10) para](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) obter informações adicionais.
-   **Modos de sombrear**. D3DSHADEMODE (que suporta sombreamento simples/gouraud/phong) foi removido. O Direct3D 10 implementa dois modificadores de interpolação para saídas de sombreador de vértice. Consulte [Exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) para ver um exemplo de como emular os modos gouraud e sombreado simples do Direct3D 9 no Direct3D 10.
-   **instrução texldp.** Um aplicativo deve implementar uma carga de textura projetada com instruções HLSL extras. Consulte [Referência para HLSL para](../direct3dhlsl/dx-graphics-hlsl-reference.md) obter informações adicionais. [A amostra FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação de texldp no Direct3D 10.
-   **Não há mais suporte** para o estado de estágio de textura TCI (D3DTSS \_ TEXCOORDINDEX).
-   **Ventiladores de triângulo.** Um aplicativo deve converter triângulos-ventiladores existentes em listas de triângulos ou faixas de triângulo. Para emular alguns comportamentos usando DrawPrimitive em APIs mais antigas, tente usar DrawIndexed no Direct3D 10. Consulte [Topologias primitivas (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) para obter informações adicionais.
-   **W buffering**. O suporte a hardware não é garantido; é recomendável que um aplicativo use buffers de profundidade de alta precisão em vez disso. Consulte [Configurando a funcionalidade de Depth-Stencil (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) para obter informações adicionais.
-   **Modos de encapsulamento** (quebra de coordenadas de textura). O encapsulamento de endereços de textura (como quebra automática, espelho, fixe etc.) ainda existe. Consulte [**d3d10 \_ Sample \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) e [**\_ modo de \_ endereço \_ de textura d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
