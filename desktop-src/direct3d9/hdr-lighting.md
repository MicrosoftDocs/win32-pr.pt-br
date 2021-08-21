---
description: A iluminação no mundo real contém um HDR (intervalo dinâmico) muito alto de valores de luminância.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Iluminação HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863e8eefab6e0199904876bdb398fefa1aeb988ef2f3556b21c24d92dbc998e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094642"
---
# <a name="hdr-lighting-direct3d-9"></a>Iluminação HDR (Direct3D 9)

A iluminação no mundo real contém um HDR (intervalo dinâmico) muito alto de valores de luminância. O mundo real tem cerca de 10 ordens de DR (intervalo dinâmico) para valores de luminância espalhados pelo espectro de brilho até o brilho. Por outro lado, uma tela do computador tem uma gama de exibição muito limitada (ou intervalo de valores de luminância): aproximadamente duas ordens de intervalo dinâmico. O desafio de produzir imagens renderizadas do HDR é mapear os valores do HDR do mundo real para a gama limitada de uma tela de computador.

Mapeamento de tom é a técnica usada pelo DirectX para mapear informações do HDR para um intervalo mais limitado. O mapeamento de tom aplicado à renderização de CGI pode melhorar drasticamente a quantidade de detalhes de iluminação renderizados, permitindo que os detalhes nas áreas mais escuras sejam vistos e fornecendo contraste em áreas tão brilhante que elas parecem desemocadas. As cenas resultantes são renderizações com detalhes de iluminação muito mais visíveis.

[Exemplo de HDRLighting é](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) um exemplo de SDK que demonstra a iluminação do HDR.

## <a name="tone-mapping"></a>Mapeamento de tom

O mapeamento de tom geralmente simula fenômenos ópticos que não podem ser causados pela DR do monitor. Exemplos disso são os óculos ou a flor (que são principalmente propriedades de lentes), a mudança azul que acontece no olho humano em condições de pouca luz e outras adaptações que são resultado da biometria do olho. Se a DR da exibição fosse grande o suficiente, o mapeamento de tom não seria tão necessário, exceto para fornecer efeitos colaterais ou algumas das propriedades de uma lente da câmera ou um CCD (dispositivo alohado de custo).

O mapeamento de tom divide o intervalo de valores de luminância em uma cena em um conjunto de zonas. Cada zona abrange um intervalo de valores de luminância.

O HDR usa os seguintes termos:

-   Zona – intervalo de valores de luminância
-   Cinza médio – região de brilho central da cena
-   Intervalo dinâmico – taxa da luminância de cena mais alta para a luminância de cena mais baixa
-   Chave – medida subjetivo da iluminação da cena: isso varia de claro a moderado a escuro

Para calcular a luminância de valores RGB, use este:


```
L = 0.27R + 0.67G + 0.06B;
```



A luminância média de log é uma aproximação útil para a chave de uma cena. Uma equação geral tem esta aparência:

L<sub>w</sub> = exp \[ 1 / N( sum \[ log( delta + L<sub>w</sub>( x, y ) \] ) ) \]

Em que:

-   L<sub>w</sub> - luminância média de log
-   N – número de pixels na imagem
-   delta – um pequeno fator para evitar problemas com pixels pretos
-   L<sub>w</sub>( x, y ) – a luminância de espaço mundial para pixel ( x, y )

Para mapear isso para um valor cinza-médio, aqui está um operador de dimensionamento de luminância:

L( x, y ) = a \* L<sub>w</sub>( x, y ) / L<sub>w</sub>

Em que:

-   L( x, y ) – luminância dimensionada para pixel ( x, y )
-   a - valor da chave de imagem depois de aplicar o dimensionamento

E, por fim, aqui está um operador de mapeamento de tom simples para compactar as altas luminâncias:

L<sub>d</sub>( x, y ) = L( x, y ) / ( 1 + L( x, y ) )

Em que:

-   L<sub>d</sub>( x, y ) - luminância compactada e dimensionada para pixel ( x, y )
-   a - valor da chave de imagem depois de aplicar o dimensionamento

Esse operador dimensiona luminâncias altas em 1/L e luminâncias baixas em 1. Para obter mais detalhes, consulte o documento a seguir.

Reinhard, Eric, Mike Ltda, Peter Ltda e James Vaiwerda. ["Reprodução de tom de voz para imagens digitais".](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf) ACM Transactions on Graphics (TOG), Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques (SIGGRAPH), pp. 267-276. Nova York, NOVA YORK: ACM Press, 2002.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 



