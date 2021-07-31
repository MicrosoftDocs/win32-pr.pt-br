---
title: O que é o Direct3D 12
description: O DirectX 12 apresenta a próxima versão do Direct3D; a API de gráficos 3D no núcleo do DirectX.
ms.assetid: 09C586BF-11CE-4392-9BFD-A40B05DD0624
ms.localizationpriority: high
ms.topic: article
ms.date: 11/19/2018
ms.openlocfilehash: f82b01ba33cfa6660f266a481b2eaaab20ade236
ms.sourcegitcommit: 60ff57d8cf94ae7a47c6046ad49f7c7256a7edb6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/31/2021
ms.locfileid: "115006791"
---
# <a name="what-is-direct3d-12"></a>O que é Direct3D 12?

O DirectX 12 apresenta a próxima versão do Direct3D a API de &mdash; gráficos 3D no núcleo do DirectX. O Direct3D 12 é mais rápido e eficiente do que qualquer versão anterior. O Direct3D 12 permite cenas mais sofisticadas, mais objetos, efeitos mais complexos e utilização completa do hardware de GPU moderno.

## <a name="how-can-direct3d-12-be-so-much-faster-and-more-efficient"></a>Como o Direct3D 12 pode ser muito mais rápido e mais eficiente?

O Direct3D 12 é exclusivo porque fornece um nível mais baixo de abstração de hardware do que as versões anteriores, o que permite melhorar significativamente o dimensionamento de CPU de vários núcleos do seu título (ou outro aplicativo). Por um lado, com o Direct3D 12, seu título é responsável por seu próprio gerenciamento [de memória.](memory-management.md) Além disso, usando o Direct3D 12, seus títulos e aplicativos se beneficiam da sobrecarga reduzida da GPU por meio de recursos como filas de comandos e listas, [tabelas](command-queues-and-command-lists.md) [de](descriptor-tables.md)descritor e objetos de estado de [pipeline](managing-graphics-pipeline-state-in-direct3d-12.md)concisos.

O Direct3D 12 e o Direct3D 11.3 apresentam um conjunto de novos recursos para o pipeline de renderização.

- [Rasterização conservadora para habilitar](../direct3d11/conservative-rasterization.md) a detecção de acertos confiável.
- [Os recursos lado a lado](../direct3d11/volume-tiled-resources.md) do volume para permitir que os recursos tridimensionais transmitidos sejam tratados como se todos eles fossem na memória de vídeo.
- [Exibições ordenadas pelo Rasterizer para](../direct3d11/rasterizer-order-views.md) habilitar a renderização de transparência confiável.
- Definir a referência de estêncil em um sombreador para habilitar sombreamento especial e outros efeitos.
- Mapeamento de textura aprimorado e cargas UAV (exibição de acesso não organizado) digitadas.

## <a name="how-deeply-should-i-invest-in-direct3d-12"></a>Quanto devo investir no Direct3D 12?

O Direct3D 12 fornece quatro benefícios principais para desenvolvedores de gráficos (em comparação com o Direct3D 11).

- Redução significativa da sobrecarga da CPU.
- Consumo de energia significativamente reduzido.
- Melhoria de até (aproximadamente) 20% na eficiência da GPU.
- Desenvolvimento de plataforma cruzada para um Windows 10 dispositivo (PC, tablet, console, móvel).

O Direct3D 12 foi projetado para que programadores gráficos avançados usem. Ele exige uma experiência gráfica significativa e um alto nível de ajuste. O Direct3D 12 foi projetado para fazer uso completo de multi-threading, sincronização cuidadosa de CPU/GPU e a transição e reuso de recursos de uma finalidade para outra. Essas são técnicas que exigem uma quantidade considerável de habilidade de programação no nível de memória.

Outra vantagem que o Direct3D 12 tem é seu pequeno espaço de API. Há cerca de 200 funções; e cerca de um terceiro deles faz todo o trabalho pesado. Isso significa que você, como desenvolvedor de gráficos, deve ser capaz de instruir e dominar o conjunto de API completo sem precisar &mdash; &mdash; memorizar muitos nomes de API.

O Direct3D 11 continua sendo uma opção viável junto com o Direct3D 12. Muitos dos novos recursos de renderização do Direct3D 12 estão disponíveis [no Direct3D 11.3](../direct3d11/direct3d-11-3-features.md). O Direct3D 11.3 é uma API de mecanismo gráfico de baixo nível; e Direct3D 12 se aprofundam ainda mais.

Há pelo menos duas maneiras pelas quais sua equipe de desenvolvimento pode abordar um título do Direct3D 12.

### <a name="use-direct3d-12-exclusively"></a>Usar o Direct3D 12 exclusivamente

Para um projeto que aproveite ao máximo todos os benefícios do Direct3D 12, você deve desenvolver um mecanismo direct3D 12 altamente personalizado desde o zero.

Se você, como desenvolvedor de gráficos, entender o uso e o re uso de recursos em seus títulos e puder aproveitar isso minimizando o carregamento e a cópia, poderá desenvolver e personalizar um mecanismo altamente eficiente para esses títulos. As melhorias de desempenho podem ser muito consideráveis, liberando o tempo de CPU para aumentar o número de chamadas de desenho e, portanto, adicionando mais brilho aos seus gráficos.

O investimento em programação é significativo e você deve considerar a depuração e a instrumentação do projeto desde o início. Threading, sincronização e outros bugs de tempo podem ser desafiadores.

### <a name="use-direct3d-12-in-concert-with-direct3d-11"></a>Usar o Direct3D 12 em conjunto com o Direct3D 11

Uma abordagem de curto prazo seria resolver gargalos conhecidos em seu título do Direct3D 11. Você pode resolver isso usando técnicas [de interop e/ou D3D11On12 do Direct3D 12,](direct3d-12-interop.md) que permitem que as duas versões da API funcionem juntas. Essa abordagem minimiza as alterações necessárias para um mecanismo gráfico do Direct3D 11 existente. No entanto, os ganhos de desempenho serão limitados ao relevo do gargalo que o código Direct3D 12 aborda.

## <a name="microsoft-directx-12-and-graphics-education-videos"></a>Vídeos do Microsoft DirectX 12 (e educação de gráficos)

[Educação aprimorada para desenvolvedores de gráficos](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA). Esses vídeos abrangem tópicos como modos de apresentação, portação para DirectX 12, rasterização conservadora, ferramentas gráficas, Angle, Win2D e eventos como GDC, Build e muito mais. O conteúdo do Technical DirectX 12 é prefaced com *o DirectX 12.* Venha aqui para aprender dicas e truques diretamente da equipe de recursos do Direct3D 12. Queremos ajudá-lo a usar nossas versões e ferramentas mais recentes para tornar seu jogo o melhor possível!

## <a name="conclusion"></a>Conclusão

O Direct3D 12 tem tudo a ver com o desempenho do mecanismo de gráficos drástica. A facilidade de desenvolvimento, constructos de alto nível e suporte ao compilador foram dimensionados novamente para habilitar isso. O suporte ao driver e a facilidade de depuração permanecem em um par com o Direct3D 11.

O Direct3D 12 é um novo território. Território que está aguardando o especialista inquisitivo vir e explorar.
