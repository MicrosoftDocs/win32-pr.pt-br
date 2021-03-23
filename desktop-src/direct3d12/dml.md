---
title: DirectML (Direct Machine Learning)
description: O Direct Machine Learning (DirectML) é uma API de nível baixo para o aprendizado de máquina. Ele tem uma interface de programação familiar (C++ nativo, nano COM) e fluxo de trabalho no estilo do DirectX 12.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103530"
---
# <a name="direct-machine-learning-directml"></a>DirectML (Direct Machine Learning)

O Direct Machine Learning (DirectML) é uma API de nível baixo para o aprendizado de máquina. Ele tem uma interface de programação familiar (C++ nativo, nano COM) e fluxo de trabalho no estilo do DirectX 12. Você pode integrar cargas de trabalho com inferência a aprendizado de máquina em seu jogo, mecanismo, middleware, back-end ou outro aplicativo. O DirectML é compatível com todo o hardware compatível com DirectX 12.

O DirectML é introduzido no Windows 10, versão 1903 e na versão correspondente do SDK do Windows.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Introdução ao DirectML](dml-intro.md) | O Direct Machine Learning (DirectML) é uma API de nível baixo para o Machine Learning (ML). |
| [Associação no DirectML](dml-binding.md) | No DirectML, a *Associação* refere-se ao anexo de recursos para o pipeline a ser usado pela GPU durante a inicialização e execução de seus operadores de aprendizado de máquina. Esses recursos podem ser tempos de entrada e de saída, por exemplo, bem como quaisquer recursos temporários ou persistentes que o operador precisa. |
| [Barreiras de UAV e barreiras de estado de recursos no DirectML](dml-barriers.md) | Descreve os benefícios de correção das barreiras e como você pode trabalhar com elas no DirectML. |
| [Usando progressos para expressar o layout de enchimento e de memória](dml-strides.md) | Os dezenases de DirectML são descritos pelas propriedades conhecidas como os *tamanhos* e os *avanços* do tensor. |
| [Tempo de vida e sincronização de recursos](dml-resource-lifetime.md) | Para evitar um comportamento indefinido, seu aplicativo DirectML deve gerenciar corretamente os tempos de vida de objeto e a sincronização entre a CPU e a GPU. |
| [Usando a camada de depuração DirectML](dml-debug-layer.md) | A camada de depuração DirectML é um componente opcional de tempo de desenvolvimento que ajuda você a depurar seu código DirectML. |
| [Lidar com erros e remoção de dispositivo](dml-errors.md) | Este tópico discute como depurar DirectML dispositivos-remoção e outras condições de erro. |
| [Funções auxiliares DirectML](dml-helper-functions.md) | Listagens de código das funções auxiliares DirectML essenciais. |
| [Aplicativos de exemplo do DirectML](dml-min-app.md) | Links para aplicativos de exemplo DirectML, incluindo um exemplo de um aplicativo de DirectML mínimo. |

## <a name="related-topics"></a>Tópicos relacionados

* [Guia de programação do Direct3D 12](directx-12-programming-guide.md)
