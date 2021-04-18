---
title: Recuperando conjuntos de resultados grandes
description: Quando há a possibilidade de que o conjunto de resultados que será retornado contenha mais de 1000 itens, você deve usar uma pesquisa paginada.
ms.assetid: 1439d6b8-50dd-4d37-bcc9-dd0f63af865f
ms.tgt_platform: multiple
keywords:
- Recuperando o ADSI de conjuntos de resultados grandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f8902d25010690953cfae8a03ff9e500b4ebda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755697"
---
# <a name="retrieving-large-results-sets"></a>Recuperando conjuntos de resultados grandes

Quando há a possibilidade de que o conjunto de resultados que será retornado contenha mais de 1000 itens, você deve usar uma pesquisa paginada. Pesquisas de Active Directory executadas sem paginação são limitadas a retornar um máximo dos primeiros 1000 registros. Com uma pesquisa paginada, o conjunto de resultados é apresentado como páginas individuais, cada um contendo um número predeterminado de entradas de resultados. Com esse tipo de pesquisa, novas páginas de entradas de resultado são retornadas até que o final do conjunto de resultados seja atingido.

Por padrão, o servidor que responde a uma solicitação de consulta calcula completamente um conjunto de resultados antes de retornar os dados. Em um conjunto de resultados grande, isso requer memória de servidor, pois o conjunto de resultados é adquirido e largura de banda de rede quando o resultado grande é retornado. Definir um tamanho de página permite que o servidor envie os dados em páginas à medida que as páginas estão sendo compiladas. Em seguida, o cliente armazena em cache esses dados e fornece um cursor para o código de nível de aplicativo. A paginação é definida definindo quantas linhas o servidor calcula antes que os dados sejam retornados pela rede para o cliente.

A pesquisa paginável oferece benefícios para o cliente e o servidor. Por exemplo, o cliente pode ser mais responsivo na apresentação dos resultados para os usuários finais. Isso é especialmente relevante para ferramentas gráficas de interface do usuário que podem exibir dados enquanto outro thread recebe simultaneamente mais dados do servidor.

Ao configurar sua consulta, se você especificar uma ordem de classificação para o conjunto de resultados, o servidor deverá calcular completamente o conjunto de resultados antes de retornar os dados para o cliente, o que afeta o tempo de resposta para a consulta.

No lado do servidor, a pesquisa paginável torna a operação escalonável. Por exemplo, se 100 clientes emitirem solicitações de pesquisa simultaneamente e, na média, cada cliente for retornado 200 objetos, se o tamanho da página não for especificado, o servidor deverá ter memória suficiente para manter o conjunto de resultados completo de entradas 20.000. Como alternativa, se cada cliente especificou um tamanho de página de dez objetos, os requisitos de memória no servidor seriam reduzidos em um fator de 20.

> [!Note]  
> Nem todos os serviços de diretório dão suporte a pesquisas paginadas. Active Directory implementa a arquitetura de tamanho de página.

 

Muitos servidores de diretório especificam um limite administrativo para o número máximo de objetos que eles podem retornar se um cliente não especificar o tamanho da página. Quando o limite administrativo é atingido, a ADSI gera o erro de **\_ limite de administrador de DS \_ \_ \_ excedido** .

No lado do cliente, uma pesquisa paginada permite que um cliente pare a operação enquanto ela ainda está em andamento. Por outro lado, em uma pesquisa não paginável, o cliente é bloqueado até que os dados sejam completamente retornados ou ocorre um erro. Isso pode afetar o desempenho da rede se o conjunto de resultados for maior e levar mais tempo do que o esperado.

Em nome do cliente, a ADSI manipula o tamanho da página de forma transparente. O cliente não precisa contar o número de objetos em andamento. A ADSI encapsula a interação do servidor para o cliente. Da perspectiva do cliente, a pesquisa retorna um conjunto de resultados completo.

Para obter mais informações sobre como usar a opção tempo limite de pesquisa com uma interface de pesquisa específica, consulte:

-   [Paginação com IDirectorySearch](paging-with-idirectorysearch.md)
-   [Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

Uma pesquisa paginada é transparente para seu aplicativo porque a ADSI continua automaticamente a recuperar páginas adicionais de resultados até atingir o final do conjunto de resultados ou o fim do limite de tempo definido. Quando você usa uma pesquisa paginada, o limite de tamanho não substitui o tamanho da página. O limite de tamanho só pode ser usado quando você recupera um conjunto de resultados que contém menos de 1000 entradas.

 

 




