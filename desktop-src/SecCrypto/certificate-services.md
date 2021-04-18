---
description: Os serviços de certificados, um serviço em execução em um sistema operacional Windows Server, recebem solicitações para novos certificados digitais em transportes como RPC ou HTTP.
ms.assetid: 4c0098be-6b1b-4ce0-b3a0-942c1290b5b4
title: Serviços de Certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a3f25972f98a79a208719eb2bcb08de07d7894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760018"
---
# <a name="certificate-services"></a>Serviços de Certificados

Os [*serviços de certificados*](../secgloss/c-gly.md), um serviço em execução em um sistema operacional Windows Server, recebem solicitações para novos certificados digitais em transportes como RPC ou http. Ele verifica cada solicitação em políticas personalizadas ou específicas do site, define propriedades opcionais para um certificado a ser emitido e emite o certificado. Os serviços de certificados permitem que os administradores adicionem elementos a uma CRL ( [*lista de certificados revogados*](../secgloss/c-gly.md) ) e publiquem CRLs assinadas regularmente.

Os serviços de certificados incluem interfaces programáveis para a criação de suporte para transportes adicionais, políticas e propriedades e formatos de certificado.

No Windows Server 2003, os serviços de certificados 2,0 podem ser instalados no **painel de controle** clicando em **Adicionar ou remover programas** e, em seguida, clicando em **Adicionar/remover componentes do Windows** para instalar ou desinstalar os serviços de certificados.

Os conceitos dos serviços de certificados são detalhados nas seções a seguir. O conteúdo destina-se a ajudá-lo a desenvolver aplicativos que irão interagir com os serviços de certificados.



| Conteúdo                                                                                                                                                           | Seção                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Descrição dos recursos dos serviços de certificados                                                                                                               | [Recursos dos serviços de certificados](certificate-services-features.md)         |
| Visão geral da arquitetura dos serviços de certificados                                                                                                                     | [Arquitetura de serviços de certificados](certificate-services-architecture.md) |
| Relação entre um certificado, o assunto do certificado e a [ *chave pública* da entidade](../secgloss/p-gly.md) | [Certificados e chaves públicas](certificates-and-public-keys.md)           |
| Informações sobre as propriedades de solicitação de certificado                                                                                                              | [Diretrizes de solicitação de certificado](certificate-request-guidelines.md)       |
| Detalhes de como um certificado é processado pelos serviços de certificados                                                                                                 | [Sobre certificados](about-certificates.md)                               |
| Descrição do processo de renovação da [*autoridade de certificação*](../secgloss/c-gly.md)        | [Renovação da autoridade de certificação](certification-authority-renewal.md)     |



 

Os tópicos úteis adicionais a seguir também estão incluídos.



| Conteúdo                                                                                                                                             | Seção                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| Documentação sobre o controle de registro de certificado, que fornece serviços para a criação de solicitações de certificado, incluindo solicitações para usuários de cartão inteligente. | [Controle de registro de certificado](certificate-enrollment-control.md) |
| Documentação sobre a interface de programação de aplicativo de criptografia da Microsoft, que fornece serviços de segurança baseados em criptografia.                | [Noções básicas de criptografia](cryptography-essentials.md)               |
| Documentação no cartão inteligente, que fornece serviços para o desenvolvimento e o uso de sistemas de cartão inteligente.                                                   | [Cartão inteligente](../secauthn/smart-card-authentication.md)                     |
| Nomear Propriedades de certificados e solicitações de certificado.                                                                                           | [Propriedades do nome](name-properties.md)                               |
| Lista e descrições das propriedades do certificado [*X. 509*](../secgloss/x-gly.md) .                                  | [Propriedades do certificado](certificate-properties.md)                 |



 

 

 
