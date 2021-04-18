---
description: Um efeito do DirectX é uma coleção de estado de pipeline, definida por expressões escritas em HLSL e alguma sintaxe específica para a estrutura de efeito.
ms.assetid: db4c7651-b6a1-4bc3-bcf8-a5cb56c7563e
title: Efeitos (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e08d0c79a6f7f52982a74d5127da70d7b82f84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757723"
---
# <a name="effects-direct3d-10"></a>Efeitos (Direct3D 10)

Um efeito do DirectX é uma coleção de estado de pipeline, definida por expressões escritas em [HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) e alguma sintaxe específica para a estrutura de efeito. Depois de compilar um efeito, use as APIs de estrutura de efeito para renderizar. A funcionalidade de efeito pode variar de algo tão simples quanto um sombreador de vértice que transforma a geometria e um sombreador de pixel que gera uma cor sólida, para uma técnica de renderização que requer várias passagens, usa cada estágio do pipeline de gráficos e manipula o estado do sombreador, bem como o estado do pipeline não associado aos sombreadores programáveis.

A primeira etapa é organizar o estado que você deseja controlar em um efeito. Isso inclui o estado do sombreador (vértice, geometria e sombreadores de pixel), o estado de textura e amostra usado pelos sombreadores e outro Estado de pipeline não programável. Você pode criar um efeito na memória como uma cadeia de caracteres de texto, mas, normalmente, o tamanho é grande o suficiente para que seja útil armazenar o estado de efeito em um arquivo de efeito (um arquivo de texto que termina em uma extensão. FX). Para usar um efeito, você deve compilá-lo (para verificar a sintaxe do HLSL, bem como a sintaxe da estrutura de efeito), inicializar o estado do efeito por meio de chamadas à API e modificar o loop de renderização para chamar as APIs de renderização.

-   [Organizando o estado em um efeito](d3d10-graphics-programming-guide-effects-organize.md)
-   [Interfaces do sistema de efeito](d3d10-graphics-programming-guide-effects-interfaces.md)
-   [Especializando interfaces](d3d10-graphics-reference-effect-specializing.md)
-   [Renderizando um efeito](d3d10-graphics-programming-guide-effects-render.md)

Um efeito encapsula todo o estado de renderização exigido por um efeito específico em uma única função de renderização chamada técnica. Uma passagem é um subconjunto de uma técnica que contém o estado de renderização. Para implementar um efeito de renderização de várias passagens, implemente um ou mais passos dentro de uma técnica. Por exemplo, digamos que você queria renderizar uma geometria com um conjunto de buffers de profundidade/estêncil e, em seguida, desenhar alguns sprites sobre isso. Você pode implementar a renderização de geometria na primeira passagem e o desenho sprite na segunda passagem. Para renderizar o efeito, basta renderizar as duas passagens em seu loop de processamento. Você pode implementar qualquer número de técnicas em um efeito. É claro que quanto maior o número de técnicas, maior o tempo de compilação para o efeito. Uma maneira de explorar essa funcionalidade é criar efeitos com técnicas que são projetadas para serem executadas em hardwares diferentes. Isso permite que um aplicativo faça o downgrade do desempenho com base nos recursos de hardware detectados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
