---
description: desenvolva aplicativos de área de trabalho mais seguros usando Windows APIs e serviços.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Segurança e identidade
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ff19c113340af314177b821bfd8294036d752d90218a5255eb6a429e9b6312ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226331"
---
# <a name="security-and-identity"></a>Segurança e identidade

desenvolva aplicativos de área de trabalho mais seguros usando Windows APIs e serviços. Essas APIs fornecem:

- Autenticação
- Autorização
- Criptografia
- Serviços de diretório, identidade e acesso
- Controles dos pais
- Gerenciamento de direitos

Esta seção também fornece as práticas recomendadas e outros artigos de segurança.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
| ----- | ----------- |
| [Interface de verificação de antimalware](./amsi/antimalware-scan-interface-portal.md) | A interface de verificação antimalware (AMSI) é um padrão de interface genérico que permite que aplicativos e serviços se integrem a qualquer produto Antimalware presente em um computador. Ele fornece proteção avançada contra malware para usuários e seus dados, aplicativos e cargas de trabalho. |
| [Autenticação](./secauthn/authentication-portal.md) | A autenticação é o processo pelo qual o sistema valida as informações de logon de um usuário. O nome e a senha de um usuário são comparados a uma lista autorizada e, se o sistema detectar uma correspondência, o acesso será concedido à extensão especificada na lista de permissões para esse usuário. |
| [Autorização](./secauthz/authorization-portal.md) | A autorização é o direito concedido a um indivíduo para usar o sistema e os dados armazenados nele. A autorização normalmente é configurada por um administrador do sistema e verificada pelo computador com base em alguma forma de identificação de usuário, como um número de código ou senha. |
| [Práticas recomendadas para as APIs de segurança](./secbp/best-practices-for-the-security-apis.md) | Fornece as práticas recomendadas para o desenvolvimento de aplicativos mais seguros. |
| [API de registro de certificado](./seccertenroll/certenroll-portal.md) | A API de registro de certificado pode ser usada para criar um aplicativo cliente para solicitar um certificado e instalar uma resposta de certificado. |
| [CFG (Proteção de Fluxo de Controle) ](./secbp/control-flow-guard.md) | o CFG (Control Flow Guard) é um recurso de segurança de plataforma altamente otimizado que foi criado para combater vulnerabilidades de corrupção de memória. |
| [Criptografia](./seccrypto/cryptography-portal.md) | Criptografia é o uso de códigos para converter dados para que apenas um destinatário específico possa lê-los, usando uma chave. O CryptoAPI permite que os usuários criem e troquem documentos e outros dados em um ambiente seguro, especialmente em mídias não seguras, como a Internet. |
| [API de criptografia: próxima geração](./seccng/cng-portal.md) | A CNG (API de criptografia: próxima geração) permite que os usuários criem e troquem documentos e outros dados em um ambiente seguro, especialmente em mídias não seguras, como a Internet. |
| [Extensibilidade do desenvolvedor de controle de acesso dinâmico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | o cenário de DAC (controle de acesso dinâmico), conforme fornecido no Windows Server 2012, tem uma variedade de pontos de extensibilidade do desenvolvedor que adicionam potencial de personalização ao desenvolvimento de aplicativos. |
| [diretório, identidade e Serviços do Access](./srvnodes/directory--identity--and-access-services.md) | Os administradores de rede podem usar os serviços de diretório para automatizar tarefas administrativas comuns, como adicionar usuários e grupos, gerenciar impressoras e definir permissões em recursos de rede.<br/> Fornecedores independentes de software e desenvolvedores de usuário final podem usar serviços de diretório para habilitar o diretório de seus produtos e aplicativos. Os serviços podem se publicar em um diretório, os clientes podem usar o diretório para localizar serviços e ambos podem usar o diretório para localizar e manipular outros objetos.<br/> O Forefront Identity Manager (FIM) fornece uma solução integrada e abrangente para gerenciar todo o ciclo de vida de identidades de usuário e suas credenciais associadas.<br/> O gerenciamento de ciclo de vida de identidade (ILM) permite que as organizações de ti reduzam o custo de gerenciar o ciclo de vida de identidade e acesso fornecendo uma única exibição da identidade de um usuário em toda a empresa heterogênea e por meio da automação de tarefas comuns.<br/> O Serviço de Federação de Active Directory (AD FS) permite o gerenciamento de identidades e acessos federados, compartilhando com segurança a identidade digital e direitos de direito em limites de segurança e corporativos. |
| [Protocolo EAP (Extensible Authentication Protocol)](./eap/extensible-authentication-protocol-reference.md) | O EAP (protocolo de autenticação extensível) é um padrão compatível com vários componentes do sistema. O EAP é crucial para proteger a segurança de LANs sem fio (802.1 X) e com fio, dial-up e redes virtuais privadas (VPNs). |
| [Host do protocolo de autenticação extensível](./eaphost/about-eap-host.md) | o EAPHost é um componente de rede Windows da Microsoft que fornece uma infraestrutura EAP (Extensible Authentication Protocol) para a autenticação de implementações de protocolo "suplicante", como 802.1 x e ponto a ponto (PPP). |
| [API de gerenciamento de senhas MS-CHAP](/previous-versions/windows/desktop/mschap/portal) | Você pode usar a API de gerenciamento de senhas do MS-CHAP para criar aplicativos para alterar as senhas de usuários em rede em estações de trabalho remotas. |
| [Proteção de Acesso à Rede](./nap/network-access-protection-start-page.md) | A NAP (proteção de acesso à rede) é um conjunto de componentes do sistema operacional que fornece uma plataforma para acesso protegido a redes privadas. A plataforma NAP fornece uma maneira integrada de avaliar o estado de integridade do sistema de um cliente de rede que está tentando se conectar ou se comunicar em uma rede e restringir o acesso do cliente de rede até que os requisitos da política de integridade sejam atendidos. |
| [Servidor de Políticas de Rede](./nps/portal.md) | O NPS (servidor de diretivas de rede) é a implementação da Microsoft de um servidor RADIUS e proxy de autenticação remota. É o sucessor do IAS (serviço de autenticação da Internet). |
| [Controles dos pais](./parcon/parental-controls-portal.md) | a tecnologia de controles dos pais no Windows destina-se a auxiliar os pais ou tutores na garantia de acesso aos materiais apropriados por idade ou nível de maturidade para aqueles sob sua guardião. Ele fornece uma infraestrutura extensível, além de recursos internos. |
| [Rights Management](./srvnodes/rights-management.md) | Três gerações do SDK do Rights Management agora estão disponíveis, bem como um roteiro para todos os exemplos de código RMS fornecidos pela Microsoft e ferramentas de desenvolvedor em todos os sistemas operacionais com suporte; Android, iOS/OS X, Windows Phone e área de trabalho do Windows. |
| [Security Development Lifecycle (SDL)-diretrizes de processo](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Microsoft Security Development Lifecycle (SDL) é um processo de garantia de segurança de software líder do setor. Uma iniciativa da Microsoft e uma política obrigatória desde 2004, o SDL tem desempenhado um papel fundamental na incorporação de segurança e privacidade em software e cultura da Microsoft. Combinando uma abordagem holística e prática, o SDL apresenta segurança e privacidade no início e em todas as fases do processo de desenvolvimento. |
| [Gerenciamento de segurança](./secmgmt/management-portal.md) | As tecnologias de gerenciamento de segurança podem ser usadas para gerenciar política de autoridade de segurança local (LSA) e política de filtro de senha, consultar a capacidade de programas de fontes externas e anexos de serviço que estendem a funcionalidade da ferramenta de configuração de segurança. |
| [Provedores WMI de segurança](./secprov/secprov-portal.md) | os provedores de segurança WMI permitem que administradores e programadores configurem Criptografia de Unidade de Disco BitLocker (BDE) e o Trusted Platform Module (TPM) usando Instrumentação de Gerenciamento do Windows (WMI). |
| [Glossário de segurança](./secgloss/security-glossary.md) | Fornece um glossário de termos de segurança. |
| [Serviços base do TPM](./tbs/tpm-base-services-portal.md) | O recurso TBS (serviços base) do Trusted Platform Module (TPM) centraliza o acesso do TPM entre aplicativos. O recurso TBS usa prioridades especificadas chamando aplicativos para agendar de acordo com o acesso do TPM. |
| [API do Windows Biometric Framework](./secbiomet/biometric-service-api-portal.md) | você pode usar a API Windows Biometric Framework para criar aplicativos cliente que capturam, salvam e comparam informações biométricas do usuário final com segurança. |
| [Artigos técnicos sobre segurança](https://msdn.microsoft.com/library/hh322936.aspx) | Artigos sobre segurança e criptografia. |



 

 

 