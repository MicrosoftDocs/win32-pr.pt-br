---
description: A iluminação no mundo real contém um HDR (intervalo dinâmico) muito alto de valores de luminância.
ms.assetid: 537700e2-802d-4fd1-b026-142d6f4f0559
title: Iluminação HDR (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f397ccef2b1fa315e64861453b13f0f6fddfe77
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163678"
---
# <a name="hdr-lighting-direct3d-9"></a>Iluminação HDR (Direct3D 9)

A iluminação no mundo real contém um HDR (intervalo dinâmico) muito alto de valores de luminância. O mundo real tem cerca de 10 pedidos de DR (intervalo dinâmico) para valores de luminância espalhados pelo espectro de escurecimento até o brilho. Por outro lado, uma tela de computador tem uma gama de monitores muito limitada (ou um intervalo de valores de luminância): aproximadamente duas ordens de intervalo dinâmico. O desafio de produzir imagens do HDR renderizadas é mapear os valores HDR do mundo real para a gama limitada de uma tela de computador.

O mapeamento de Tom é a técnica usada pelo DirectX para mapear informações HDR em um intervalo mais limitado. O mapeamento de Tom aplicado à renderização CGI pode melhorar drasticamente a quantidade de detalhes de iluminação renderizados, permitindo que os detalhes nas áreas mais escuras sejam vistos e fornecendo contraste em áreas que são tão brilhantes, eles aparecem gravados. As cenas resultantes são renderizadas com detalhes de iluminação muito mais visíveis.

[HDRLighting exemplo](https://msdn.microsoft.com/library/Ee417769(v=VS.85).aspx) é um exemplo de SDK que demonstra a iluminação HDR.

## <a name="tone-mapping"></a>Mapeamento de Tom

O mapeamento de Tom geralmente simula fenômenos ópticos que não podem ser causados pelo DR do monitor. Os exemplos disso são os flares ou a cair (que são basicamente Propriedades de lentes), a mudança azul que ocorre no olho humano em condições de pouca luz e outras adaptações que são resultado da bioquímica do olho. Se a DR da exibição fosse grande o suficiente, o mapeamento de Tom não seria tão necessário, exceto para fornecer efeitos artísticos ou algumas das propriedades de uma lente da câmera ou um dispositivo acoplado de encargo (CCD).

O mapeamento de Tom divide o intervalo de valores de luminância em uma cena em um conjunto de zonas. Cada zona abrange um intervalo de valores de luminância.

O HDR usa os seguintes termos:

-   Intervalo de zona de valores de luminância
-   Cinza intermediária-região de brilho central da cena
-   Taxa de intervalo dinâmica da luminância de cena mais alta para a luminância de cena mais baixa
-   Medição subjetiva de chave da iluminação de cena: isso varia de claro para moderado a escuro

Para calcular a luminância a partir de valores RGB, use:


```
L = 0.27R + 0.67G + 0.06B;
```



A luminância de média de log é uma aproximação útil para a chave de uma cena. Uma equação geral tem esta aparência:

L<sub>w</sub> = exp \[ 1/N ( \[ log Sum (Delta + L<sub>w</sub>(x, y) \] ) \]

Em que:

-   L<sub>w</sub> -log-luminância de média
-   N-número de pixels na imagem
-   Delta-um pequeno fator para evitar problemas com pixels pretos
-   L<sub>w</sub>(x, y)-a luminância de espaço mundial para pixel (x, y)

Para mapear isso para um valor de cinza médio, aqui está um operador de dimensionamento de luminescência:

L (x, y) = a \* L<sub>w</sub>(x, y)/L<sub>w</sub>

Em que:

-   L (x, y)-luminância em escala para pixel (x, y)
-   um valor de chave de imagem depois de aplicar o dimensionamento

E, finalmente, aqui está um operador de mapeamento de Tom simples para compactar as altas luminosidades:

L<sub>d</sub>(x, y) = l (x, y)/(1 + L (x, y))

Em que:

-   L<sub>d</sub>(x, y)-luminância compactada e dimensionada para pixel (x, y)
-   um valor de chave de imagem depois de aplicar o dimensionamento

Esse operador dimensiona altas luminâncias de 1/L e baixa luminância em 1. Para obter mais detalhes, consulte o documento a seguir.

Reinhard, Erik, Mike Stark, Peter Shirley e James Ferwerda. ["Reprodução de tons fotográficos para imagens digitais"](https://www.cs.utah.edu/~reinhard/cdrom/tonemap.pdf). Transações de ACM sobre gráficos (TOG), procedimentos de conferência anual de 29 em inglês (SIGGRAPH), pp. 267-276. Nova York, NY: ACM Press, 2002.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos avançados](advanced-topics.md)
</dt> </dl>

 

 



