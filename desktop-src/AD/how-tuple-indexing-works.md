---
title: Como funciona a indexação de tupla
description: Os índices de tupla são usados para otimizar as pesquisas que têm 0 ou mais cadeias de caracteres de pesquisa de média e 0 ou 1 cadeias de caracteres de pesquisa final. Eles também podem ser usados para otimizar as pesquisas de uma cadeia de caracteres de pesquisa inicial se nenhum índice comum estiver disponível nesse atributo.
ms.assetid: 0f7b3f64-70cd-4581-a9ab-bb882eabef8c
ms.tgt_platform: multiple
keywords:
- indexação de tupla
- Pesquisando Active Directory Active Directory, otimização
- Active Directory, Active Directory de otimização da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607b9a50ef0ec367bea95f82afd89aa39fbf5b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640396"
---
# <a name="how-tuple-indexing-works"></a>Como funciona a indexação de tupla

Os índices de tupla são usados para otimizar as pesquisas que têm 0 ou mais [cadeias de caracteres de pesquisa de média](search-string-types.md) e 0 ou 1 cadeias de caracteres de pesquisa final. Eles também podem ser usados para otimizar as pesquisas de uma cadeia de caracteres de pesquisa inicial se nenhum índice comum estiver disponível nesse atributo.

Você pode ativar a indexação de tupla para um atributo definindo o bit 5, que corresponde ao valor 32, no atributo [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) . Esse atributo é definido no objeto de esquema que representa o atributo que precisa do índice de tupla. O impacto no desempenho de ativar a indexação de tupla é que qualquer valor de cadeia de caracteres definido para esse atributo será expandido em um grande número de fragmentos no índice de tupla. Quando um atributo é expandido, ele consome uma quantidade maior de espaço em disco no arquivo da árvore de informações do diretório e também é atualizado mais lentamente.

Os índices de tupla são projetados para acelerar as pesquisas do formulário `*string*` . A aceleração pode ser considerável, pois essa forma de pesquisa não pode ser otimizada de nenhuma outra maneira e, em seu formato não otimizado, força o servidor de Active Directory a percorrer cada objeto no escopo da pesquisa para executar a consulta. Portanto, uma pesquisa de base simplesmente pesquisaria um objeto, que usaria menos recursos, uma pesquisa de filhos imediata pesquisaria apenas os filhos de um objeto (o que poderia usar menos recursos ou mais recursos, dependendo do tamanho do contêiner), e uma pesquisa de subárvore percorrerá toda a subárvore sob o objeto base, o que geralmente exigiria muitos recursos e seria muito lento devido ao tamanho

Os índices de tupla funcionam dividindo uma cadeia de caracteres em *tuplas*. Por exemplo, a cadeia de caracteres "Active Directory" seria dividida nas seguintes tuplas:

-   ` "Active Dir"`
-   ` "ctive Dire"`
-   ` "tive Direc"`
-   ` "ive Direct"`
-   ` "ve Directo"`
-   ` "e Director"`
-   ` " Directory"`
-   ` "Directory"`
-   ` "irectory"`
-   ` "rectory"`
-   ` "ectory"`
-   ` "ctory"`
-   ` "tory"`
-   ` "ory"`

> [!Note]  
> O diretório será interrompido em 32767 caracteres ao expandir uma cadeia de caracteres para indexação de tupla.

 

Um índice de tupla conterá uma entrada para cada uma dessas tuplas. Portanto, se um usuário procurar `*cto*` , o servidor de Active Directory pesquisará todas as correspondências para "CTO" no índice e, nesse caso, localizará um ponteiro de volta para o registro que tinha um atributo (tupla indexada) com um valor de "Directory".

Se a cadeia de caracteres de pesquisa medial ( `*cto*` no exemplo anterior) for específica o suficiente, a pesquisa será bastante eficiente, pois reduz consideravelmente o número de objetos que o servidor de Active Directory deve inspecionar para executar a consulta.

 

 