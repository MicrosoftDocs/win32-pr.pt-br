---
title: Seção Descrição
description: Seção Descrição
ms.assetid: 280a9a4d-935f-440d-a606-94aeba0007db
keywords:
- Windows Media Player Capas móveis, seção Descrição
- skins, seção Descrição
- criando capas, seção Descrição
- escrevendo código para capas, seção Descrição
- Seção de descrição em capas
- arquivos de definição de capa, seção Descrição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96735f07432f8075fe1842d97a4ff1737c65c25ae7ac75ddd61b805460ba6293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839538"
---
# <a name="description-section"></a>Seção Descrição

Em seguida, você deve fornecer uma seção que descreve o tamanho e a orientação da capa ao criar uma capa para o Windows Media Player Série 9 para o Windows Mobile 2003 e versões posteriores:


```C++
[ Description ]
//              <X,Y>       <DPI>
//              ------      -----
    Dimensions  240, 320    96

//    <Orientation>
//    -------------
    Orientation Portrait

```



A seção Descrição deve começar com a palavra Descrição entre colchetes e, em seguida, incluir uma linha que especifica as dimensões e a resolução de exibição para a capa.

As linhas que começam com duas barras não são processadas e podem ser usadas para comentários ou, conforme mostrado no código anterior, um modelo para ajudá-lo a se lembrar do que acontece em uma seção. Você também pode usar modelos para ajudar a alinhar tudo em colunas.

Para obter mais informações sobre a seção Descrição, consulte [Descrição](description.md) na Referência de capa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escrevendo o código**](writing-the-code.md)
</dt> </dl>

 

 




