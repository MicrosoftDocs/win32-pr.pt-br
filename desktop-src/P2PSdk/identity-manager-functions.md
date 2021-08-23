---
description: A API do Peer Identity Manager usa as funções a seguir.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Funções do Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a640aa7250cdf34fed7440d955a8de8ac7ac1a58316bef3f6e97b3564ac7fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518566"
---
# <a name="identity-manager-functions"></a>Funções do Identity Manager

A API do Peer Identity Manager usa as funções a seguir.



| Função                                                           | Descrição                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Cria um novo nome com base no nome existente da identidade e do classificador de pares especificados. No entanto, uma nova identidade não é criada por uma chamada para [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Cria e retorna um alça de enumeração par usado para enumerar todos os grupos de pares associados a uma identidade de par específica.                                                                                                                                                                          |
| [**Entidades PeerEnumId**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Cria e retorna um alça de enumeração de par usado para enumerar todas as identidades de par que pertencem a um usuário específico.                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Libera uma enumeração, por exemplo, um registro ou enumeração de membro e desaloca todos os recursos associados à enumeração.                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Desaloca um bloco de dados e o retorna para o pool de memória.                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Retorna uma contagem dos itens em uma enumeração par.                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Retorna um número específico de itens de uma enumeração par.                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Cria uma nova identidade de par e retorna seu nome. O nome da identidade de par deve ser passado em todas as chamadas subsequentes para as funções Peer Identity Manager, Peer Grouping ou PNRP que operam em nome da identidade de par. O nome da identidade de par especifica qual identidade de par está sendo usada. |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Exclui uma identidade de par. Isso inclui a remoção de todos os certificados, chaves privadas e todas as informações de grupo associadas a uma identidade de par especificada.                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Permite que um usuário exporte uma identidade de par. Em seguida, o usuário pode transferir a identidade par para um computador diferente.                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Recupera um handle para um CSP (provedor de serviços de criptografia).                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Recupera o nome de par padrão definido para o usuário atual.                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Retorna o nome amigável da identidade do par.                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Retorna uma descrição da identidade de par, que pode ser passada para terceiros e usada para convidar uma identidade de par em um grupo par. Essas informações são retornadas como um fragmento XML.                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importa uma identidade de par. Se a identidade de par existir em um computador, **PEER \_ E ALREADY \_ \_ EXISTS** será retornado.                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Modifica o nome amigável de uma identidade de par especificada. O nome amigável é o nome acessível por humanos.                                                                                                                                                                                                |



 

 

 



