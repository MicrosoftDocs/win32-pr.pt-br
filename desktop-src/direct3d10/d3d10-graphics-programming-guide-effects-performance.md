---
description: Considerações sobre desempenho (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Considerações sobre desempenho (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010139"
---
# <a name="performance-considerations-direct3d-10"></a>Considerações sobre desempenho (Direct3D 10)

## <a name="using-effect-pools"></a>Usando pools de efeito

É comum que os pipelines de renderização usem muitos sombreadores para renderizar diferentes tipos de objeto e efeitos especiais. O sombreador é uma mistura de Estados que um comum entre todos os sombreadores, como uma matriz mundial ou uma posição clara, e outro estado específico para cada sombreador, como a cor difusa de um objeto ou o cálculo de realce especulativo. Um pool de efeitos é um local na memória para armazenar o estado que é usado em vários sombreadores, bem como objetos de dispositivo comuns, como sombreadores, objetos de estado de renderização e buffers de constantes. A melhoria de desempenho resulta da atualização do Estado comum uma vez para todos os sombreadores que precisam desse Estado.

Um pool de efeitos é um local de memória compartilhada para o estado de efeito. Um pool é criado de forma semelhante a um efeito; Ele pode ser criado a partir da memória (ou um arquivo ou um recurso). Isso leva a dois tipos diferentes de efeitos: um efeito global que não depende do estado em outro efeito em vez de um efeito filho que depende do estado em outro efeito.

Você especifica se um efeito é um efeito global (o caso padrão) ou um efeito filho (fornecendo o sinalizador de [ \_ \_ \_ \_ efeito filho de compilação de efeito d3d10](d3d10-effect.md) ) quando o efeito é criado. Um efeito global pode servir como um pool de efeito; um efeito filho não pode ser um pool de efeitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um efeito](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[Efeitos (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



