---
title: Arquitetura de cliente NAP
description: Um cliente NAP é um computador que executa o Windows XP com Service Pack 3 (SP3), o Windows Vista ou o Windows Server 2008 que inclui a plataforma NAP.
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15862eaa6ae4f4c1f79c53cf9d540aedec295e8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292664"
---
# <a name="nap-client-architecture"></a>Arquitetura de cliente NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

Um cliente NAP é um computador que executa o Windows XP com Service Pack 3 (SP3), o Windows Vista ou o Windows Server 2008 que inclui a plataforma NAP.

Esta figura mostra a arquitetura da plataforma NAP em um cliente NAP.

![arquitetura da plataforma NAP em um cliente NAP](images/nap-client-side-arch.png)

A arquitetura de cliente NAP consiste no seguinte:

-   Uma camada de componentes de cliente de imposição (EC)

    Cada NAP EC é definida para um tipo diferente de acesso à rede. Por exemplo, há um NAP EC para a configuração do DHCP e um NAP EC para conexões VPN de acesso remoto. O NAP EC pode ser correspondido a um tipo específico de ponto de imposição de NAP. Por exemplo, o NAP EC DHCP foi projetado para funcionar com um ponto de imposição de NAP baseado em DHCP. Alguns ECs de NAP são fornecidos com a plataforma NAP e fornecedores de software de terceiros, ou a Microsoft pode fornecer outros.

-   Uma camada de componentes do agente de integridade do sistema (SHA)

    Um componente SHA mantém e relata um ou vários elementos da integridade do sistema. Por exemplo, pode haver um SHA para assinaturas de antivírus e um SHA para atualizações do sistema operacional. Um SHA pode corresponder a um servidor de atualizações, que é um computador que contém recursos de atualização de integridade que os clientes NAP podem acessar para corrigir seu estado não compatível. Por exemplo, um SHA para verificar assinaturas de antivírus é compatível com o servidor que contém o arquivo de assinatura antivírus mais recente. Os SHAs não precisam ter um servidor de correção correspondente. Por exemplo, um SHA pode apenas verificar as configurações do sistema local para garantir que um firewall baseado em host esteja habilitado. O Windows Vista e o Windows XP Service Pack 3 incluem o Agente de Integridade da Segurança do Windows (WSHA) que monitora as configurações da central de segurança do Windows. Fornecedores de software de terceiros ou a Microsoft podem fornecer SHAs adicionais para a plataforma NAP.

-   Agente NAP

    Mantém as informações de estado de integridade atuais do cliente NAP e facilita a comunicação entre as camadas NAP EC e SHA. O agente NAP é fornecido com a plataforma NAP.

-   API do agente de integridade do sistema

    Fornece um conjunto de funções que permitem que os SHAs se registrem com o agente NAP, para indicar o status de integridade do sistema, responder a consultas de status de integridade do sistema do agente NAP e para que o agente NAP passe informações de atualização da integridade do sistema para um SHA. A API do SHA permite que os fornecedores criem e instalem SHAs adicionais. A API do SHA é fornecida com a plataforma NAP. Consulte as seguintes interfaces NAP: [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md), [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)e [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md).

Para indicar o estado de integridade de um SHA específico, um SHA cria uma [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh)(declaração de integridade) e a passa para o agente NAP. Uma SoH pode conter um ou vários elementos da integridade do sistema. Por exemplo, o SHA para um programa antivírus pode criar uma SoH contendo o estado do software antivírus em execução no computador, sua versão e a última atualização de assinatura de antivírus recebida. Sempre que um SHA atualiza seu status, ele cria uma nova SoH e a passa para o agente NAP. Para indicar o estado de integridade geral de um cliente NAP, o agente NAP usa uma SSoH (declaração de integridade do sistema), que inclui informações de versão para o cliente NAP e o conjunto de SoHs para os SHAs instalados.

As seções a seguir descrevem os componentes da arquitetura do cliente NAP mais detalhadamente.

## <a name="nap-enforcement-client"></a>Cliente de imposição de NAP

Um cliente de imposição de NAP (EC) solicita algum nível de acesso a uma rede, passa o status de integridade do computador para um ponto de imposição de NAP que está fornecendo o acesso à rede. Os pontos de imposição de NAP são computadores ou dispositivos de acesso à rede que usam NAP ou podem ser usados com a NAP para exigir a avaliação do estado de integridade de um cliente NAP e fornecer acesso restrito à rede ou comunicação. Se a integridade do computador não for compatível, o NAP EC indicará o status restrito do cliente NAP para outros componentes da arquitetura do cliente NAP.

O ECs do NAP para a plataforma NAP fornecido no Windows XP com SP3, Windows Vista e Windows Server 2008 são os seguintes:

