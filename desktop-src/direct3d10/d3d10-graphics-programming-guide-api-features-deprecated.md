---
description: Uma lista dos recursos disponíveis no Direct3D 10 está aqui. Esta página lista os recursos do Direct3D 9 que não têm mais suporte no Direct3D 10.
ms.assetid: ad3eff8e-a225-47c0-a53f-b1a3c94bcaac
title: Recursos preteridos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66b6fe5092427cd66876ab5f6e1d7aaf83f0880
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089171"
---
# <a name="deprecated-features-direct3d-10"></a>Recursos preteridos (Direct3D 10)

Uma lista dos recursos disponíveis no Direct3D 10 está [aqui](d3d10-graphics-programming-guide-api-features.md). Esta página lista os recursos do Direct3D 9 que não têm mais suporte no Direct3D 10.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| As maiores alterações de recursos no Direct3D 10 são:<br/> O Direct3D 10 não dá mais suporte ao pipeline de transformação e iluminação de função fixa.<br/> O Direct3D 10 não dá mais suporte ao misturador de textura de função fixa (às vezes chamado de sombreador de pixel de função fixa).<br/> O Direct3D 10 implementa novas regras de rasterização, que são mais simples e limpas do que as regras GDI herdadas que são implementadas no Direct3D 9. Por exemplo, não há mais suporte para o controle de último pixel para linhas.<br/> |



 

Aqui está uma lista completa dos recursos do Direct3D 9 que foram preteridos no Direct3D 10.

-   **Combinação alfa**. A mistura alfa agora é programada independentemente da mistura de cores. O Direct3D 10 adiciona uma alternância alfa-Blend-Enable, que é habilitada por padrão. Consulte [objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obter mais informações.
-   **Teste alfa**. O teste alfa é um comportamento de pixel de função fixa para o Direct3D 9. O teste alfa é movido para os sombreadores de pixel programáveis para o Direct3D 10 e superior. Para obter informações sobre como emular a funcionalidade de teste do Direct3D 9 Alpha no Direct3D 10 e superior, consulte o exemplo FixedFuncEMU no [SDK do DirectX para junho de 2010](https://www.microsoft.com/download/en/details.aspx?id=6812).
-   **Opções do modo de mesclagem**. BOTHSRCALPHA foi removido do D3D10 \_ Blend, pois ele é redundante com BOTHINVSRCALPHA. Consulte [**d3d10 \_ Blend**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_blend) para obter mais informações.
-   **Bloquear formatos de compactação**. Não há nenhuma distinção entre alfa multiplicado previamente ou não premultiplicado em Direct3D 10. Esses formatos do Direct3D 9 são mapeados para esses formatos do Direct3D 10: 

    | Direct3D 9 | Direct3D 10 |
    |------------|-------------|
    | DXT1       | BC1\*       |
    | DXT2,DXT3  | BC2\*       |
    | DXT4,DXT5  | BC3\*       |

    

     

    Consulte [Bloquear compactação (Direct3D 10)](d3d10-graphics-programming-guide-resources-block-compression.md) para obter informações adicionais.

-   **Planos de corte**. Em vez de usar os recortes de clipes, o Direct3D 10 implementa distâncias de clip e de seleção, com até 8 componentes, cada um em até 2 elementos de atributos de vértice. Consulte [semântica (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-semantics.md) para obter informações adicionais. O [exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação de planos de corte no Direct3D 10.
-   **Pontilhamento**. O Direct3D 10 não dá suporte à gravação de dados diquerdos em um destino de renderização.
-   O **pipeline de transformação e iluminação de função fixa não está disponível**. Em vez disso, você deve usar sombreadores. Confira [estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Blender de textura de função fixa (também chamado de sombreador de pixel de função fixa)**. Em vez disso, você deve usar sombreadores. Confira [estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   Os **modos de preenchimento** foram alterados. O Direct3D 10 implementa os modos de preenchimento sólido e delineado. O ponto de D3DFILLMODE foi removido, use um sombreador de geometria para emular o modo de ponto, se necessário. O [exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação do ponto de D3DFILLMODE no Direct3D 10. Consulte [**\_ \_ modo de preenchimento d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) e [estágios de sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Formatos**. O hardware pode usar formatos expostos pela API. Os formatos de luminância não são mais implementados.
-   **Filtragem de mipmap**. Removida a opção para selecionar nenhum modo de filtro. Em vez disso, use uma textura com apenas um único mipmap ou defina o estado da amostra MaxLOD como 0. Consulte [objetos de estado (Direct3D 10)](d3d10-graphics-programming-guide-api-features-state-objects.md) para obter informações adicionais.
-   **Paletas**. Os aplicativos devem usar uma textura dependente de leitura em vez disso.
-   **Modelos de sombreador de pixel e Vertex**: 1 \_ x, 2 \_ x e 3 \_ 0. O Direct3D 10 dá suporte ao modelo de sombreador 4. Consulte o [modelo de sombreador 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md) para obter informações adicionais.
-   **Sprites de ponto**. Em vez disso, use um sombreador Geometry. Confira [estágios do sombreador (Direct3D 10)](/previous-versions//bb205146(v=vs.85)) para obter informações adicionais.
-   **Regras de rasterização**. As regras de rasterização de linha GDI herdadas são substituídas por regras mais claras e mais simples. Não há mais suporte para o controle de último pixel para linhas. Consulte [regras de rasterização (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-rules.md) para obter informações adicionais.
-   **Modos de sombreamento**. D3DSHADEMODE (que dá suporte a sombreamento Flat/Gouraud/Phong) foi removido. O Direct3D 10 implementa dois modificadores de interpolações para saídas de sombreador de vértice. Consulte o [exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) para obter um exemplo de emulação do Direct3D 9 Gouraud e modos de sombreamento simples no Direct3D 10.
-   instrução **texldp** . Um aplicativo deve implementar uma carga de textura projetada com instruções HLSL extras. Consulte [a referência para HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) para obter informações adicionais. O [exemplo de FixedFuncEMU](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx) fornece um exemplo de emulação de Texldp no Direct3D 10.
-   Não há mais suporte para o estado de TCI (D3DTSS TEXCOORDINDEX) de textura de **textura (índice de coordenadas de** diferida) \_ .
-   **Fãs de triângulo**. Um aplicativo deve converter os ventiladores de triângulo existentes em listas de triângulos ou em faixas de triângulo. Para emular alguns comportamentos usando o DrawPrimitive em APIs mais antigas, tente usar o DrawIndexed no Direct3D 10. Consulte [topologias primitivas (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) para obter informações adicionais.
-   **Buffer de W**. O suporte a hardware não é garantido; é recomendável que um aplicativo use buffers de profundidade de alta precisão em vez disso. Consulte [Configurando a funcionalidade de Depth-Stencil (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md) para obter informações adicionais.
-   **Modos de encapsulamento** (quebra de coordenadas de textura). O encapsulamento de endereços de textura (como quebra automática, espelho, fixe etc.) ainda existe. Consulte [**d3d10 \_ Sample \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) e [**\_ modo de \_ endereço \_ de textura d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_texture_address_mode).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
