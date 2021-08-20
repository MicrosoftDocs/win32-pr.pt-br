---
title: Combinações de texto
description: Combinações de texto
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player Aparências móveis, letreiros
- capas, letreiros
- referência para capas, letreiros
- letreiros em capas, combinações de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0d937d0ae2f90fe37ea8f4af1208443bbb127d622a83ecb5f556ddff596824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933414"
---
# <a name="text-combinations"></a>Combinações de texto

Esse valor é uma lista de combinações de caixa de exibição de texto, separadas por vírgulas. As caixas de exibição de texto podem ser Unidas em conjunto por um caractere de adição para criar um novo valor de exibição de letreiro e qualquer tipo de texto definido na seção tipo de texto pode ser usado em seu letreiro.

ao determinar o que exibir, Windows Media Player Mobile avalia cada item da lista para ver se todas as partes estão disponíveis. Caso contrário, o próximo item será avaliado e assim por diante, até que todas as partes disponíveis sejam encontradas. Por exemplo, se você quiser exibir autor e título, mas não tiver certeza se ambos estão disponíveis, use o seguinte valor:


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

 

 




