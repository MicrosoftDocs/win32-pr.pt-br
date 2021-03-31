---
title: Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários
description: Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários
ms.assetid: 28ba863b-9c3e-4b0e-875d-6b696600888c
keywords:
- fluxos, taxas de bits
- codecs, calculando taxas de bits para fluxos arbitrários
- taxas de bits, calculando para fluxos arbitrários
- fluxos, calculando taxas de bits para fluxos arbitrários
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d704352d414b1fe5079fb068593c2d0d8b2f8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004944"
---
# <a name="calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams"></a>Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários

Calcular a taxa de bits e a janela de buffer adequadas para um tipo de fluxo arbitrário não é uma ciência exata. Uma abordagem simples é definir a taxa de bits para corresponder ao tamanho do fluxo dividido por seu comprimento, em segundos. Por exemplo, um fluxo contendo um total de 68000 bits com duração de 20 segundos pode ter uma taxa de bits de 3400 bits por segundo (68000 bits/20 segundos = 3400 bits por segundo).

O problema com essa técnica simples de atribuição de taxa de bits é que ela não leva em conta a distribuição de dados dentro do fluxo. Muitos fluxos arbitrários contêm grandes quantidades de dados em intervalos ao longo da linha do tempo do arquivo. Fluxos de imagem, por exemplo, têm amostras que são muito grandes, mas geralmente têm um espaçamento de vários segundos de distância. A janela buffer deve ser definida para garantir que o buffer não irá exceder.

Para verificar a janela de buffer, multiplique a taxa de bits (bits por segundo) pela janela de buffer (em segundos) e divida por 1000 para obter o tamanho, em bits, do buffer para o fluxo. Em seguida, certifique-se de que o tamanho do buffer seja grande o suficiente para conter qualquer combinação de amostras no fluxo que seja menor do que a janela de buffer, além do tempo de apresentação. Em caso de dúvida, defina os dois valores um pouco mais alto do que você imagina que precisa deles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Armazenando conteúdo em buffer**](buffering-content.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




