---
title: Sobre a NAP
description: Sobre a NAP
ms.assetid: c5dc4956-dcb7-4fcf-b4cc-2fac016427dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4227e1291945fa2d3b7876df27c2cc18cdfde2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635010"
---
# <a name="about-nap"></a>Sobre a NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A NAP (proteção de acesso à rede) foi criada para ajudar os administradores a manter a integridade dos computadores na rede, o que ajuda a manter a integridade geral da rede. Ele não foi projetado para proteger uma rede contra usuários mal-intencionados. Por exemplo, se um computador tiver todo o software e as configurações que a política de acesso à rede exigir, o computador será considerado Íntegro ou em conformidade, e ele receberá o acesso apropriado à rede. A NAP não impede que um usuário autorizado com um computador em conformidade carregue um programa mal-intencionado na rede ou esteja participando de outro comportamento inadequado.

Para proteger o acesso a uma rede, uma infraestrutura de rede precisa fornecer as seguintes áreas de funcionalidade:

-   Validação de integridade: determina se os computadores estão em conformidade com os requisitos de integridade do sistema.
-   Restrição de rede: restringe o acesso à rede ou à comunicação para clientes que não estão em conformidade com os requisitos de integridade do sistema.
-   Correção: fornece as atualizações necessárias para permitir que o computador corrija seu estado de integridade não compatível.
-   Conformidade contínua: permite o acesso à rede, desde que o computador do usuário atenda aos requisitos da política de integridade.

O Windows XP com Service Pack 3 (SP3), o Windows Vista e o Windows Server 2008 fornecem métodos de imposição de NAP para a configuração de endereço DHCP, conexões de rede virtual privada (VPN) baseadas em acesso remoto, conexões com e sem fio com base no IEEE 802.1 X e comunicações baseadas em IPsec (Internet Protocol Security). Além disso, a plataforma NAP dá suporte a uma arquitetura por meio da qual a validação de integridade, a restrição de rede, a correção e a conformidade contínua têm suporte de componentes adicionais que podem ser fornecidos por fornecedores de software de terceiros ou pela Microsoft.

A plataforma NAP inclui os seguintes componentes:

-   [Arquitetura de cliente NAP](nap-client-architecture.md)
-   [Arquitetura do lado do servidor NAP](nap-server-side-architecture.md)
-   [Comunicação do cliente NAP e do componente do lado do servidor](nap-client-and-server-side-component-communication.md)

O cliente NAP requer o Windows Vista, o Windows XP com SP3 ou o Windows Server 2008. O servidor de diretiva de integridade NAP e os pontos de imposição de NAP para imposição de DHCP, VPN e IPsec exigem o Windows Server 2008.

 

 




