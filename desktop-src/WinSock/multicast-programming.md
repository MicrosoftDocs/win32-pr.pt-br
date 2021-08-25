---
description: A programação multicast é habilitada por meio Windows Sockets.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programação multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0582f9d03cd5614bbe284eb81cdcb40bea8233627564ec2d3603de11fb663e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858156"
---
# <a name="multicast-programming"></a>Programação multicast

A programação multicast é habilitada por meio Windows Sockets. Windows Os soquetes habilitam as versões 1 (MLDv1) e 2 (MLDv2) do Multicast Listener Discovery (MLD) no IPv6 e nas versões 2 (IGMPv2) e 3 (IGMPv3) da Internet por meio do uso de opções de soquete ou IOCTLs. Esta seção descreve a implementação Windows, explica como habilitar a programação multicast usando soquetes Windows e fornece exemplos de programação para ilustrar seu uso.

A segunda versão do IGMP, conhecida como IGMPv2, permite que os hosts inscrevam e deixam grupos multicast identificados por um endereço multicast IPv4 em um interface de rede específico. Windows Soquetes permitem que um aplicativo in join e deixe esses grupos em soquetes específicos. No entanto, uma desvantagem de IGMPv2 é que qualquer endereço de origem IPv4 associado ao grupo IGMPv2 pode transmitir para todos os membros, potencialmente inundando o grupo e tornando-o inutilizável para transmissões que exigem uma fonte primária, como uma estação de rádio da Internet. O problema com IGMPv2 é sua incapacidade de escolher seletivamente um único endereço de origem IPv4 (ou até mesmo algumas fontes) e sua incapacidade de bloquear remetentes (como difusões não confiáveis ou ataques de negação de serviço) para um determinado grupo multicast. IGMPv3 resolve essas deficiências.

Com Windows Soquetes e IGMPv3, os aplicativos podem selecionar um endereço de origem IPv4 multicast específico e um par de grupos multicast. Além disso, Windows Soquetes permite que os desenvolvedores permitam seletivamente difusões adicionais em um determinado par de origem/grupo ou permite que os aplicativos bloqueiem difusões específicas. Há suporte para IGMPv3 no Windows Vista e posterior.

A primeira versão do MLD no IPv6, conhecida como MLDv1, é muito semelhante ao IGMPv2 e tem as mesmas limitações. O MLDv1 permite que os hosts inserem e deixam grupos multicast identificados por um endereço multicast IPv6 em um interface de rede específico. Windows Soquetes permitem que um aplicativo in join e deixe esses grupos em soquetes específicos. No entanto, qualquer endereço de origem IPv6 ingressado no grupo MLDv1 pode transmitir para todos os membros, potencialmente inundando o grupo e tornando-o inutilizável para transmissões que exigem uma fonte primária. O problema com MLDv1 é sua incapacidade de escolher seletivamente um único endereço de origem IPv6 (ou até mesmo algumas fontes) e sua incapacidade de bloquear remetentes (como difusões não confiáveis ou ataques de negação de serviço) para um determinado grupo multicast. O MLDv2 resolve essas deficiências.

Com Windows Sockets e MLDv2, os aplicativos podem selecionar um endereço de origem IPv6 multicast específico e um par de grupos multicast. Além disso, Windows Soquetes permite que os desenvolvedores permitam seletivamente difusões adicionais em um determinado par de origem/grupo ou permite que os aplicativos bloqueiem difusões específicas. O MLDv2 tem suporte no Windows Vista e posterior.

Há duas abordagens que um programador de aplicativos pode usar ao desenvolver aplicativos multicast Windows. A primeira abordagem é baseada em alterações; As fontes multicast são adicionadas ou removidas usando opções de soquete, mesmo durante o curso da transmissão, conforme necessário. A segunda abordagem é baseada em estado final; endereços de origem e quaisquer endereços incluídos/excluídos são especificados com um IOCTL. Cada abordagem é uma prática de multicast válida, mas os desenvolvedores podem achar o uso de opções de soquete e a abordagem baseada em alterações mais intuitiva e flexível.

Esta seção tem as seguintes páginas: 

| Título da página                                                                             | Descrição                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD e IGMP usando Windows soquetes](igmp-and-windows-sockets.md)                     | Enumera as opções de soquete multicast disponíveis para uso na programação Windows Sockets, usando uma abordagem de programação baseada em alterações. Define duas categorias de aplicativo multicast. |
| [Comportamento da opção De soquete multicast](multicast-socket-option-behavior.md)               | Fornece uma tabela extensiva para explicar as implicações e os requisitos de chamada de opções de soquete multicast em ordem específica.                                                  |
| [Exemplo de programação multicast](multicast-programming-sample.md)                       | Snippet de programação que ilustra como usar opções de soquete para habilitar aplicativos multicast Windows.                                                                        |
| [Programação multicast baseada em estado final](final-state-based-multicast-programming.md) | Explica a abordagem de estado final e como usar IOCTLs para programação multicast com Windows Sockets.                                                                               |
| [Portando aplicativos de difusão para IPv6](porting-broadcast-applications-to-ipv6.md)   | Fornece diretrizes para portar aplicativos de difusão IPv4 para multicast IPv6.                                                                                                     |



 

 

 



