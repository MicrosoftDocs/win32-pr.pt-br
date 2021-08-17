---
description: Windows Os soquetes 2 estendem a funcionalidade do Windows Sockets 1.1 em várias áreas. A tabela a seguir resume algumas das principais alterações de recurso.
ms.assetid: 26bfb614-5700-44d3-b4fb-1002d757d15e
title: Considerações sobre programação winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8451601f92f0fbf7b85532fc5a63479fe2bec26adc1984c74fc1cd7d750a04aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739855"
---
# <a name="winsock-programming-considerations"></a>Considerações sobre programação winsock

Windows Os soquetes 2 estendem a funcionalidade do Windows Sockets 1.1 em várias áreas. A tabela a seguir resume algumas das principais alterações de recurso.



| Recursos                                                                                                           | Descrição                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Arquitetura de soquetes 2](windows-sockets-2-architecture-2.md)                                             | Uma descrição da arquitetura Windows Sockets 2.                                                                                                                                                                                                                                           |
| [Alças de soquete](socket-handles-2.md)                                                                             | Opcionalmente, um alça de soquete pode ser um alça de arquivo Windows Soquetes 2. É possível usar os alças de soquete com funções Windows E/S de arquivo padrão.                                                                                                                                           |
| [Acesso simultâneo a vários protocolos de transporte](simultaneous-access-to-multiple-transport-protocols-2.md)   | Permite que um aplicativo use a interface de soquete familiar para obter acesso simultâneo a vários protocolos de transporte instalados.                                                                                                                                                        |
| [Resolução de nomes independentes de protocolo](protocol-independent-name-resolution-2.md)                                 | Inclui um conjunto padronizado de funções para consultar e trabalhar com os domínios de resolução de nomes diversos que existem hoje (por exemplo, DNS, SAP e X.500).                                                                                                                                  |
| [Multicast e multipoint independentes de protocolo](protocol-independent-multicast-and-multipoint-2.md)               | Os aplicativos descobrem que tipo de recursos multicast ou multicast um transporte fornece e usa essas instalações de maneira genérica.                                                                                                                                                     |
| [E/S sobressalvada](overlapped-i-o-and-event-objects-2.md)                                                           | Incorpora o paradigma sobre mapeado para E/S de soquete seguindo o modelo estabelecido Windows ambientes.                                                                                                                                                                                   |
| [E/S de dispersão/coleta](scatter-gather-i-o-2.md)                                                                     | Incorpora funcionalidades de dispersão/coleta com o paradigma sobre mapeado para E/S de soquete, seguindo o modelo estabelecido Windows ambientes.                                                                                                                                                 |
| [QoS](flow-specification-quality-of-service-2.md) (Qualidade de Serviço)                                            | Estabelece convenções que os aplicativos usam para negociar os níveis de serviço necessários para parâmetros como largura de banda e latência. Outros aprimoramentos relacionados a QoS incluem mecanismos para extensões de Qualidade de Serviço específicas de rede.                                                         |
| [Mecanismo de extensão específico do provedor](provider-specific-extension-mechanism-2.md)                               | A [**função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) permite que os provedores de serviços ofereçam extensões de recurso específicas do provedor.                                                                                                                                                                           |
| [Soquetes compartilhados](shared-sockets-2.md)                                                                             | A [**função WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) é introduzida para habilitar o compartilhamento de soquete entre processos.                                                                                                                                                                       |
| [Instalação e rebaixamento de conexão](connection-setup-and-teardown-2.md)                                               | Um aplicativo pode obter informações do chamador, como identificador de chamador e Qualidade de Serviço, antes de decidir se deve aceitar uma solicitação de conexão de entrada. Também é possível (para protocolos que suportam isso) trocar dados de usuário entre os pontos de extremidade no momento da redução da conexão. |
| [Desligamento normalmente, opções de persistente e fechamento de soquete](graceful-shutdown-linger-options-and-socket-closure-2.md) | Um aplicativo tem várias opções para desligar uma conexão de soquete (sequência de desligamento).                                                                                                                                                                                                  |
| [Dados fora de banda independentes de protocolo](protocol-independent-out-of-band-data-2.md)                               | A abstração de soquete de fluxo inclui a noção de dados OOB (fora de banda).                                                                                                                                                                                                                   |
| [Recursos de depuração e rastreamento](debug-and-trace-facilities-2.md)                                                     | Windows Os soquetes 2 são compatíveis com uma versão especialmente idealizada do Ws232.dll uma DLL separada \_ de depuração/rastreamento.                                                                                                                                                                                      |
| [Windows Problemas de compatibilidade de soquetes](windows-sockets-compatibility-issues-2.md)                                 | Windows Os soquetes 2 continuam a dar suporte a todas as chamadas de função e semântica do Windows Sockets 1.1, exceto aquelas que lidam com pseudo-bloqueio.                                                                                                                                              |
| [Tratamento de erros winsock](handling-winsock-errors.md)                                                             | Como os erros do Winsock podem ser recuperados e tratados por um aplicativo.                                                                                                                                                                                                                             |



 

 

 



