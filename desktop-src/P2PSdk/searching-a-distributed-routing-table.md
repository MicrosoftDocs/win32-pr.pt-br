---
description: Antes que um aplicativo possa Pesquisar a DRT (tabela de roteamento distribuído), uma consulta de pesquisa deve ser criada.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Pesquisando uma tabela de roteamento distribuída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780490"
---
# <a name="searching-a-distributed-routing-table"></a>Pesquisando uma tabela de roteamento distribuída

Antes que um aplicativo possa Pesquisar a DRT (tabela de roteamento distribuído), uma consulta de pesquisa deve ser criada. O valor de chave desejado é especificado pelo aplicativo quando a função [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) é chamada. O comportamento da pesquisa é determinado pelas informações especificadas pelo aplicativo na estrutura de [**informações de \_ pesquisa \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .

Normalmente, um evento de aplicativo é sinalizado quando a pesquisa descobre resultados e outra na conclusão da pesquisa. No entanto, se **fIterative** for definido em [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info), um evento de aplicativo poderá ser sinalizado quando o contato for feito com cada nó ao longo do caminho.

Depois que um evento é sinalizado, o aplicativo chama a função [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) para os resultados. Se o código retornado for **S \_ OK**, os resultados serão apontados na estrutura [**de \_ \_ resultados da pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) retornada pela API. Os resultados retornados se enquadram no intervalo de valores especificado em [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). Caso a pesquisa não encontre nenhuma correspondência, somente o valor **DRT \_ E \_ nenhum \_ maior** será retornado na conclusão dos retornos de resultado.

As informações a seguir detalham como os membros contidos nas [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) permitem que um aplicativo dite especificamente o comportamento de pesquisa da infraestrutura DRT:

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

Por padrão, os resultados da pesquisa DRT incluem somente correspondências encontradas fora do nó local. A configuração de **fAllowCurrentInstanceMatch** especifica que os resultados da pesquisa também incluem correspondências encontradas na instância DRT local.

## <a name="cmaxendpoints"></a>cMaxEndpoints

A quantidade e o intervalo dos resultados retornados pela pesquisa são especificados pelo aplicativo com os valores de **cMaxEndpoints** (quantidade) e **pMinimumKey** e **pMaximumKey** (intervalo) e referenciados pelas informações de [**\_ pesquisa DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_info).

Quando **cMaxEndpoints = 1**, a infraestrutura DRT procura uma chave, retornando uma correspondência dentro do intervalo especificado pelos valores **pMinimumKey** e **PMaximumKey** nas [**informações de \_ pesquisa \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). Essa correspondência pode ser uma correspondência exata ou a correspondência mais próxima no intervalo. Se uma correspondência não for encontrada, **DRT \_ E \_ não \_ mais** será retornado.

Se **cMaxEndpoints > 1**, a infraestrutura DRT retornará correspondências dentro do intervalo até o valor de **cMaxEndpoints**. As correspondências retornadas podem conter uma correspondência exata ou os resultados de correspondência mais próximos no intervalo. Além disso, se **pMinimumKey** e **pMaximumKey** forem definidos com o mesmo valor, uma pesquisa será executada somente para esse valor, retornando **DRT \_ E \_ não \_ mais** se não for encontrada.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

O membro **fAnyMatchInRange** indica se a pesquisa será interrompida depois que a primeira correspondência estiver localizada dentro do intervalo especificado, ou se a pesquisa continuar para a correspondência mais próxima à chave especificada na API [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) . Quando **fAnyMatchInRange** é definido, a pesquisa é executada com **cMaxEndpoints = 1** , independentemente do valor especificado de **CMaxEndpoints** nas [**\_ \_ informações de pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

O membro **fIterative** especifica se cada nó contatado pela infraestrutura DRT durante a pesquisa terá os dados de chave/ponto de extremidade associados a ele disponibilizados para o aplicativo por meio do [**\_ \_ resultado da pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result). Ao definir **fIterative** como **true**, o valor de **cMaxEndpoints = 1** será forçado. Quando **fIterative** é definido como **true** em uma consulta de pesquisa para o DRT, o aplicativo é chamado de volta após o contato com cada nó ou "hop". Cada resultado de salto contém uma chave que indica qual nó será pesquisado pelo DRT em seguida. Um resultado de salto é retornado por meio de [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) como um resultado **\_ \_ intermediário de correspondência DRT** .

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey e pMaximumKey

Os membros **pMinimumKey** e **pMaximumKey** podem ser usados para pesquisar chaves que estejam dentro de um intervalo. Se o membro **fAnyMatchInRange** for definido como **false**, o DRT retornará as chaves mais próximas para o destino de pesquisa (especificado usando o argumento PKey passado na função [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) ) que se enquadram dentro do intervalo. Observe que o argumento *pKey* passado para **DrtStartSearch** deve estar dentro do intervalo definido por **pMinimumKey** e **pMaximumKey**. Para procurar uma chave precisa, defina **pMinimumKey**, **pMaximumKey** e *pKey* com o mesmo valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando e cancelando o registro de chaves](registering-and-deregistering-keys.md)
</dt> <dt>

[Sobre tabelas de roteamento distribuído](about-distributed-routing-tables.md)
</dt> <dt>

[Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



