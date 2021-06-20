---
description: Saiba mais sobre o suporte de desenho de linha no D3DX. D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.
ms.assetid: 34ad82f2-542c-4342-af02-a767d6d4c96c
title: Suporte de desenho de linha no D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cf15eae461d0dbe719e99cfac605a6c8b8d272
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407529"
---
# <a name="line-drawing-support-in-d3dx-direct3d-9"></a>Suporte de desenho de linha no D3DX (Direct3D 9)

D3DX é uma biblioteca de utilitários que fornece serviços auxiliares. É uma camada acima do componente do Direct3D.

O D3DX dá suporte a linhas com alias único de grande pixel. Não há mais suporte para padrões de linha.

A biblioteca de desenho de linha emula as linhas usando triângulos de textura e pressupõe o seguinte:

-   O hardware está disponível por meio das interfaces do Direct3D 9.
-   Pelo menos um estágio de textura está disponível.
-   as texturas 64 x 64 são usadas.
-   Os seguintes modos estão disponíveis:
    -   Filtragem bilinear
    -   Modo de endereço fixe
    -   Modo de endereço de quebra
    -   Modular de op Alpha
    -   Mistura alfa (SRCBLEND = SRC \_ Alpha, DESTBLEND = inv \_ src \_ Alpha)
    -   Teste alfa se a mistura alfa não estiver disponível; resultado de qualidade inferior

Para a renderização de linha AntiAlias em destinos de renderização multiamostrais, use [**ID3DXLine**](id3dxline.md) que gera polígonos texturizados. Os valores de cobertura de pixel, gerados pela rasterização de linha AntiAlias, modulam o valor alfa do pixel calculado pelo sombreador de pixel. Para desenhar uma linha AntiAlias, um aplicativo deve habilitar a mesclagem alfa e, em seguida, deve definir o \_ estado de RENDERIZAÇÃO D3DRS ANTIALIASEDLINEENABLE como **true**.

## <a name="functionality-description"></a>Descrição da funcionalidade

A biblioteca dá suporte a desenho de faixas de linha coloridas com os seguintes recursos de linha, cada um dos quais é independente de qualquer outra:

-   Largura da linha
-   Padrão de linha com repetição (o contador de padrão de linha é redefinido com cada [**ID3DXLine::D RAW**](id3dxline--draw.md) ou [**ID3DXLine::D chamada rawtransform**](id3dxline--drawtransform.md) . Ele não é redefinido com cada segmento da faixa de linhas.)
-   Suavização
-   Linhas de estilo OpenGL

> [!Note]  
> Não há suporte para a mitra.

 

A biblioteca usa o suporte a desenho de linha de hardware nativo (se disponível no dispositivo) somente se:

-   A largura da linha é 1.
-   Nenhum padrão de linha está habilitado.

Há suporte para linhas com alias de todo um pixel em um hardware, portanto, a biblioteca usa isso, se disponível. O membro LineCaps da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) enumera os recursos de hardware para primitivos de desenho de linha.

Quando o desenho de linha de software é usado, cada linha é expandida em um retângulo e quatro vértices são enviados para o driver.

Cada segmento de linha é desenhado com dois triângulos. A largura da primitiva é a largura especificada mais 1,0, o que pode resultar em uma linha ou coluna de pixels extra. À medida que a linha fica mais larga, o gradiente AntiAlias na textura se torna mais grande e os texels mais opacos são replicados ao meio do meio. O gradiente é codificado na direção v da textura e normalmente replicado ao longo da direção de u. O modo de endereçamento de textura para v é fixe.

Cada segmento de linha na lista pode ser considerado como uma linha separada que ocorre para iniciar do ponto de extremidade anterior.

A qualidade de anti-aliasing ao longo das bordas paralelas ao comprimento da linha original sofre à medida que a linha fica mais larga. Espera-se que as larguras de linha maiores que 32,0 comecem a exibir artefatos ao longo dessas bordas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



