---
description: 'A API de grafo de pares usa as seguintes funções:'
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: Funções de API de gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343f3f5ff1e53180cced98cbebbd66af1d28e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828413"
---
# <a name="graphing-api-functions"></a>Funções de API de gráfico

A API de grafo de pares usa as seguintes funções:

## <a name="initialization-and-cleanup-functions"></a>Funções de inicialização e limpeza



| Função                                       | Descrição                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphShutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | Limpa todos os recursos alocados pela chamada para [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup).                     |
| [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | Indica à infraestrutura de gráfico de pares a qual versão dos protocolos pares o aplicativo de chamada requer. |



 

## <a name="graph-creation-and-access-functions"></a>Funções de criação e acesso do grafo



| Função                                   | Descrição                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | Invalida o identificador de grafo par retornado por uma chamada para [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) ou [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)e fecha todas as conexões de rede para o grafo par especificado. |
| [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | Cria um novo grafo par.                                                                                                                                                                                             |
| [**PeerGraphDelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | Exclui os dados associados a um grafo par especificado.                                                                                                                                                              |
| [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | Indica que um grafo par deve começar a escutar conexões de entrada.                                                                                                                                          |
| [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | Abre um grafo de mesmo nível que é criado anteriormente pelo nó local ou por um nó remoto.                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>Funções de informações de gráfico e de nó



| Função                                                         | Descrição                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEnumNodes**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | Cria e retorna um identificador de enumeração usado para enumerar os nós em um grafo par.                                                                             |
| [**PeerGraphGetNodeInfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | Recupera informações sobre um nó específico.                                                                                                                       |
| [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | Recupera as propriedades do grafo par atual.                                                                                                                       |
| [**PeerGraphGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | Retorna o status atual do grafo par.                                                                                                                      |
| [**PeerGraphSetNodeAttributes**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | Define os atributos da estrutura [**de \_ \_ informações do nó par**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) para o nó local.                                                                |
| [**PeerGraphSetPresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | Ativa ou desativa explicitamente a publicação de registros de presença para um nó específico. Essa função pode substituir as configurações de presença nas propriedades do grafo par. |
| [**PeerGraphSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | Define as propriedades do grafo par.                                                                                                                                    |



 

## <a name="record-management-functions"></a>Funções de gerenciamento de registros



| Função                                                                     | Descrição                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | Adiciona um novo registro a um grafo par. Um registro adicionado com essa função é enviado para cada nó em um grafo de mesmo nível.                          |
| [**PeerGraphDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | Marca um registro como excluído em um grafo par.                                                                                      |
| [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | Cria e retorna um identificador de enumeração usado para enumerar registros de um tipo específico de registro, usuário ou ambos.                    |
| [**PeerGraphGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | Recupera um registro específico com base na ID de registro especificada.                                                                       |
| [**PeerGraphSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | Pesquisa o grafo par para registros específicos.                                                                                       |
| [**PeerGraphUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | Atualiza um registro no grafo par e, em seguida, inunda o registro para cada nó no grafo par.                                       |
| [**PeerGraphValidateDeferredRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | Indica à infraestrutura de gráfico de pares que é hora de reenviar quaisquer registros adiados para que o módulo de segurança seja validado. |



 

## <a name="export-and-import-functions"></a>Funções de exportação e importação



| Função                                                   | Descrição                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | Exporta um banco de dados de grafo par para um arquivo que você pode mover para um computador diferente. |
| [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | Importa um arquivo que contém as informações de um banco de dados de grafo par.             |



 

## <a name="utility-and-support-functions"></a>Funções de utilitário e suporte



| Função                                                                     | Descrição                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | Libera um identificador de enumeração e libera os recursos associados a uma enumeração.                                           |
| [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | Libera recursos que várias das funções de API de grafo de pares retornam.                                                           |
| [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | Recupera o número de itens em uma enumeração.                                                                                  |
| [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | Obtém o próximo item ou itens em uma enumeração criada por uma chamada para funções específicas, que retornam uma enumeração de pares.        |
| [**PeerGraphPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | Converte o valor de tempo de referência mantido do grafo de pares em um valor de hora localizado apropriado para exibição no computador do par. |
| [**PeerGraphUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | Converte um valor de tempo universal do computador do par em um valor de tempo do grafo de pares comum.                                       |



 

## <a name="connection-functions"></a>Funções de conexão



| Função                                                                 | Descrição                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | Fecha uma conexão direta especificada.                                                                                                                                                                                                          |
| [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | Tenta estabelecer uma conexão com um nó especificado em um grafo par. Essa função inicia uma operação assíncrona.                                                                                                                             |
| [**PeerGraphEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | Cria e retorna um identificador de enumeração usado para enumerar as conexões de um nó local.                                                                                                                                                   |
| [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | Permite que um aplicativo estabeleça uma conexão direta com um nó em um grafo de mesmo nível. A conexão só poderá ser feita se o nó ao qual o aplicativo está se conectando tiver assinado com o evento de **\_ \_ \_ \_ conexão direta do evento de grafo de pares** . |
| [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | Envia dados para um nó vizinho ou um nó conectado diretamente.                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>Funções de infraestrutura de eventos



| Função                                                     | Descrição                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | Recupera eventos de mesmo nível.                                                                                       |
| [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | Registra a solicitação de um par para ser notificado das alterações associadas a um grafo de mesmo nível e tipo de evento.            |
| [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | Solicita que o aplicativo não seja mais notificado sobre as alterações associadas a um grafo par e tipo de registro. |



 

 

 



