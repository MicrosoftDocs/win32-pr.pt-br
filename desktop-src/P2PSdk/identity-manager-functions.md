---
description: A API do Gerenciador de identidade do par usa as funções a seguir.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Funções do Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea56df6500239141038f76ba312b84148581f8f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753729"
---
# <a name="identity-manager-functions"></a>Funções do Identity Manager

A API do Gerenciador de identidade do par usa as funções a seguir.



| Função                                                           | Descrição                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Cria um novo nome com base no nome existente da identidade e do classificador de mesmo nível especificados. No entanto, uma nova identidade não é criada por uma chamada para [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Cria e retorna um identificador de enumeração de pares usado para enumerar todos os grupos de pares associados a uma identidade de par específica.                                                                                                                                                                          |
| [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Cria e retorna um identificador de enumeração de pares usado para enumerar todas as identidades de pares que pertencem a um usuário específico.                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Libera uma enumeração, por exemplo, uma enumeração de registro ou membro, e desaloca todos os recursos associados à enumeração.                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Desaloca um bloco de dados e o retorna ao pool de memória.                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Retorna uma contagem dos itens em uma enumeração de pares.                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Retorna um número específico de itens de uma enumeração de pares.                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Cria uma nova identidade de par e retorna seu nome. O nome da identidade do par deve ser passado em todas as chamadas subsequentes para o Gerenciador de identidade do par, o agrupamento de pares ou as funções do PNRP que operam em nome da identidade do par. O nome de identidade do par especifica qual identidade do par está sendo usada. |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Exclui uma identidade de par. Isso inclui remover todos os certificados, chaves privadas e todas as informações de grupo associadas a uma identidade de par especificada.                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Permite que um usuário exporte uma identidade de par. Em seguida, o usuário pode transferir a identidade do par para um computador diferente.                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Recupera um identificador para um CSP (provedor de serviços de criptografia).                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Recupera o nome de par padrão definido para o usuário atual.                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Retorna o nome amigável da identidade do par.                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Retorna uma descrição da identidade do par, que pode ser passada para terceiros e usada para convidar uma identidade de mesmo nível em um grupo de pares. Essas informações são retornadas como um fragmento XML.                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importa uma identidade de par. Se a identidade do par existir em um computador, o **par \_ E \_ já \_ existir** será retornado.                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Modifica o nome amigável de uma identidade de par especificada. O nome amigável é o nome legível.                                                                                                                                                                                                |



 

 

 



