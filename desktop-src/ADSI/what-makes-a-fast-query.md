---
title: O que faz uma consulta rápida
description: Este tópico lista os métodos de programação preferenciais a usar ao consultar um diretório.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- O que faz uma ADSI de consulta rápida
- consultas ADSI , o que faz uma consulta rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134d391c728d543c407ee770081e2ced96afbba86d205462e814d89f74e82a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589836"
---
# <a name="what-makes-a-fast-query"></a>O que faz uma consulta rápida?

Considere os seguintes conceitos de melhoria de desempenho ao executar uma consulta:

-   Se possível, filtre somente atributos indexados. Usar atributos de índice esperados gerará o menor número de acertos. Para obter mais informações e uma lista abrangente de atributos indexados para Windows, consulte [Esquema do Active Directory](/windows/desktop/ADSchema/active-directory-schema).
-   **Pesquise objectCategory em** vez **de objectClass** porque **objectClass** não é uma propriedade indexada.
-   Esteja ciente das indicações. Considere pesquisar o catálogo global se os atributos estão listados como replicados por GC.
-   Evite pesquisar texto no meio e no final de uma cadeia de caracteres. Por exemplo, "cn= \* \* montanhe" ou "cn= \* lação".
-   Suponha que uma pesquisa de subárvore retornará um conjunto de resultados grande. Use paging ao executar pesquisas de subárvore. Em seguida, o servidor poderá transmitir um grande conjunto de resultados em partes, reduzindo os recursos de memória do lado do servidor. Isso efetivamente nivela o uso da rede e reduz a necessidade de enviar partes extremamente grandes de dados pela rede.
-   Escopo correto de suas pesquisas para não recuperar mais do que o necessário.
-   Execute uma pesquisa complexa em vários atributos, pois é menos intensivo de desempenho do que executar várias pesquisas. Uma pesquisa por um objeto que lê dois atributos é mais eficiente do que duas pesquisas para o mesmo objeto, cada um retornando um atributo.
-   Para ler o atributo com um grande número de valores, use limites de intervalo para minimizar o tamanho da pesquisa para que você possa ler alguns milhares de membros por vez. Para obter mais informações sobre como especificar limites de intervalo de atributos, consulte [Recuperação de intervalo de atributos.](attribute-range-retrieval.md)
-   A associação a um objeto mantém o identificador de associação para o restante da sessão. Não a bind e unbind para cada chamada. Se você estiver usando ADO ou OLE DB, não crie muitos objetos de conexão.
-   Leia o rootDSE uma vez e lembre-se de seu conteúdo para o restante da sessão.

 

 