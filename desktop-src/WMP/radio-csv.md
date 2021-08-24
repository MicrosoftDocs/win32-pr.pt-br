---
title: radio.csv
description: radio.csv
ms.assetid: 8b0a1852-b6c9-4598-b1ab-c679362794b3
keywords:
- Windows Media Player lojas online radio.csv
- lojas online, radio.csv
- Digite 1 lojas online, radio.csv
- radio.csv
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b473bfaa960dd499fae7eb309d02ccbd693b70061d0975c58357bd72e9dcc410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002936"
---
# <a name="radiocsv"></a>radio.csv

Esse arquivo contém entradas para cada feed de rádio incluído no catálogo. Cada entrada é uma linha composta pelos campos delimitados por tabulação descritos na tabela a seguir. Os campos devem aparecer na ordem listada.

A coluna Format na tabela a seguir descreve a maneira como cada campo de texto Unicode é formatado. Ele não se refere ao tipo de dados do conteúdo. Por exemplo, se Integer for indicado na coluna Format, significa que o campo contém uma cadeia de caracteres Unicode que representa um valor integral, em vez de um inteiro real.



| Campo              | Obrigatório | Formatar                                                                                                               | Descrição                                                                                                                        |
|--------------------|----------|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Radioid            | Sim      | Inteiro não negativo.                                                                                                | ID do feed de rádio que é exclusivo dentro do radio.csv.                                                                             |
| RadioTitle         | Sim      | Cadeia de caracteres Unicode. Exemplo: acertos essenciais<br/>                                                                    | Título do feed de rádio.                                                                                                                  |
| RadioSubtitle      | Não       | Cadeia de caracteres Unicode. Exemplo: Top 40.                                                                                     | Subtítulo do feed de rádio. Geralmente, um gênero ou um nome de subgênero.                                                                               |
| Programador         | Sim      | Cadeia de caracteres Unicode. Exemplo: Terri Lee Duffy                                                                             | Nome do programador do feed de rádio. É recomendável que esse campo não exceda 32 caracteres.                                     |
| PrimaryGenre       | Sim      | Inteiro não negativo.                                                                                                | A ID do gênero principal. Apenas um valor é permitido.                                                                            |
| Espírito               | Sim      | Cadeia de caracteres Unicode. Exemplo: diversão; amiable; energético elegante exuberant<br/>                                       | Uma série de adjetivos que descrevem a música. Nenhum ponto e vírgula à direita após o último adjetivo.                                    |
| Categoria           | Sim      | Cadeia de caracteres Unicode                                                                                                       | Não usado nesta versão. Deve estar vazio.                                                                                         |
| Descrição        | Não       | Cadeia de caracteres Unicode. Exemplo: upsuperando música amigável para a parte dos artistas testados e verdadeiros que não desaponta.<br/> | Descrição amigável para exibição em páginas de propriedades. É recomendável que esse campo não exceda 256 caracteres.                   |
| Popularidade         | Sim      | Valor inteiro ou decimal não negativo. Exemplo: 31<br/>                                                         | Classificação de popularidade entre os feeds de rádio. Pode ser 0.                                                                                    |
| StarRating         | Não       | Float. example: 3,21<br/>                                                                                       | Opcional. O valor, normalmente entre 0 e 5, é arredondado para o 1/4 mais próximo para exibição na interface do usuário.                   |
| IsSubscriptionOnly | Sim      | Booliano. Pode ser 0 ou 1.                                                                                              | Indica se o feed está disponível apenas por assinatura.                                                                      |
| IsRecentlyAdded    | Sim      | Booliano. Pode ser 0 ou 1.                                                                                              | Indica se este feed foi adicionado recentemente.                                                                                    |
| Isfeatured         | Sim      | Booliano. Pode ser 0 ou 1.                                                                                              | Indica se o feed está em destaque.                                                                                            |
| EditorialGlyph     | Sim      | Inteiro não negativo. Deve ser 0.                                                                                   | Não usado nesta versão. Deve ser 0.                                                                                             |
| SortOrderRank      | Sim      | Inteiro não negativo.                                                                                                | Pode ser usado para determinar a ordem de classificação quando todas as estações são listadas na interface do usuário. Deverá ser 0 se esse campo não for usado. |



 

 

 





