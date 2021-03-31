---
title: Seção de descrição
description: Seção de descrição
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Capas móveis do Windows Media Player, seção Descrição
- capas, seção de descrição
- Criando capas, seção de descrição
- escrevendo código para capas, seção de descrição
- Seção de descrição em capas
- arquivos de definição de capa, seção de descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9518b6b1de128457dc3e6b3738ddab9be2a873
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822958"
---
# <a name="description-section"></a>Seção de descrição

Em seguida, você deve fornecer uma seção que descreve o tamanho e a orientação da capa ao criar uma capa para o Windows Media Player 9 Series para Windows Mobile 2003 e versões posteriores:


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



A seção descrição deve começar com a palavra descrição entre colchetes e, em seguida, incluir uma linha que especifica as dimensões e a resolução de exibição da capa.

As linhas que começam com duas barras invertidas não são processadas e podem ser usadas para comentários ou, conforme mostrado no código anterior, um modelo para ajudá-lo a se lembrar do que acontece em uma seção. Você também pode usar modelos para ajudar a alinhar tudo em colunas.

Para obter mais informações sobre a seção Descrição, consulte [Descrição](description.md) na referência de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo o código**](writing-the-code.md)
</dt> </dl>

 

 




