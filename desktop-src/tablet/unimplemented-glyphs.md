---
description: Veja a seguir uma lista de glifos de gestos para os quais a Microsoft planeja dar suporte no futuro como parte do reconhecedor de gestos da Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glifos não implementados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d479c6f3b486706b9e8d063ae2bc46daf5a0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164431"
---
# <a name="unimplemented-glyphs"></a>Glifos não implementados

Veja a seguir uma lista de glifos de gestos para os quais a Microsoft planeja dar suporte no futuro como parte do *reconhecedor de gestos da Microsoft*. O trabalho está em andamento para garantir que a precisão do reconhecimento para esses glifos seja alta (para evitar a ativação acidental) e que eles sejam mapeados para as operações apropriadas.

Para garantir a consistência dos *gestos* usados para *ações* comuns entre aplicativos, você deve seguir as seguintes sugestões:

-   A *ação* é o comportamento semântico sugerido associado ao gesto.
-   Para os gestos rotulados como *corrigidos* na tabela a seguir, é recomendável que você não altere o comportamento semântico sugerido. Se um aplicativo não precisar do comportamento semântico especificado, é recomendável que você não reutilize o gesto para outra ação ou semântica.
-   Você deve se sentir à vontade para associar comportamentos semânticos relevantes a todos os outros gestos. Esses gestos são rotulados como *específicos do aplicativo*. Para os gestos que têm um comportamento semântico sugerido, é recomendável que você use o gesto para a semântica sugerida se a funcionalidade correspondente existir no seu aplicativo.
-   O ponto de acesso de um gesto é um ponto de distinção na geometria do gesto. O ponto de acesso pode ser usado para determinar onde o gesto foi feito. A API de gestos possibilita determinar o ponto de acesso de um determinado gesto. No entanto, nem todos os gestos têm um ponto de acesso diferencial específico. Para aqueles que não têm um ponto de acesso diferencial específico, o ponto de partida é relatado como ponto de acesso.

> [!Note]  
> Alguns dos gestos têm um ponto de acesso diferenciado que acaba sendo o ponto de partida. Eles são diferenciados na tabela.

 



| Nome do gesto                      | Ação                                         | Fixo                           | Ponto de acesso                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infinito<br/>               | Alternar para dentro e para fora do modo de gesto<br/> | Fixo<br/>                | Ponto de partida<br/>                                           |
| Cross<br/>                  | Excluir<br/>                              | Específico do aplicativo<br/> | Interseção dos traços<br/>                              |
| Marca de parágrafo<br/>         | Novo parágrafo<br/>                       | Fixo<br/>                | Ponto de partida<br/>                                           |
| Seção<br/>                | Nova seção<br/>                         | Fixo<br/>                | Ponto de partida<br/>                                           |
| Listas<br/>                 | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Com marcadores-cruzado<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Rabisco<br/>               | Negrito<br/>                                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Trocar<br/>                   | Conteúdo do Exchange<br/>                    | Específico do aplicativo<br/> | Meio do traço acima<br/>                                  |
| Openup<br/>                 | Abrir espaço entre palavras<br/>         | Específico do aplicativo<br/> | Meio do traço abaixo<br/>                                |
| Closeup<br/>                | Fechar espaço extra<br/>                | Específico do aplicativo<br/> | Centro do espaço vertical entre os dois parênteses<br/> |
| Retângulo<br/>              | Seleciona conteúdo incluído<br/>            | Fixo<br/>                | Ponto de partida<br/>                                           |
| Círculo-toque<br/>             | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Toque<br/>                                                      |
| Círculo-círculo<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Círculo cruzado<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Círculo-linha-vertical<br/>   | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Círculo-linha-horizontal<br/> | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Seta dupla para cima<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta dupla para baixo<br/>      | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta dupla-esquerda<br/>      | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta dupla-direita<br/>     | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para cima-esquerda<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para cima à direita<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para baixo-esquerda<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para baixo-direita<br/>       | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para a esquerda-para cima<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | O Apex da cabeça de seta<br/>                               |
| Seta para a esquerda-para baixo<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para cima à direita<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para a direita para baixo<br/>       | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Diagonal-leftup<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Diagonal-rightup<br/>       | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Diagonal-leftdown<br/>      | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Diagonal-rightdown<br/>     | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-A<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-B<br/>         | Negrito<br/>                                | Fixo<br/>                | Ponto de partida<br/>                                           |
| Letra Latina-C<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-D<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-E<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-F<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-G<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-H<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-I<br/>         | Itálico<br/>                              | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-J<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-K<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-L<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-M<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-N<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-O<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-P<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-Q<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-R<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-S<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-T<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-U<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-V<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-W<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-X<br/>         | Recortar<br/>                                 | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-Y<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Letra Latina-Z<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-0<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-1<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito 2<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-3<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-4<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito 5<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-6<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-7<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-8<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Dígito-9<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Ponto de interrogação<br/>          | Ajuda<br/>                                | Fixo<br/>                | Centralizar ao longo da altura da curva<br/>                     |
| Nitidamente<br/>                  | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Mina<br/>                 | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Asterisk<br/>               | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Centro<br/>                                                   |
| Acrescido<br/>                   | Colar<br/>                               | Fixo<br/>                | Interseção dos traços<br/>                              |
| Double-Up<br/>              | Rolar para cima<br/>                           | Fixo<br/>                | Ponto de partida<br/>                                           |
| Duplo para baixo<br/>            | Rolar para baixo<br/>                         | Fixo<br/>                | Ponto de partida<br/>                                           |
| Duplo esquerdo<br/>            | Rolar para a esquerda<br/>                         | Fixo<br/>                | Ponto de partida<br/>                                           |
| Duplo à direita<br/>           | Rolar para a direita<br/>                        | Fixo<br/>                | Ponto de partida<br/>                                           |
| Triplo<br/>              | Uma página acima<br/>                             | Fixo<br/>                | Ponto de partida<br/>                                           |
| Tripla para baixo<br/>            | Page Down<br/>                           | Fixo<br/>                | Ponto de partida<br/>                                           |
| Triplo esquerda<br/>            | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Triplo à direita<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto de partida<br/>                                           |
| Colchete para cima<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Midpoint<br/>                                                 |
| Entre colchetes<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Midpoint<br/>                                                 |
| Colchete à esquerda<br/>           | Início da seleção<br/>                  | Fixo<br/>                | Midpoint<br/>                                                 |
| Colchete à direita<br/>          | Fim da seleção<br/>                    | Fixo<br/>                | Midpoint<br/>                                                 |
| Chaves<br/>             | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Midpoint<br/>                                                 |
| Chave-em<br/>            | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Midpoint<br/>                                                 |
| Chave-esquerda<br/>             | Início da seleção descontínua<br/>    | Fixo<br/>                | Midpoint<br/>                                                 |
| Chave à direita<br/>            | Fim da seleção descontínua<br/>      | Fixo<br/>                | Midpoint<br/>                                                 |
| Toque triplo<br/>             | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | O ponto de partida está diferenciando o ponto de acesso<br/>               |
| Toque quádruplo<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | O ponto de partida está diferenciando o ponto de acesso<br/>               |



 

 

 




