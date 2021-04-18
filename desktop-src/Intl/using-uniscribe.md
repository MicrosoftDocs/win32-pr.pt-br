---
description: O Uniscribe fornece APIs para dar suporte à tipografia e dar suporte à exibição e edição de texto internacional, incluindo as complexas regras de scripts do Oriente Médio e asiático.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Usando o Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810163"
---
# <a name="using-uniscribe"></a>Usando o Uniscribe

O Uniscribe fornece APIs para dar suporte à tipografia e dar suporte à exibição e edição de texto internacional, incluindo as complexas regras de scripts do Oriente Médio e asiático. O Uniscribe fornece rotinas de baixo nível para lidar com texto totalmente formatado e uma API ScriptString simples definida para texto não formatado.

Usando o Uniscribe, os aplicativos precisam apenas gerenciar um repositório de backup de códigos de caracteres Unicode. Os aplicativos de layout de texto não precisam manter nenhum outro buffer ou tabela de mapeamento para rastrear a ordem dos caracteres. Cada aplicativo só precisa armazenar e gerenciar a ordem na qual os caracteres são inseridos pelo usuário, que é a mesma ordem lógica definida por Unicode. O armazenamento de backup nunca muda como resultado de operações de layout. O Uniscribe mantém um índice dos clusters reordenados para os limites de caracteres originais passados pelo aplicativo.

Os tópicos a seguir são abordados nesta seção.

**Formatação**

-   [Determinando se um script requer formatação de glifos](determining-if-a-script-requires-glyph-shaping.md)
-   [Usando mecanismos de shaping](using-shaping-engines.md)

**Outro processamento**

-   [Cache](caching.md)
-   [Exibindo texto com o Uniscribe](displaying-text-with-uniscribe.md)
-   [Processando scripts complexos](processing-complex-scripts.md)
-   [Usando fallback de fonte](using-font-fallback.md)
-   [Usando as funções ScriptString](using-the-scriptstring-functions.md)

**Acento**

-   [Exibindo o cursor em cadeias bidirecionais](displaying-the-caret-in-bidirectional-strings.md)
-   [Gerenciando posicionamento de cursor e teste de clique](managing-caret-placement-and-hit-testing.md)
-   [Convertendo o deslocamento de clique do mouse X na posição do cursor](translating-mouse-hit-x-offset-to-caret-position.md)

**Palavras e clusters de caracteres**

-   [Usando clusters de caracteres](using-character-clusters.md)
-   [Usando pontos de quebra de palavras](using-word-break-points.md)
-   [Trabalhando com relações entre posições de cursor, pontos de justificações e clusters](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



