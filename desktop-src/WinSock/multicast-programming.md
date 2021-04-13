---
description: A programação multicast é habilitada por meio do Windows Sockets.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programação de multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67af0eeb087e8c6a5938f26a0644dc346d55cf51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501689"
---
# <a name="multicast-programming"></a>Programação de multicast

A programação multicast é habilitada por meio do Windows Sockets. O Windows Sockets permite a descoberta de ouvinte multicast (MLD) versões 1 (MLDv1) e 2 (MLDv2) no IPv6 e o protocolo de gerenciamento de grupo da Internet versões 2 (IGMPv2) e 3 (IGMPv3) por meio do uso de opções de soquete ou de IOCTLs. Esta seção descreve a implementação do Windows, explica como habilitar a programação de multicast usando o Windows Sockets e fornece exemplos de programação para ilustrar seu uso.

A segunda versão do IGMP, daqui em diante, chamada de IGMPv2, permite que os hosts ingressem e deixem grupos de multicast identificados por um endereço de multicast IPv4 em um adaptador de rede específico. O Windows Sockets permite que um aplicativo ingresse e deixe esses grupos em soquetes específicos. No entanto, uma desvantagem do IGMPv2 é que qualquer endereço de origem IPv4 ingressado no grupo IGMPv2 pode transmitir para todos os membros, potencialmente inundando o grupo e tornando-o inutilizável para transmissões que exigem uma fonte primária, como uma estação de rádio da Internet. O problema com o IGMPv2 é sua incapacidade de escolher seletivamente um único endereço de origem IPv4 (ou até mesmo algumas fontes) e sua incapacidade de bloquear remetentes (como difusores não autorizados ou criminosos de negação de serviço) para um determinado grupo de multicast. O IGMPv3 atende a essas deficiências.

Com o Windows Sockets e o IGMPv3, os aplicativos podem selecionar um determinado endereço de origem IPv4 e um par de grupos multicast. Além disso, o Windows Sockets permite aos desenvolvedores permitir seletivamente difusões adicionais em um determinado par de origem/grupo ou permite que os aplicativos bloqueiem difusores específicos. O IGMPv3 tem suporte no Windows Vista e posterior.

A primeira versão do MLD no IPv6, conhecida como MLDv1, é muito semelhante à IGMPv2 e sofre das mesmas limitações. O MLDv1 permite que os hosts ingressem e deixem grupos de multicast identificados por um endereço de multicast IPv6 em uma interface de rede específica. O Windows Sockets permite que um aplicativo ingresse e deixe esses grupos em soquetes específicos. No entanto, qualquer endereço de origem IPv6 ingressado no grupo MLDv1 pode transmitir para todos os membros, potencialmente inundando o grupo e tornando-o inutilizável para transmissões que exigem uma origem primária. O problema com o MLDv1 é sua incapacidade de escolher seletivamente um único endereço de origem IPv6 (ou até mesmo algumas fontes) e sua incapacidade de bloquear remetentes (como difusores não autorizados ou criminosos de negação de serviço) para um determinado grupo de multicast. O MLDv2 resolve essas deficiências.

Com o Windows Sockets e o MLDv2, os aplicativos podem selecionar um determinado endereço de origem IPv6 de multicast e um par de grupos multicast. Além disso, o Windows Sockets permite aos desenvolvedores permitir seletivamente difusões adicionais em um determinado par de origem/grupo ou permite que os aplicativos bloqueiem difusores específicos. O MLDv2 tem suporte no Windows Vista e versões posteriores.

Há duas abordagens que um programador de aplicativos pode tomar ao desenvolver aplicativos multicast no Windows. A primeira abordagem é baseada em alteração; as fontes multicast são adicionadas ou removidas usando opções de soquete, mesmo durante o curso de transmissão, conforme necessário. A segunda abordagem é baseada no estado final; os endereços de origem e todos os endereços incluídos/excluídos são especificados com um IOCTL. Cada abordagem é uma prática de multicast válida, mas os desenvolvedores podem encontrar o uso de opções de soquete e a abordagem baseada em alteração mais intuitiva e flexível.

Esta seção tem as seguintes páginas: 

| Título da página                                                                             | Descrição                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD e IGMP usando soquetes do Windows](igmp-and-windows-sockets.md)                     | Enumera as opções de soquete multicast disponíveis para uso na programação do Windows Sockets, usando uma abordagem de programação baseada em alteração. Define duas categorias de aplicativo multicast. |
| [Comportamento da opção de soquete multicast](multicast-socket-option-behavior.md)               | Fornece uma tabela abrangente para explicar as implicações e os requisitos de chamada de opções de soquete de multicast em ordem específica.                                                  |
| [Exemplo de programação multicast](multicast-programming-sample.md)                       | Trecho de programação que ilustra como usar opções de soquete para habilitar aplicativos multicast no Windows.                                                                        |
| [Programação de multicast com base no estado final](final-state-based-multicast-programming.md) | Explica a abordagem de estado final e como usar os IOCTLs para programação de multicast com o Windows Sockets.                                                                               |
| [Portando aplicativos de difusão para IPv6](porting-broadcast-applications-to-ipv6.md)   | Fornece diretrizes para portar aplicativos de difusão IPv4 para multicast IPv6.                                                                                                     |



 

 

 



