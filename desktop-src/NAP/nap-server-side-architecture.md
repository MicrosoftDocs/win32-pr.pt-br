---
title: Arquitetura do lado do servidor NAP
description: Arquitetura do lado do servidor NAP
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104084371"
---
# <a name="nap-server-side-architecture"></a>Arquitetura do lado do servidor NAP

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A arquitetura da plataforma do lado do servidor NAP usa computadores que executam o Windows Server 2008. A figura a seguir mostra a arquitetura do suporte do lado do servidor para a plataforma NAP, que consiste em pontos de imposição de NAP baseados no Windows e em um servidor de diretiva de integridade de NAP.

![arquitetura do suporte do lado do servidor para a plataforma NAP](images/nap-server-side-arch.png)

Um ponto de imposição de NAP baseado no Windows tem uma camada de componentes de servidor (ES) de imposição NAP. Cada NAP ES é definida para um tipo diferente de acesso à rede ou comunicação. Por exemplo, há um NAP ES para conexões VPN de acesso remoto e um NAP ES para a configuração de DHCP. O NAP ES normalmente é correspondido a um tipo específico de cliente compatível com NAP. Por exemplo, o NAP ES DHCP foi projetado para funcionar com um cliente de imposição NAP baseado em DHCP (EC). Fornecedores de software de terceiros ou a Microsoft podem fornecer NAP ESs adicional para a plataforma NAP. Uma NAP ES Obtém a SSoH (declaração de integridade do sistema) de seu NAP EC correspondente e a envia para um servidor de diretiva de integridade de NAP como um VSA (atributo específico do fornecedor) do RADIUS (serviço de usuário de discagem de autenticação remota) da [mensagem de Access-Request do RADIUS](https://www.ietf.org/rfc/rfc2865.txt?number=2865)

Como mostrado na figura da arquitetura do lado do servidor, o servidor de diretiva de integridade NAP tem os seguintes componentes:

-   Serviço de servidor de políticas de rede (NPS)

    Recebe a mensagem de Access-Request RADIUS, extrai o SSoH e o passa para o componente de servidor de administração NAP. O serviço NPS é fornecido com o Windows Server 2008.

-   Servidor de administração NAP

    Facilita a comunicação entre o serviço NPS e os SHVs (validadores da integridade do sistema). O componente de servidor de administração NAP é fornecido com a plataforma NAP.

-   Uma camada de componentes SHV

    Cada SHV é definido para um ou vários tipos de informações de integridade do sistema e pode ser correspondido a um SHA. Por exemplo, pode haver um SHV para um programa antivírus. Um SHV pode ser correspondido a um ou vários servidores de requisitos de integridade. Por exemplo, um SHV para verificar assinaturas de antivírus é compatível com o servidor que contém o arquivo de assinatura mais recente. Os SHVs não precisam ter um servidor de requisitos de integridade correspondente. Um SHV pode apenas instruir os clientes compatíveis com NAP a verificar as configurações do sistema local para garantir que um firewall baseado em host esteja habilitado. O Windows Server 2008 inclui o Validador da Integridade da Segurança do Windows (WSHV). Os SHVs adicionais são fornecidos por fornecedores de software de terceiros ou pela Microsoft como Complementos para a plataforma NAP.

-   API SHV

    Fornece um conjunto de chamadas de função que permitem que os SHVs se registrem com o componente de servidor de administração NAP, SoHs (instruções de recebimento de integridade) do componente de servidor de administração NAP e enviem SoHRs (declaração de resposta de integridade) para o componente de servidor de administração NAP. A API SHV é fornecida com a plataforma NAP. Consulte as seguintes interfaces NAP: [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) e [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).

Conforme descrito anteriormente, a configuração mais comum para a infraestrutura do lado do servidor NAP consiste em pontos de imposição de NAP que fornecem acesso à rede ou comunicação de um tipo específico e servidores de política de integridade de NPS separados que fornecem validação e correção da integridade do sistema. É possível instalar o serviço NPS como um servidor de diretiva de integridade de NAP em pontos de imposição de NAP baseados em Windows individuais. No entanto, nessa configuração, cada ponto de imposição de NAP deve ser configurado separadamente com as políticas de integridade e acesso à rede. A configuração recomendada é usar servidores de diretiva de integridade NAP separados.

A arquitetura NAP geral consiste nos seguintes conjuntos de componentes:

-   Os três componentes de cliente NAP (uma camada SHA, o agente NAP e uma NAP EC camada).
-   Os quatro componentes NAP do lado do servidor (uma camada SHV, o servidor de administração NAP, o serviço NPS e uma camada de NAP ES em pontos de imposição de NAP baseados no Windows).
-   Os servidores de requisitos de integridade, que são computadores que podem fornecer os requisitos atuais de integridade do sistema para servidor de política de integridade de NAP.
-   Servidores de atualizações, que são computadores que contêm recursos de atualização de integridade que os clientes NAP podem acessar para corrigir seu estado não compatível.

A figura a seguir mostra as relações entre os componentes da plataforma NAP.

![relações entre os componentes da plataforma NAP](images/nap-components.png)

Observe a correspondência dos seguintes conjuntos de componentes:

-   O NAP ECs e o NAP ESs normalmente são correspondentes.

    Por exemplo, o NAP EC DHCP no cliente NAP é correspondido ao NAP ES DHCP no servidor DHCP.

-   Os servidores de correção e SHA podem ser correspondidos.

    Por exemplo, um SHA de antivírus no cliente é correspondido a um servidor de atualização de assinatura de antivírus.

-   Os SHVs e os servidores de requisitos de integridade podem ser correspondidos.

    Por exemplo, um SHV de antivírus no servidor de diretiva de integridade de NAP pode ser correspondido a um servidor de requisito de integridade do antivírus.

Fornecedores de software de terceiros podem estender a plataforma NAP das seguintes maneiras:

-   Crie um novo método pelo qual a integridade de um cliente NAP é avaliada.

    Fornecedores de software de terceiros devem criar um SHA para o cliente NAP, um SHV para o servidor de diretiva de integridade de NAP e, se necessário, os requisitos de integridade e servidores de atualização. Se o requisito de integridade ou os servidores de atualização já existirem, como um servidor de distribuição de assinatura de antivírus, somente os componentes SHA e SHV correspondentes precisarão ser criados. Em alguns casos, os requisitos de integridade ou os servidores de atualização não são necessários.

-   Crie um novo método para impor os requisitos de integridade para acesso à rede ou comunicação.

    Fornecedores de software de terceiros devem criar um NAP EC no cliente NAP. Se o método de imposição usa um serviço baseado no Windows, fornecedores de software de terceiros devem criar um NAP ES correspondente que se comunica com um servidor de diretiva de integridade de NAP usando o protocolo RADIUS ou usando o serviço NPS instalado no ponto de imposição de NAP como um proxy RADIUS.

As seções a seguir descrevem os componentes da arquitetura do lado do servidor NAP com mais detalhes.

## <a name="nap-enforcement-server"></a>Servidor de imposição de NAP

Um servidor de imposição de NAP permite algum nível de acesso à rede ou comunicação, pode passar o status de integridade de um cliente NAP para o servidor de diretiva de integridade de rede para avaliação e, com base na resposta, pode fornecer a imposição de acesso limitado à rede.

O ESs do NAP incluído no Windows Server 2008 é o seguinte:

-   Um NAP ES IPsec para comunicações protegidas por IPsec.

    Para comunicação protegida por IPsec, a HRA (autoridade de registro de integridade), um computador que executa o Windows Server 2008 e o Serviços de Informações da Internet (IIS) que obtém certificados de integridade de uma autoridade de certificação (CA) para computadores compatíveis, passa as informações de status de integridade do cliente NAP para o servidor de diretiva de integridade NAP.

-   Um NAP ES DHCP para configuração de endereço IP baseado em DHCP.

    A NAP ES DHCP é uma funcionalidade no serviço do servidor DHCP que usa mensagens DHCP padrão do setor para se comunicar com o NAP EC DHCP em um cliente NAP. A imposição de DHCP para acesso limitado à rede é feita por meio de opções de DHCP.

-   Um Gateway TS (serviços de terminal) NAP ES para conexões baseadas no servidor Gateway TS.

Para as conexões VPN de acesso remoto e 802.1 X autenticadas, a funcionalidade no serviço NPS usa mensagens PEAP-TLV entre clientes NAP e o servidor de política de integridade NAP. A imposição de VPN é feita por meio de filtros de pacotes IP que são aplicados à conexão VPN. a imposição do 802.1 x é feita no dispositivo de acesso à rede 802.1 X aplicando filtros de pacote IP à conexão ou atribuindo a conexão uma ID de VLAN correspondente à rede restrita.

## <a name="nap-administration-server"></a>Servidor de administração NAP

O componente de servidor de administração NAP fornece os seguintes serviços:

-   Obtém o SSoHs do NAP ES por meio do serviço NPS.
-   Distribui o SoHs no SSoHs para os validadores de integridade do sistema (SHV) apropriados.
-   Coleta SoHRs dos SHVs e os passa para o serviço NPS para avaliação.

## <a name="nps-service"></a>Serviço NPS

O RADIUS é um protocolo amplamente implantado que permite autenticação centralizada, autorização e contabilidade para acesso à rede que é descrito em solicitações de comentários (RFCs) 2865 e 2866. Originalmente desenvolvido para acesso remoto dial-up, o RADIUS agora tem suporte de pontos de acesso sem fio, autenticação de comutadores Ethernet, servidores VPN, servidores de acesso DSL (Digital Subscriber Line) e outros servidores de acesso à rede.

O NPS é a implementação de um servidor RADIUS e proxy no Windows Server 2008. O NPS substitui o IAS (serviço de autenticação da Internet) no Windows Server 2003. Para a plataforma NAP, o serviço NPS inclui o componente de servidor de administrador NAP, suporte para a API SHV e SHVs instaláveis, e opções para configurar políticas de integridade.

Com base no SoHRs dos SHVs e das políticas de integridade configuradas, o serviço NPS cria uma SSoHR (declaração de resposta de integridade) do sistema, que indica se o cliente NAP está em conformidade ou não e inclui o conjunto de SoHRs de SHVs.

## <a name="system-health-validator-shv"></a>Validador da integridade do sistema (SHV)

Um SHV recebe uma SoH do servidor de administração de NAP e compara as informações de status de integridade do sistema com o estado de integridade do sistema necessário. Por exemplo, se a SoH for de um SHA de antivírus e contiver o número de versão do último arquivo de assinatura de vírus, o SHV de antivírus correspondente poderá verificar o servidor de requisitos de integridade do antivírus para obter o número de versão mais recente para validar a SoH do cliente NAP.

O SHV retorna um SoHR para o servidor de administração de NAP. O SoHR pode conter informações sobre como o SHA correspondente no cliente NAP pode atender aos requisitos atuais de integridade do sistema. Por exemplo, o SoHR enviado pelo SHV do antivírus pode instruir o SHA do antivírus no cliente NAP a solicitar a versão mais recente do arquivo de assinatura de antivírus de um servidor de assinatura antivírus específico por nome ou endereço IP.

 

 




