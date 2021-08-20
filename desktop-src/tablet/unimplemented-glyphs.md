---
description: Veja a seguir uma lista de glifos de gesto que a Microsoft planeja dar suporte no futuro como parte do reconhecedor de gestos da Microsoft.
ms.assetid: 4d504140-ff48-4a07-9bf7-a36913e44426
title: Glifos não simplificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3966ef2e4bec268bc4b45b65b6778abd434f4169ec1e2aa971703032f07ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966705"
---
# <a name="unimplemented-glyphs"></a>Glifos não simplificados

Veja a seguir uma lista de glifos de gesto que a Microsoft planeja dar suporte no futuro como parte do *reconhecedor de gestos da Microsoft.* O trabalho está em andamento para garantir que a precisão de reconhecimento desses glifos seja alta (para evitar a ativação acidental) e mapeie para as operações apropriadas.

Para garantir a consistência *dos gestos usados* para *ações comuns* entre aplicativos, você deve seguir as seguintes sugestões:

-   A *Ação* é o comportamento semântico sugerido associado ao gesto.
-   Para os gestos rotulados como *Fixo* na tabela a seguir, é recomendável que você não altere o comportamento semântico sugerido. Se um aplicativo não precisar do comportamento semântico especificado, é recomendável não reutilizar o gesto para outra ação ou semântica.
-   Você deve se sentir à vontade para associar comportamentos semânticos relevantes a todos os outros gestos. Esses gestos são rotulados como *Específicos do aplicativo.* Para esses gestos que têm um comportamento semântico sugerido, é recomendável usar o gesto para a semântica sugerida se a funcionalidade correspondente existir em seu aplicativo.
-   O ponto quente de um gesto é um ponto de distinção na geometria do gesto. O ponto quente pode ser usado para determinar onde o gesto foi feito. A API de gestos possibilita determinar o ponto quente para um determinado gesto. No entanto, nem todos os gestos têm um ponto de acesso específico e diferenciado. Para aqueles que não têm um ponto quente de distinção específico, o ponto de partida é relatado como o ponto de acesso.

> [!Note]  
> Alguns dos gestos têm um ponto de acesso diferenciado que é apenas o ponto de partida. Eles são diferenciados na tabela.

 



| Nome do gesto                      | Ação                                         | Fixo                           | Ponto de a quente                                                           |
|-----------------------------------|------------------------------------------------|---------------------------------|---------------------------------------------------------------------|
| Infinity<br/>               | Alternar para dentro e para fora do modo de gesto<br/> | Fixo<br/>                | Ponto inicial<br/>                                           |
| Cross<br/>                  | Excluir<br/>                              | Específico do aplicativo<br/> | Interseção dos traços<br/>                              |
| Marca de parágrafo<br/>         | Novo parágrafo<br/>                       | Fixo<br/>                | Ponto inicial<br/>                                           |
| Seção<br/>                | Nova seção<br/>                         | Fixo<br/>                | Ponto inicial<br/>                                           |
| Bala<br/>                 | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Cruzado de marcador<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Rabisco<br/>               | Negrito<br/>                                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Trocar<br/>                   | Exchange conteúdo<br/>                    | Específico do aplicativo<br/> | Meio do traço para cima<br/>                                  |
| Openup<br/>                 | Abrir espaço entre palavras<br/>         | Específico do aplicativo<br/> | Meio do traço para baixo<br/>                                |
| Closeup<br/>                | Fechar espaço extra<br/>                | Específico do aplicativo<br/> | Centro do espaço vertical entre os dois parênteses<br/> |
| Retângulo<br/>              | Seleciona o conteúdo incluído<br/>            | Fixo<br/>                | Ponto inicial<br/>                                           |
| Toque de círculo<br/>             | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Toque<br/>                                                      |
| Círculo circular<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Círculo cruzado<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Linha circular vertical<br/>   | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Linha circular horizontal<br/> | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Seta dupla para cima<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça da seta<br/>                                   |
| Seta dupla para baixo<br/>      | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça da seta<br/>                                   |
| Seta dupla para a esquerda<br/>      | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça da seta<br/>                                   |
| Seta dupla para a direita<br/>     | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para cima-esquerda<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para cima à direita<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para baixo-esquerda<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para baixo-direita<br/>       | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para a esquerda-para cima<br/>          | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | O Apex da cabeça de seta<br/>                               |
| Seta para a esquerda-para baixo<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para cima à direita<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Seta para a direita para baixo<br/>       | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Apex da cabeça de seta<br/>                                   |
| Diagonal-leftup<br/>        | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Diagonal-rightup<br/>       | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Diagonal-leftdown<br/>      | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Diagonal-rightdown<br/>     | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-A<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-B<br/>         | Negrito<br/>                                | Fixo<br/>                | Ponto inicial<br/>                                           |
| Letra Latina-C<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-D<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-E<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-F<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-G<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-H<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-I<br/>         | Itálico<br/>                              | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-J<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-K<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-L<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-M<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-N<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-O<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-P<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-Q<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-R<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-S<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-T<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-U<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-V<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-W<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-X<br/>         | Recortar<br/>                                 | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-Y<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Letra Latina-Z<br/>         | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-0<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-1<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito 2<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-3<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-4<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito 5<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-6<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-7<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-8<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Dígito-9<br/>                | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Ponto de interrogação<br/>          | Ajuda<br/>                                | Fixo<br/>                | Centralizar ao longo da altura da curva<br/>                     |
| Nitidamente<br/>                  | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Mina<br/>                 | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Asterisk<br/>               | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Centro<br/>                                                   |
| Plus<br/>                   | Colar<br/>                               | Fixo<br/>                | Interseção dos traços<br/>                              |
| Double-Up<br/>              | Rolar para cima<br/>                           | Fixo<br/>                | Ponto inicial<br/>                                           |
| Duplo para baixo<br/>            | Rolar para baixo<br/>                         | Fixo<br/>                | Ponto inicial<br/>                                           |
| Duplo esquerdo<br/>            | Rolar para a esquerda<br/>                         | Fixo<br/>                | Ponto inicial<br/>                                           |
| Duplo à direita<br/>           | Rolar para a direita<br/>                        | Fixo<br/>                | Ponto inicial<br/>                                           |
| Triplo<br/>              | Uma página acima<br/>                             | Fixo<br/>                | Ponto inicial<br/>                                           |
| Tripla para baixo<br/>            | Page Down<br/>                           | Fixo<br/>                | Ponto inicial<br/>                                           |
| Triplo esquerda<br/>            | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
| Triplo à direita<br/>           | Específico do aplicativo<br/>                | Específico do aplicativo<br/> | Ponto inicial<br/>                                           |
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



 

 

 




