---
description: A tabela a seguir lista objetos COM e interfaces associados aos controles de conferência de reunião.
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: Interfaces COM de reunião
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6df7fbdac45480ae7aa9d5968209f22fabe9a4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784081"
---
# <a name="rendezvous-com-interfaces"></a>Interfaces COM de reunião

\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A tabela a seguir lista objetos COM e interfaces associados aos controles de conferência de reunião.

Para obter informações adicionais sobre o COM (Component Object Model), consulte as seções relevantes no SDK (Software Development Kit) da plataforma.



| Interfaces                                                         | Descrição                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IEnumDialableAddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | Enumera os endereços de discagem disponíveis no diretório atual.                                                     |
| [**IEnumDirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | Enumera objetos [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) .                                                                    |
| [**IEnumDirectoryObject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | Enumera objetos [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) .                                                        |
| [**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | Enumera objetos [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope) .                                                                    |
| [**IEnumMedia**](ienummedia.md)                                   | Enumera objetos [**ITMedia**](itmedia.md) .                                                                            |
| [**IEnumTime**](ienumtime.md)                                     | Enumera objetos [**ITTime**](ittime.md) .                                                                              |
| [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | Interface principal para wrapper COM de alocação de endereço multicast.                                                           |
| [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | Fornece métodos para recuperar e definir informações de concessão de endereço.                                                           |
| [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | Encapsula todas as propriedades de um escopo de multicast e fornece métodos para obter informações sobre o escopo.             |
| [**ITAttributeList**](itattributelist.md)                         | Permite obter e definir atributos não interpretados.                                                                   |
| [**ITConferenceBlob**](itconferenceblob.md)                       | Fornece acesso a informações de conferência específicas do provedor.                                                              |
| [**ITConnection**](itconnection.md)                               | Fornece métodos para manipular fatores de conexão, como endereço de conferência, escopo e largura de banda.                       |
| [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | Obtém e define informações de diretório e fornece acesso a um objeto de diretório específico.                                |
| [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | Obtém e define informações genéricas para uma conferência ou um usuário em um diretório.                                            |
| [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | Obtém e define informações genéricas específicas para uma conferência, como horários de início e de parada.                                 |
| [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | Obtém e define informações genéricas específicas para um usuário, como o nome de um computador que é o telefone IP primário do usuário. |
| [**ITILSConfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | Obtém e define informações específicas para o servidor de um determinado diretório do ILS.                                                |
| [**ITMedia**](itmedia.md)                                         | Obtém e define as propriedades básicas de mídia, como o nome da mídia e o protocolo de transporte.                                       |
| [**ITMediaCollection**](itmediacollection.md)                     | Permite o acesso à mídia por índice. Habilita a criação e a exclusão de mídia.                                                     |
| [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | Interface principal para o controle de reunião.                                                                                |
| [**ITSdp**](itsdp.md)                                             | Manipula o blob de SDP (protocolo de descrição de sessão). Referência: RFC 2327.                                             |
| [**ITTime**](ittime.md)                                           | Fornece acesso a um conjunto de tempos de ativação para a sessão.                                                             |
| [**ITTimeCollection**](ittimecollection.md)                       | Permite o acesso ao componente de tempo por índice. Permite a criação e a exclusão de componentes de tempo.                                  |



 

 

 



