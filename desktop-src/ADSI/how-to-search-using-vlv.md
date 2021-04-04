---
title: Como Pesquisar usando VLV
description: O Active Directory dá suporte a pesquisas de VLV (exibição de lista virtual). Esse estilo de pesquisa é projetado especificamente para grandes conjuntos de resultados e permite que um aplicativo exiba um subconjunto de milhares de entradas sem precisar recuperar cada entrada.
ms.assetid: fea04190-0846-4b62-99f4-7d8fb35fd510
ms.tgt_platform: multiple
keywords:
- Como Pesquisar usando VLV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4a24250c8e54ccb7917f86b193152c62810b93
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917682"
---
# <a name="how-to-search-using-vlv"></a>Como Pesquisar usando VLV

O Active Directory dá suporte a pesquisas de VLV (exibição de lista virtual). Esse estilo de pesquisa é projetado especificamente para grandes conjuntos de resultados e permite que um aplicativo exiba um subconjunto de milhares de entradas sem precisar recuperar cada entrada.

Há duas maneiras diferentes de usar uma pesquisa VLV. A primeira é recuperar os atributos para entradas específicas com base em um deslocamento numérico. Esse método é útil ao recuperar resultados da pesquisa em resposta a uma operação de rolagem.

A segunda maneira de usar pesquisas de VLV é Pesquisar por parte ou por todo um atributo textual e exibir apenas os resultados da pesquisa. Um exemplo de uso disso é um catálogo de endereços. Se o usuário digitar um "s", o aplicativo poderá usar uma pesquisa VLV para pesquisar entradas que tenham um nome comum que comece com "s". Se o usuário adicionar um "m" para o "s", o aplicativo poderá usar outra pesquisa de VLV para pesquisar entradas que tenham um nome comum que comece com "SM".

Para executar uma pesquisa de VLV, instrua o ADSI a usar o controle VLV. Para fazer isso, chame o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) com uma opção de pesquisa de **\_ \_ VLV SEARCHPREF de anúncios** com um valor **\_ \_ específico de Prov ADSTYPE** . O **valor \_ \_ específico do ADSTYPE Prov** é um ponteiro para uma estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) que contém dados sobre a pesquisa. A função de exemplo [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) mostra como definir ambas as preferências de pesquisa.

Todas as pesquisas de VLV devem usar a classificação de resultados do lado do servidor, que é executada pela definição da preferência de pesquisa **SEARCHPREF de anúncios \_ \_ \_** . Para obter mais informações sobre a preferência de pesquisa do **ADS \_ SEARCHPREF \_ \_** , consulte [classificar os resultados da pesquisa com IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).

Quando uma pesquisa de VLV é executada, uma determinada quantidade de metadados sobre a pesquisa é retornada em uma coluna que é recuperada chamando [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) com o identificador de **\_ \_ resposta VLV ADS** . Esses dados estão contidos em uma [**estrutura \_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . De importância específica são os membros **dwContentCount** e **lpContextID** . O membro **dwContentCount** conterá o número de resultados que atendem aos critérios de pesquisa VLV. Esse valor pode ser usado como uma estimativa do número total de itens que seriam retornados para uma pesquisa desse tipo. O membro **lpContextID** contém um valor definido pelo servidor que pode ser passado para a próxima pesquisa para identificar a pesquisa. O uso do **lpContextID** pode melhorar o desempenho da pesquisa. Lembre-se de que **lpContextID** é um valor definido pelo servidor e seu comprimento está contido no membro **dwContextIDLength** . Esse buffer é liberado quando o método [**IDirectorySearch:: FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) é chamado, portanto, o chamador deve alocar um buffer do tamanho apropriado e copiar e salvar o conteúdo do buffer entre as pesquisas.

Para obter mais informações sobre o controle de VLV LDAP, consulte [pesquisando com o controle de VLV LDAP](/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control).

Para obter mais informações, consulte:

-   Obtendo o número de itens
-   Pesquisando por deslocamento
-   Pesquisando por cadeia de caracteres
-   [Código de exemplo para usar uma pesquisa VLV](example-code-for-using-a-vlv-search.md)

## <a name="obtaining-the-number-of-items"></a>Obtendo o número de itens

**Para obter uma estimativa do número de itens que serão retornados para uma pesquisa específica, execute as etapas a seguir.**

1.  Preencha uma [**estrutura \_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) com todos os valores zero ou **nulos** .
2.  Preencha uma [**\_ \_ informação de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) com os valores a seguir.

    -   Defina o membro **dwSearchPref** como **ADS \_ SEARCHPREF \_ VLV**.
    -   Defina o membro **vValue. dwType** como **ADSTYPE \_ Prov \_ específico**.
    -   Defina o membro **vValue. ProviderSpecific. dwLength** como o tamanho da estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
    -   Defina o membro **vValue. ProviderSpecific. lpValue** como o endereço da estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) da etapa 1.

