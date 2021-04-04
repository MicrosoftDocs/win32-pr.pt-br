---
title: Teste de colisão de toque
description: Os tópicos desta seção fornecem uma visão geral do suporte para teste de colisão de toque no Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- interação do usuário
- input
- ponteiro
- touch
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: 9e389b8e39616dcef8f7ff4bc53d945179401478
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/07/2020
ms.locfileid: "103823545"
---
# <a name="touch-hit-testing"></a>Teste de colisão de toque

## <a name="purpose"></a>Finalidade

Os tópicos desta seção fornecem uma visão geral do suporte para teste de colisão de toque no Windows. O teste de colisão de toque permite identificar um destino de entrada com base em se a área de conteúdo de um elemento de interface do usuário está dentro da área de contato ou inclui o ponto de contato.

O teste de colisão de toque usa geometria de contato complexa para toda a área de toque em vez de uma única coordenada x-y interpolada. O uso de toda a geometria de contato melhora muito a precisão e a precisão quando você está identificando o destino mais provável de entrada por toque.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
| --- | --- |
| [Referência de teste de colisão de toque](touchhittest-reference.md)<br/> | Os tópicos nesta seção fornecem as especificações de referência para [teste de colisão de toque](touch-hit-testing-portal.md).<br/> |

## <a name="developer-audience"></a>Público de desenvolvedores

As APIs de teste de colisão de toque são projetadas para os desenvolvedores que estão criando estruturas de interface do usuário que fornecem uma experiência de usuários consistente e otimizada para toque em aplicativos de área de trabalho.

## <a name="related-topics"></a>Tópicos relacionados

[Interação do usuário](../user-interaction.md)