-   Um NAP EC IPsec para comunicações protegidas por IPsec.
-   Um NAP EC EAPHost para conexões autenticadas por 802.1 X.
-   Um NAP EC VPN para conexões VPN de acesso remoto.
-   Um NAP EC DHCP para configuração de endereço IPv4 baseado em DHCP.
-   Um Gateway TS NAP EC para conexões de Gateway TS.

Para o Windows XP com SP3, há um ECs NAP separado para conexões com e sem fio autenticadas por 802.1 X.

### <a name="ipsec-nap-ec"></a>NAP EC IPsec

O IPsec NAP EC é um componente que obtém o SSoH do agente NAP e o envia para uma HRA (autoridade de registro de integridade), um computador executando o Windows Server 2008 e o Serviços de Informações da Internet (IIS) que obtém certificados de integridade de uma autoridade de certificação (CA) para computadores compatíveis. O IPsec NAP EC é conhecido como o EC da parte confiável do IPsec no snap-in de configuração do cliente NAP. O IPsec NAP EC também interage com o seguinte:

-   O repositório de certificados para armazenar o certificado de integridade.
-   Os componentes IPsec no Windows para garantir que o certificado de integridade seja usado para comunicação protegida por IPsec.
-   O firewall baseado em host (como o Firewall do Windows) para que o tráfego protegido por IPsec seja permitido pelo firewall.

### <a name="eaphost-nap-ec"></a>EAPHost NAP EC

O NAP EC EAPHost é um componente que obtém o SSoH do agente NAP e o envia como uma mensagem de TLV (tipo de tamanho de PEAP) para conexões autenticadas com 802.1 X. O NAP EC do EAPHost é conhecido como o EC de quarentena do EAP no snap-in de configuração do cliente NAP.

### <a name="vpn-nap-ec"></a>NAP EC VPN

A NAP EC VPN é uma funcionalidade no serviço Gerenciador de conexões de acesso remoto que obtém o SSoH do agente NAP e o envia como uma mensagem PEAP-TLV para conexões VPN de acesso remoto. O NAP EC VPN é conhecido como o EC de quarentena de acesso remoto no snap-in de configuração do cliente NAP.

### <a name="dhcp-nap-ec"></a>NAP EC DHCP

O NAP EC DHCP é uma funcionalidade no serviço de cliente DHCP que usa mensagens DHCP padrão do setor para trocar mensagens de integridade do sistema e informações de acesso limitado à rede. O IPsec DHCP EC é conhecido como o EC de quarentena do DHCP no snap-in de configuração do cliente NAP. O NAP EC DHCP Obtém o SSoH do agente NAP. O serviço cliente DHCP fragmenta o SSoH, se necessário, e coloca cada fragmento em uma opção DHCP específica do fornecedor da Microsoft que é enviada em mensagens DHCPDiscover, DHCPRequest ou DHCPInform. As mensagens DHCPDecline e DHCPRelease não contêm o SSoH.

## <a name="system-health-agent"></a>Agente de integridade do sistema

Um SHA (agente de integridade do sistema) executa atualizações de integridade do sistema e publica seu status na forma de uma SoH para o agente NAP. A SoH contém informações que o servidor de diretiva de integridade de NAP pode usar para verificar se o computador cliente está no estado de integridade necessário. Um SHA é correspondido a um SHV (validador de integridade do sistema) no lado do servidor da arquitetura da plataforma NAP. O SHV correspondente pode retornar uma resposta SoH (SoHR) para o cliente NAP, que é passado pelo NAP EC e o agente NAP para o SHA, informando o que fazer se o SHA não estiver em um estado de integridade necessário. Por exemplo, o SoHR enviado por um SHV de antivírus pode instruir o SHA do antivírus correspondente a consultar um servidor de assinatura de antivírus para obter a versão mais recente do arquivo de assinatura de antivírus. O SoHR também pode incluir o nome ou endereço IP do servidor de assinatura antivírus para consultar.

Um SHA pode usar um cliente de política instalado localmente para auxiliar nas funções de gerenciamento de integridade do sistema em conjunto com um servidor de políticas. Por exemplo, um SHA de atualização de software pode usar o software cliente de software instalado localmente (o cliente de política) para executar a verificação de versão e as funções de instalação e atualização com o servidor de atualização de software (o servidor de política).

## <a name="nap-agent"></a>Agente NAP

O agente NAP fornece os seguintes serviços:

-   Coleta o SoHs de cada SHA e os armazena em cache. O cache SoH é atualizado sempre que um SHA fornece uma SoH nova ou atualizada.
-   Armazena o SSoH e o fornece ao ECs de NAP mediante solicitação.
-   Passa notificações para SHAs quando o estado restrito é alterado.
-   Mantém o estado restrito do sistema e coleta informações de status de cada SHA.
-   Passa SoHRs para o SHA apropriado.

 

 




