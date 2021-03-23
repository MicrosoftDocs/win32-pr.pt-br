---
title: O que é o Direct3D 12
description: O DirectX 12 apresenta a próxima versão do Direct3D; a API de gráficos 3D no centro do DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: b3ff1896372719b011b283e3ff1f5426db9e13d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104102"
---
# <a name="what-is-direct3d-12"></a>O que é Direct3D 12?

O DirectX 12 apresenta a próxima versão do Direct3D &mdash; a API de gráficos 3D no coração do DirectX. O Direct3D 12 é mais rápido e mais eficiente do que qualquer versão anterior. O Direct3D 12 permite cenas mais avançadas, mais objetos, efeitos mais complexos e a utilização total do hardware de GPU moderno.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>Como o Direct3D 12 pode ser muito mais rápido e eficiente?

O Direct3D 12 é exclusivo, pois fornece um nível mais baixo de abstração de hardware do que as versões anteriores, o que permite melhorar significativamente o dimensionamento de CPU de vários núcleos de seu título (ou outro aplicativo). Para uma coisa, com o Direct3D 12, seu título é responsável por seu próprio [Gerenciamento de memória](memory-management.md). Além disso, usando o Direct3D 12, seus títulos e aplicativos se beneficiam da sobrecarga de GPU reduzida por meio de recursos como [filas de comando e listas](command-queues-and-command-lists.md), [tabelas de descritores](descriptor-tables.md)e [objetos de estado de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md)conciso.

O Direct3D 12 e o Direct3D 11,3 apresentam um conjunto de novos recursos para o pipeline de renderização.

- [Rasterização conservadora](../direct3d11/conservative-rasterization.md) para habilitar a detecção de colisão confiável.
- [Recursos do lado do volume](../direct3d11/volume-tiled-resources.md) para habilitar recursos tridimensionais em fluxo para serem tratados como se estivessem todos na memória de vídeo.
- [Exibições ordenadas pelo rasterizador](../direct3d11/volume-tiled-resources.md) para habilitar a renderização de transparência confiável.
- Definir a referência de estêncil dentro de um sombreador para habilitar a sombra especial e outros efeitos.
- Mapeamento de textura aprimorado e carregamentos de UAV (exibição de acesso não ordenado) digitados.

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>Quão profundamente devo investir no Direct3D 12?

O Direct3D 12 fornece quatro principais benefícios para desenvolvedores de gráficos (em comparação com o Direct3D 11).

- Sobrecarga de CPU reduzida amplamente.
- Consumo de energia reduzido significativamente.
- Até (aproximadamente) 20% de melhoria na eficiência da GPU.
- Desenvolvimento de plataforma cruzada para um dispositivo Windows 10 (PC, Tablet, console, móvel).

O Direct3D 12 foi projetado para os programadores de gráficos avançados usarem. Ele chama uma experiência de gráficos significativa e um alto nível de ajuste fino. O Direct3D 12 foi projetado para fazer uso completo de multithreading, uma sincronização cuidadosa de CPU/GPU e a transição e reutilização de recursos de uma finalidade para outra. Essas são técnicas que exigem uma quantidade considerável de habilidades de programação de nível de memória.

Outra vantagem que o Direct3D 12 tem é sua pequena superfície de API. Há cerca de 200 funções; e cerca de um terço deles faz todo o trabalho pesado. Isso significa que você, como desenvolvedor de gráficos, deve ser capaz de instruir o consideram sobre &mdash; e dominar &mdash; o conjunto de API completo sem ter que memorizar muitos nomes de API.

O Direct3D 11 continua sendo uma opção viável juntamente com o Direct3D 12. Muitos dos novos recursos de renderização do Direct3D 12 estão disponíveis no [direct3d 11,3](../direct3d11/direct3d-11-3-features.md). O Direct3D 11,3 é uma API de mecanismo gráfico de baixo nível; e o Direct3D 12 é ainda mais profundo.

Há pelo menos duas maneiras de que sua equipe de desenvolvimento possa abordar um título do Direct3D 12.

### <a name="use-direct3d-12-exclusively"></a>Usar o Direct3D 12 exclusivamente

Para um projeto que tira vantagem máxima de todos os benefícios do Direct3D 12, você deve desenvolver um mecanismo Direct3D 12 altamente personalizado desde o início.

Se você, como desenvolvedor de gráficos, entender o uso e reutilização de recursos dentro de seus títulos, e pode aproveitar isso ao minimizar o carregamento e a cópia, você pode desenvolver e personalizar um mecanismo altamente eficiente para esses títulos. As melhorias de desempenho podem ser muito consideráveis, liberando tempo de CPU para aumentar o número de chamadas de desenho e, portanto, adicionando mais cluster aos seus elementos gráficos.

O investimento em programação é significativo e você deve considerar a depuração e a instrumentação do projeto desde o início. Threads, sincronização e outros bugs de tempo podem ser desafiadores.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Usar o Direct3D 12 em conjunto com o Direct3D 11

Uma abordagem de curto prazo seria resolver afunilamentos conhecidos no seu título do Direct3D 11. Você pode solucioná-los usando a [interoperabilidade do Direct3D 12 e/ou](direct3d-12-interop.md) as técnicas D3D11On12, que permitem que as duas versões da API funcionem juntas. Essa abordagem minimiza as alterações necessárias para um mecanismo de gráficos do Direct3D 11 existente. No entanto, os ganhos de desempenho serão limitados ao alívio do afunilamento que o código do Direct3D 12 aborda.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Vídeos sobre o Microsoft DirectX 12 (e o treinamento de gráficos)

[Treinamento aprimorado para desenvolvedores de gráficos](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). Esses vídeos abrangem tópicos como modos de apresentação, portando para DirectX 12, rasterização conservadora, ferramentas gráficas, ângulo, Win2D e eventos como GDC, Build e muito mais. O conteúdo técnico do DirectX 12 é precedido pelo *DirectX 12*. Venha aqui para aprender dicas e truques diretamente da equipe de recursos do Direct3D 12. Queremos ajudá-lo a usar nossas versões e ferramentas mais recentes para tornar seu jogo o melhor possível!

## <a name="conclusion"></a>Conclusão

O Direct3D 12 é um desempenho considerável do mecanismo de gráficos. A facilidade de desenvolvimento, as construções de alto nível e o suporte do compilador foram dimensionados de volta para permitir isso. O suporte a drivers e a facilidade de depuração permanecem em um par com o Direct3D 11.

O Direct3D 12 é uma nova região. Território que está aguardando o especialista de Inquisitive vir e explorar.