3.  Preencha uma estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) , conforme mostrado na [classificação dos resultados da pesquisa com IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md) para classificar o atributo desejado.
4.  Preencha outras [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) para adicionar a estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) às preferências de pesquisa, conforme mostrado em [classificando os resultados da pesquisa com IDirectorySearch](sorting-the-search-results-with-idirectorysearch.md).
5.  Adicione outras preferências de pesquisa desejadas e chame [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) para definir as preferências de pesquisa.
6.  Execute a pesquisa com [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
7.  Obtenha a primeira linha de resultados chamando [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
8.  Chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) com **a \_ \_ resposta VLV do ADS** para obter os metadados de pesquisa VLV.
9.  Converta o **pADsValues->ProviderSpecific. lpValue** da estrutura de [**coluna de \_ pesquisa \_ do ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) em um ponteiro de estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . O membro **dwContentCount** desta estrutura **\_ VLV do ADS** contém o número aproximado de itens que seriam retornados por uma pesquisa desse tipo.
10. Se outras pesquisas de VLV do mesmo tipo forem executadas, faça uma cópia dos dados do **lpContextID** e preserve-as para a próxima pesquisa de VLV.

A função de exemplo [**GetVLVItemCount**](example-code-for-using-a-vlv-search.md) mostra como fazer isso.

## <a name="searching-by-offset"></a>Pesquisando por deslocamento

Uma coisa que torna a pesquisa de VLV tão rápida é que é possível pesquisar um resultado específico por um deslocamento numérico. Por exemplo, se uma pesquisa resultar em 10.000 itens sendo retornados, uma pesquisa VLV torna possível obter as informações para aproximadamente o item 4072nd sem precisar recuperar todos os itens antes do item em questão.

Os deslocamentos são especificados como uma proporção entre o deslocamento e a contagem de conteúdo. As proporções são úteis porque o servidor pode não ter uma estimativa precisa do número de entradas que existem na lista ou o tamanho da lista pode ser alterado durante o tempo que o usuário está navegando. Como você deve indicar o início e o fim da lista, você pode usar um valor estimado para a contagem de conteúdo na primeira solicitação de pesquisa, juntamente com um valor de deslocamento. O servidor usa esses dados para computar os deslocamentos correspondentes dentro da lista, com base na sua ideia de contagem de conteúdo, que é enviada em sua resposta ao cliente por meio do membro **dwContentCount** da estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) . Por exemplo, se você estimar que o tamanho da lista seja 3000 e quiser que o deslocamento seja a entrada da lista 1500, você definiria **dwContentCount** como 3000 e **dwOffset** como 1500. Se o servidor estimar o tamanho da lista real como 4500, ele recalculará o deslocamento para 2250 e retornará as novas estimativas em **dwContentCount** e **dwOffset**.

> [!Note]
>
> Todos os valores numéricos em uma pesquisa VLV são aproximações e não devem ser usados para valores absolutos. Por exemplo, se você emitir uma pesquisa VLV para o item 50 º em um ração de 100, não será garantido que você obtenha o item do meio exato.
>
> **Para procurar um item específico por deslocamento, execute as etapas a seguir.**
>
> 1.  Preencha uma [**estrutura \_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) com os valores a seguir. Membros adicionais da estrutura devem ser definidos como zero ou **NULL**.
>
>     -   Defina o membro **dwContentCount** como o valor máximo da taxa de itens a serem recuperados.
>     -   Defina o membro **dwOffset** para a taxa, em relação a **dwContentCount**, do item ou dos itens a serem recuperados.
>     -   Defina o membro **lpContextID** como o endereço da cópia do buffer de ID de contexto e o **dwContextIDLength** para o comprimento, em bytes, do buffer de ID de contexto. Se nenhuma ID de contexto tiver sido salva, ambos os membros deverão ser zero ou **NULL**.
>
> 2.  Defina as preferências de pesquisa, conforme mostrado nas etapas 2 a 5 do procedimento obtendo o número de itens.
> 3.  Execute a pesquisa com [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
> 4.  Obtenha a primeira linha de resultados chamando [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
> 5.  Chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) com o nome do atributo a ser recuperado para obter os dados reais para o item solicitado.
> 6.  Chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) com **a \_ \_ resposta VLV do ADS** para obter os metadados de pesquisa VLV.
> 7.  Converta o **pADsValues->ProviderSpecific. lpValue** da estrutura de [**coluna de \_ pesquisa \_ do ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) em um ponteiro de estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
> 8.  Faça uma cópia dos dados do **lpContextID** e preserve-o para a próxima pesquisa de VLV.

 

