---
description: O Windows Sockets 2 estende a funcionalidade do Windows Sockets 1,1 em várias áreas. A tabela a seguir resume algumas das principais alterações de recursos.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Considerações sobre programação do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaee2cd04f03afe050ca539190b51e66c0abff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090997"
---
# <a name="winsock-programming-considerations"></a>Considerações sobre programação do Winsock

O Windows Sockets 2 estende a funcionalidade do Windows Sockets 1,1 em várias áreas. A tabela a seguir resume algumas das principais alterações de recursos.



| Recursos                                                                                                           | Descrição                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Arquitetura do Windows Sockets 2](windows-sockets-2-architecture-2.md)                                             | Uma descrição da arquitetura do Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Identificadores de soquete](socket-handles-2.md)                                                                             | Um identificador de soquete pode, opcionalmente, ser um identificador de arquivo no Windows Sockets 2. É possível usar identificadores de soquete com funções padrão de e/s de arquivo do Windows.                                                                                                                                           |
| [Acesso simultâneo a vários protocolos de transporte](simultaneous-access-to-multiple-transport-protocols-2.md)   | Permite que um aplicativo use a interface de soquete familiar para obter acesso simultâneo a vários protocolos de transporte instalados.                                                                                                                                                        |
| [Resolução de nomes independente de protocolo](protocol-independent-name-resolution-2.md)                                 | Inclui um conjunto padronizado de funções para consultar e trabalhar com inúmeros domínios de resolução de nomes que existem hoje (por exemplo, DNS, SAP e X. 500).                                                                                                                                  |
| [Multicast independente de protocolo e MultiPoint](protocol-independent-multicast-and-multipoint-2.md)               | Os aplicativos detectam o tipo de recursos de transmissão múltipla ou de MultiPoint que um transporte fornece e usam essas instalações de maneira genérica.                                                                                                                                                     |
| [E/s sobreposta](overlapped-i-o-and-event-objects-2.md)                                                           | Incorpora o paradigma sobreposto para a e/s de soquete após o modelo estabelecido em ambientes Windows.                                                                                                                                                                                   |
| [Dispersão/coleta de e/s](scatter-gather-i-o-2.md)                                                                     | Incorpora recursos de dispersão/coleta com o paradigma sobreposto para e/s de soquete, seguindo o modelo estabelecido em ambientes Windows.                                                                                                                                                 |
| QoS ( [qualidade de serviço](flow-specification-quality-of-service-2.md) )                                            | Estabelece convenções que os aplicativos usam para negociar os níveis de serviço necessários para parâmetros como largura de banda e latência. Outros aprimoramentos relacionados a QoS incluem mecanismos para a qualidade de extensões de serviço específica da rede.                                                         |
| [Mecanismo de extensão específico do provedor](provider-specific-extension-mechanism-2.md)                               | A função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite que os provedores de serviços ofereçam extensões de recurso específicas do provedor.                                                                                                                                                                           |
| [Soquetes compartilhados](shared-sockets-2.md)                                                                             | A função [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) é introduzida para habilitar o compartilhamento de soquete entre processos.                                                                                                                                                                       |
| [Configuração e desmontagem da conexão](connection-setup-and-teardown-2.md)                                               | Um aplicativo pode obter informações do chamador, como o identificador do chamador e a qualidade do serviço antes de decidir se deve aceitar uma solicitação de conexão de entrada. Também é possível (para protocolos que dão suporte a isso) para trocar dados de usuário entre os pontos de extremidade no momento da desmontagem da conexão. |
| [Desligamento normal, opções persistentes e fechamento de soquete](graceful-shutdown-linger-options-and-socket-closure-2.md) | Um aplicativo tem várias opções para desligar uma conexão de soquete (sequência de desligamento).                                                                                                                                                                                                  |
| [Dados fora de banda independentes de protocolo](protocol-independent-out-of-band-data-2.md)                               | A abstração de soquete de fluxo inclui a noção de dados de fora de banda (OOB).                                                                                                                                                                                                                   |
| [Recursos de depuração e rastreamento](debug-and-trace-facilities-2.md)                                                     | O Windows Sockets 2 dá suporte a uma versão especialmente elaborada do \_32.dll Ws2 e uma DLL de depuração/rastreamento separada.                                                                                                                                                                                      |
| [Problemas de compatibilidade do Windows Sockets](windows-sockets-compatibility-issues-2.md)                                 | O Windows Sockets 2 continua a dar suporte a todas as semânticas e chamadas de função do Windows Sockets 1,1, exceto aquelas que lidam com o pseudo-bloqueio.                                                                                                                                              |
| [Manipulando erros do Winsock](handling-winsock-errors.md)                                                             | Como erros de Winsock podem ser recuperados e manipulados por um aplicativo.                                                                                                                                                                                                                             |



 

 

 



