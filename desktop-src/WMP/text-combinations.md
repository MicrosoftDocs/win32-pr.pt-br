---
title: Combinações de texto
description: Combinações de texto
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Aparências móveis do Windows Media Player, letreiros
- capas, letreiros
- referência para capas, letreiros
- letreiros em capas, combinações de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498728"
---
# <a name="text-combinations"></a>Combinações de texto

Esse valor é uma lista de combinações de caixa de exibição de texto, separadas por vírgulas. As caixas de exibição de texto podem ser Unidas em conjunto por um caractere de adição para criar um novo valor de exibição de letreiro e qualquer tipo de texto definido na seção tipo de texto pode ser usado em seu letreiro.

Ao determinar o que exibir, o Windows Media Player Mobile avalia cada item na lista para ver se todas as partes estão disponíveis. Caso contrário, o próximo item será avaliado e assim por diante, até que todas as partes disponíveis sejam encontradas. Por exemplo, se você quiser exibir autor e título, mas não tiver certeza se ambos estão disponíveis, use o seguinte valor:


```C++
Title+Author, Title, Author

```



No exemplo anterior, o título + autor será exibido se o título e o autor tiverem sido definidos para o item de mídia. Se ambos não estiverem definidos, o título será avaliado e exibido se definido. Se o título não for definido, o autor será exibido, se definido. Se nenhum for definido, nada será exibido.

Ao usar o sinal de adição para concatenação, certifique-se de que você não tem espaços em nenhum dos lados do sinal de adição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Marquee**](marquee.md)
</dt> <dt>

[**Tipo de texto**](text-type.md)
</dt> </dl>

 

 




