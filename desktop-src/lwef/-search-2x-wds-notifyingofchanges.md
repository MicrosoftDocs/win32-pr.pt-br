---
title: Notificando o índice de alterações (recursos de ambiente herdado do Windows)
description: Com o Microsoft Windows Desktop Search (WDS) 2,6, os manipuladores de protocolo para um determinado armazenamento de dados podem informar ao indexador do WDS quando os dados em seu armazenamento foram alterados.
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104163577"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>Notificando o índice de alterações (recursos de ambiente herdado do Windows)

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

Com o Microsoft Windows Desktop Search (WDS) 2,6, os manipuladores de protocolo para um determinado armazenamento de dados podem informar ao indexador do WDS quando os dados em seu armazenamento foram alterados. Isso melhora o desempenho garantindo que o indexador não rastreie todo o armazenamento em índices incrementais. Usando APIs de notificação, os manipuladores de protocolo podem notificar o indexador de que um item foi movido ou excluído e pode adicionar escopos à fila de rastreamento do indexador WDS de URLs que exigem indexação. A notificação é útil para aplicativos como email, em que o manipulador de protocolo monitora o repositório e notifica o indexador de que os itens foram alterados e exigem indexação.

## <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

Os manipuladores de Protocolo notificam o indexador de alterações por meio da interface [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) . Informações sobre alterações de dados devem ser coletadas \_ em \_ estruturas de alteração de item de pesquisa e \_ tipo \_ de pesquisa de \_ tipos de enumeração de alteração e, em seguida, comunicadas ao indexador por meio do método **onitems** da interface **ISearchItemsChangedSink** .

Para acessar essa interface, um manipulador de protocolo personalizado deve primeiro criar uma instância de um objeto [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) para obter acesso ao objeto [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) . A partir daí, uma instância pode criar um objeto [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) e notificar o indexador das alterações de dados.

O método onitems permite coletar e comunicar alterações de dados no armazenamento de dados do cliente para iniciar a indexação.



| Direção | Variável              | Descrição                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| Em        | dwNumberofChanges     | Número total de alterações na notificação.                             |
| Em        | DataChangeEntries\[\] | Todas as notificações de alteração em uma matriz de estruturas de alteração de item de pesquisa \_ \_ . |
| Saída       | dwBatchId             | A ID do lote que será devolvida com erros.                       |
| Saída       | hrCompletionCodes\[\] | Indica se cada URL foi aceita para indexação.                    |



 

A estrutura de alteração do item de pesquisa \_ \_ identifica o tipo de alteração que ocorreu, bem como a URL atual do item e a URL anterior, se aplicável. A estrutura é definida da seguinte maneira:



| Nome da Propriedade | Tipo de propriedade                  | Descrição                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| Alteração        | Pesquisar \_ tipo \_ de \_ alteração       | O tipo de alteração que está sendo notificado.                                 |
| URL           | LPWSTR                         | A URL do objeto que foi alterado.                                   |
| OldURL        | LPWSTR                         | Se a notificação for uma movimentação, a URL antiga será fornecida e deverá ser exclusiva. |
| Prioridade      | \_prioridade de notificação de pesquisa \_ | A prioridade da alteração.                                                |



 

O \_ tipo \_ de pesquisa de enumeração de \_ alteração é definido da seguinte maneira:



| Valor de enumeração                           | Valor   | Descrição                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| \_Adicionar alteração de pesquisa \_                  | 0       | A notificação é para uma URL adicional.                                                      |
| Pesquisar \_ \_ excluir alteração               | 1       | A notificação é para a exclusão de uma URL.                                                  |
| Pesquisar \_ alterar \_ modificação               | 2       | A notificação é que uma URL foi modificada.                                               |
| Pesquisar \_ alterar \_ mover \_ renomear         | 3       | A notificação é para a movimentação e renomeação de um objeto para uma nova URL.                          |
| Pesquisar \_ o \_ diretório de semântica de alteração \_ | 0x10000 | A notificação é para uma URL de contêiner.                                                        |
| semântica de alteração de pesquisa \_ \_ \_ superficial   | 0x20000 | A notificação é para uma URL de contêiner que deve ter apenas suas propriedades de contêiner indexadas. |
| \_segurança de \_ semântica de alteração de pesquisa \_  | 0x40000 | A notificação é para uma URL ou URL de contêiner que teve suas propriedades de segurança alteradas.    |



 

A enumeração de prioridade de notificação de pesquisa \_ \_ é definida da seguinte maneira:



| Valor de enumeração               | Valor | Descrição                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| prioridade de pesquisa \_ normal \_ | 0     | Somente uma prioridade normal deve ser usada ao indexar a URL. Essas notificações são processadas antes da indexação incremental normal em segundo plano dos arquivos e armazenamentos de um usuário. |



 

 

 
