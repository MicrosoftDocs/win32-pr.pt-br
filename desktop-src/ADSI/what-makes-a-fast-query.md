---
title: O que faz uma consulta rápida
description: Este tópico lista os métodos de programação preferenciais a serem usados ao consultar um diretório.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- O que faz um ADSI de consulta rápida
- consultas ADSI, o que faz uma consulta rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103823986"
---
# <a name="what-makes-a-fast-query"></a>O que faz uma consulta rápida?

Considere os seguintes conceitos de aprimoramento de desempenho ao executar uma consulta:

-   Se possível, filtre apenas os atributos indexados. Use atributos de índice que você espera gerará o menor número de ocorrências. Para obter mais informações e uma lista abrangente de atributos indexados para o Windows, consulte [Active Directory esquema](/windows/desktop/ADSchema/active-directory-schema).
-   Pesquise por **objectCategory** em vez de **objectClass** porque **objectClass** não é uma propriedade indexada.
-   Esteja atento às referências. Considere Pesquisar o catálogo global se seus atributos estiverem listados como GC replicado.
-   Evite Pesquisar texto no meio e no final de uma cadeia de caracteres. Por exemplo, "CN = \* Hill \* " ou "CN = \* Larouse".
-   Suponha que uma pesquisa de subárvore retornará um grande conjunto de resultados. Use a paginação ao executar pesquisas de subárvore. O servidor será capaz de transmitir um conjunto de resultados grande em partes que reduzem os recursos de memória do lado do servidor. Isso simplifica efetivamente o uso da rede e reduz a necessidade de enviar partes extremamente grandes de dados pela rede.
-   Delimitar corretamente suas pesquisas para não recuperar mais do que o necessário.
-   Execute uma pesquisa complexa em vários atributos, pois isso é menos intensivo de desempenho do que a execução de várias pesquisas. Uma pesquisa por um objeto que lê dois atributos é mais eficiente do que duas pesquisas para o mesmo objeto, cada uma retornando um atributo.
-   Para ler o atributo com um grande número de valores, use limites de intervalo para minimizar o tamanho da pesquisa para que você possa ler alguns milhares de membros por vez. Para obter mais informações sobre como especificar limites de intervalo de atributos, consulte [recuperação de intervalo de atributos](attribute-range-retrieval.md).
-   Associar a um objeto Mantenha o identificador de associação para o restante da sessão. Não associe e desassocie para cada chamada. Se você estiver usando o ADO ou o OLE DB, não crie muitos objetos de conexão.
-   Leia o rootDSE uma vez e lembre-se do seu conteúdo para o restante da sessão.

 

 