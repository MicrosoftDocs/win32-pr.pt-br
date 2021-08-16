---
title: Paginação com IDirectorySearch
description: A paginação especifica quantas linhas o servidor retorna ao cliente.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paginação com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, paginação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48494c01831e6b69931fc6b6f779ed9b042b7fecaaf17fa62286c094a926ba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838936"
---
# <a name="paging-with-idirectorysearch"></a>Paginação com IDirectorySearch

A paginação especifica quantas linhas o servidor retorna ao cliente. Uma página pode ser definida pelo número de linhas ou um limite de tempo. O objeto COM ADSI recupera cada página de resultados com base nos valores listados na tabela a seguir. O chamador chama [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) quando atingiu o final da página e o objeto com ADSI recupera a próxima página.



| Valor                                   | Descrição                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PageSize do ADS \_ SEARCHPREF \_**           | Especifica o número máximo de linhas a serem retornadas em uma página.                                                                                                                                                                                            |
| **\_limite de \_ tempo paginado do ADS SEARCHPREF \_ \_** | Especifica o tempo máximo, em segundos, que o servidor deve gastar para coletar uma página de resultados antes de retornar a página para o cliente. Se o limite for atingido, o servidor parará a pesquisa e retornará as linhas já recuperadas para a página. |



 

Se nenhuma dessas preferências de pesquisa for definida, o padrão será nenhuma paginação. As pesquisas do Active Directory executadas sem paginação são limitadas a retornar um máximo dos primeiros 1000 registros, portanto, você deve usar uma pesquisa paginada se houver a possibilidade de que o conjunto de resultados contenha mais de 1000 itens.

Uma operação de pesquisa pode resultar em um grande número de objetos retornados. Se o servidor retornar o resultado em um conjunto, ele poderá diminuir o desempenho do cliente e do servidor, bem como afetar a carga de rede. Pesquisas paginadas podem ser usadas para evitar isso. Em uma pesquisa paginada, o cliente pode aceitar resultados em pacotes menores. O tamanho de um pacote é conhecido como o tamanho da página de pesquisa.

As pesquisas paginadas oferecem benefícios ao cliente e ao servidor. O cliente pode ser mais responsivo na apresentação dos resultados para os usuários. Isso é especialmente relevante para as ferramentas gráficas de interface do usuário que podem iniciar o processo de exibição da janela enquanto o outro thread recebe os dados simultaneamente.

No lado do servidor, as pesquisas paginadas tornam a operação escalonável. Por exemplo, se 100 clientes emitirem solicitações de pesquisa simultaneamente e, na média, cada cliente receberá 200 objetos. Se nenhum tamanho de página for especificado, no pior cenário, o servidor deverá ter memória suficiente para conter 20.000 objetos. Por outro lado, se cada cliente especifica um tamanho de página, por exemplo, dez objetos, o requisito de memória no servidor é reduzido por um fator de 20.

Além disso, usando uma pesquisa paginada, um cliente pode abandonar a operação em andamento. Por outro lado, em uma pesquisa não paginável, o cliente recebe um conjunto de resultados em um pacote. Isso pode diminuir o desempenho da rede.

A ADSI manipula o tamanho da página para o cliente. O cliente não precisa contar o número de objetos em andamento. A ADSI encapsula a interação do servidor para o cliente. Da perspectiva do cliente, a pesquisa retorna um conjunto de resultados completo.

É recomendável que a paginação seja usada.

Para especificar um tamanho máximo de página, defina uma opção de pesquisa do **ADS \_ SEARCHPREF \_ PageSize** com um valor **\_ inteiro ADSTYPE** definido como o número máximo de linhas por página na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

O exemplo de código a seguir mostra como definir o tamanho máximo da página.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Para especificar um tempo de página, defina uma opção de pesquisa de **\_ \_ \_ \_ limite de tempo paginado do ADS SEARCHPREF** com um valor **\_ inteiro de ADSTYPE** definido como o número máximo de segundos que o servidor deve gastar para recuperar uma página na matriz de [**\_ \_ informações de SEARCHPREF de anúncios**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

O exemplo de código a seguir mostra como especificar o tempo de página.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




