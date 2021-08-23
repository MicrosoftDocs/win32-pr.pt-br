---
description: 'A API de Agrupação usa as seguintes funções:'
ms.assetid: 56ea2880-b468-4816-b6c9-5780c807b3f1
title: Funções de API de agrupação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 888a64096f66a9adf048d91c2d577d71203a03da6d1b698f2ea305396c4be0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776166"
---
# <a name="grouping-api-functions"></a>Funções de API de agrupação

A API de Agrupação usa as seguintes funções:

## <a name="group-initialization-and-cleanup-functions"></a>Funções de inicialização e limpeza de grupo



| Função                                       | Descrição                                                                                                            |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown) | Fecha um grupo de pares criado com [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) e descarta todos os recursos alocados. |
| [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup)   | Inicia um grupo de pares usando uma versão solicitada da infraestrutura par.                                        |



 

## <a name="group-creation-and-access-functions"></a>Funções de criação e acesso de grupo



| Função                                                                       | Descrição                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)                                       | Invalida o alça do grupo de pares obtido por uma chamada anterior para a função [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)ou [**PeerGroupOpen.**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) |
| [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)                                   | Inicia uma pesquisa PNRP para um grupo de pares e tenta se conectar a ele. Depois que essa função é chamada com êxito, um par pode se comunicar com outros membros do grupo par.                             |
| [**PeerGroupConnectByAddress**](/windows/desktop/api/P2P/nf-p2p-peergroupconnectbyaddress)                 | Tenta se conectar ao grupo de pares em que outros pares com endereços IPv6 conhecidos estão participando.                                                                                                       |
| [**PeerGroupCriar**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate)                                     | Cria um novo grupo de pares.                                                                                                                                                                                    |
| [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation)                 | Retorna uma cadeia de caracteres XML que pode ser usada pelo par especificado para ingressar em um grupo.                                                                                                                                |
| [**PeerGroupCreatePasswordInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreatepasswordinvitation) | Retorna uma cadeia de caracteres XML que pode ser usada pelo par especificado para ingressar em um grupo com uma senha correspondente.                                                                                                       |
| [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)                                     | Exclui os dados locais e o certificado associados a um grupo par.                                                                                                                                         |
| [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus)                               | Recupera o status atual de um grupo.                                                                                                                                                                     |
| [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials)                 | Emite credenciais, incluindo um GMC, para uma identidade específica e, opcionalmente, retorna uma cadeia de caracteres XML de convite que o par convidado pode usar para ingressar em um grupo par.                                                  |
| [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)                                         | Permite que um par com um convite participe de um grupo de pares existente.                                                                                                                                             |
| [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)                                         | Abre um grupo par que um par criou ou ingressou.                                                                                                                                                        |
| [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation)                   | Retorna uma [**estrutura \_ PEER INVITATION \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) com os detalhes de um convite específico.                                                                                        |
| [**PeerGroupPasswordJoin**](/windows/desktop/api/P2P/nf-p2p-peergrouppasswordjoin)                         | Permite que um par com um convite e a senha correta participem de um grupo de pares protegido por senha.                                                                                                           |



 

## <a name="group-and-member-information-functions"></a>Funções de informações de grupo e membro



| Função                                                 | Descrição                                                                                                                        |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers)     | Cria uma enumeração de membros do grupo de pares disponíveis e as informações de associação associadas.                                  |
| [**PeerGroupGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupgetproperties) | Recupera informações sobre as propriedades de um grupo especificado.                                                                      |
| [**PeerGroupSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergroupsetproperties) | Define as propriedades atuais do grupo de pares. Na versão 1.0 dessa API, somente o criador do grupo par pode executar essa operação. |



 

## <a name="records-and-record-management-functions"></a>Funções de gerenciamento de registros e registros



| Função                                                 | Descrição                                                                          |
|----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGroupAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupaddrecord)         | Adiciona um novo registro ao grupo par, que é propagado para todos os pares participantes. |
| [**PeerGroupDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupdeleterecord)   | Exclui um registro de um grupo par. Somente o criador de um registro pode excluí-lo.      |
| [**PeerGroupEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupenumrecords)     | Cria uma enumeração de registros de grupo par.                                        |
| [**PeerGroupGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupgetrecord)         | Recupera um registro de grupo específico.                                                   |
| [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) | Pesquisa no banco de dados de grupo par local registros que corresponderem aos critérios fornecidos. |
| [**PeerGroupUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergroupupdaterecord)   | Atualiza um registro dentro de um grupo de pares específico.                                       |



 

## <a name="group-database-importexport-functions"></a>Funções de Importação/Exportação banco de dados de grupo



| Função                                                   | Descrição                                                                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase) | Exporta um banco de dados de grupo par para um arquivo específico, que pode ser transportado para outro computador e importado com a [**função PeerGroupImportDatabase.**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) |
| [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase) | Importa um banco de dados de grupo par de um arquivo local.                                                                                                                                          |



 

## <a name="direct-connection-functions"></a>Funções de conexão direta



| Função                                                                 | Descrição                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) | Fecha uma conexão direta específica entre dois pares.              |
| [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections)             | Cria uma enumeração de conexões atualmente ativas no par. |
| [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)   | Estabelece uma conexão direta com outro par em um grupo par.  |
| [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)                           | Envia dados a um membro por uma conexão direta ou de vizinho.        |



 

## <a name="group-events-infrastructure"></a>Infraestrutura de Eventos de Grupo



| Função                                                     | Descrição                                                                                    |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)       | Permite que um aplicativo recupere os dados retornados por um evento de agrupação.                       |
| [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)     | Registra um par para eventos de grupo de pares específicos.                                               |
| [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) | Desassocia um par da notificação de eventos de pares associados ao handle de evento fornecido. |



 

## <a name="group-time-conversion-functions"></a>Funções de conversão de tempo de grupo



| Função                                                                     | Descrição                                                                                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergrouppeertimetouniversaltime) | Converte o valor de tempo de referência mantido pelo grupo par em um valor de tempo localizado apropriado para exibição em um computador par. |
| [**PeerGroupUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergroupuniversaltimetopeertime) | Converte um valor de hora local do computador de um par em um valor de tempo de grupo par comum.                                         |



 

## <a name="group-configuration-functions"></a>Funções de configuração de grupo



| Função                                               | Descrição                                                                                                                       |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGroupExportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupexportconfig) | Exporta a configuração de grupo para um par como uma cadeia de caracteres XML que contém a identidade, o nome do grupo e o GMC para a identidade. |
| [**PeerGroupImportConfig**](/windows/desktop/api/P2P/nf-p2p-peergroupimportconfig) | Importa uma configuração de grupo par para uma identidade com base nas configurações específicas em uma cadeia de caracteres de configuração XML fornecida.         |



 

 

 