A função de exemplo [**GetVLVItemText**](example-code-for-using-a-vlv-search.md) mostra como fazer isso.

Também é possível recuperar mais de uma linha de dados com uma única chamada de pesquisa. Isso é feito na etapa 1 definindo os membros **dwBeforeCount** e **dwAfterCount** da estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) adequadamente. O membro **dwBeforeCount** contém o número de itens que aparecem na lista antes do item em questão e o membro **dwAfterCount** contém o número de itens que aparecem na lista depois do item em questão. Ambas as contagens excluem o item em si, portanto, definir **dwBeforeCount** como 10 e **dwAfterCount** como 10 resultará em um total de 21 itens retornados. Essa opção permite armazenar em cache os resultados da pesquisa no lado do cliente.

## <a name="searching-by-string"></a>Pesquisando por cadeia de caracteres

Também é possível usar uma pesquisa VLV para localizar itens que têm um atributo de cadeia de caracteres cujo valor corresponde a toda ou parte de uma cadeia de caracteres sem precisar recuperar todos os itens. A correspondência de cadeia de caracteres é executada em relação ao atributo especificado na estrutura de [**\_ SORTKEY do ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) do **\_ SEARCHPREF \_ classificar \_ na preferência de** pesquisa.

**Para procurar um item específico por cadeia de caracteres, execute as etapas a seguir.**

1.  Preencha uma [**estrutura \_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) com os valores a seguir. Membros adicionais da estrutura devem ser definidos como zero ou **NULL**.

    -   Defina o membro **pszTarget** como um ponteiro para uma cadeia de caracteres terminada em nulo que contenha a cadeia de caracteres a ser pesquisada.
    -   Defina o membro **lpContextID** como o endereço da cópia do buffer de ID de contexto e o **dwContextIDLength** para o comprimento, em bytes, do buffer de ID de contexto. Se nenhuma ID de contexto tiver sido salva, ambos os membros deverão ser zero ou **NULL**.

2.  Defina as preferências de pesquisa, conforme mostrado nas etapas 2 a 5 do procedimento obtendo o número de itens.
3.  Execute a pesquisa com [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch).
4.  Obtenha a primeira linha de resultados chamando [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow).
5.  Chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) com o nome do atributo a ser recuperado para obter os dados reais para o item solicitado.
6.  Chame [**IDirectorySearch:: GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) com **a \_ \_ resposta VLV do ADS** para obter os metadados de pesquisa VLV.
7.  Converta o **pADsValues->ProviderSpecific. lpValue** da estrutura de [**coluna de \_ pesquisa \_ do ADS**](/windows/desktop/api/Iads/ns-iads-ads_search_column) em um ponteiro de estrutura [**\_ VLV do ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv) .
8.  Faça uma cópia dos dados do **lpContextID** e preserve-o para a próxima pesquisa de VLV. Se necessário, o membro **dwOffset** contém o índice baseado em um do primeiro item cujo atributo de cadeia de caracteres começa com o valor especificado em **pszTarget**.

A função de exemplo [**GetVLVItemsByString**](example-code-for-using-a-vlv-search.md) mostra como fazer isso.

Da mesma forma que Pesquisar por índice, também é possível recuperar mais de uma linha de dados com uma única chamada de pesquisa. Isso é feito da mesma maneira definindo os membros **dwBeforeCount** e **dwAfterCount** da estrutura VLV do [**ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_vlv) adequadamente.

 

 