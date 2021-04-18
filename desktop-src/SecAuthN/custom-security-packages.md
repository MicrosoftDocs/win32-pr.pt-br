---
description: Explica como criar pacotes de segurança personalizados usando a API personalizada do pacote de segurança.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Pacotes de segurança personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4c447f1a24a3edc2f25a55f83d82c174094c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748744"
---
# <a name="custom-security-packages"></a>Pacotes de segurança personalizados

Para implementar novos protocolos de segurança integrados com os sistemas operacionais Windows Server e Windows, use a API do pacote de segurança personalizado e as funções de [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA).

A API do pacote de segurança personalizado dá suporte ao desenvolvimento combinado de SSPs ( [*provedores de suporte de segurança*](/windows/desktop/SecGloss/s-gly) ) personalizados, que fornecem serviços de autenticação não [interativos](noninteractive-authentication.md) e troca segura de mensagens para aplicativos cliente/servidor, com o desenvolvimento de [*pacotes de autenticação*](/windows/desktop/SecGloss/a-gly)personalizados, que fornecem serviços para aplicativos que executam a [autenticação interativa](interactive-authentication.md). Esses serviços, quando combinados em um único pacote, são chamados de provedor de suporte de segurança/pacote de autenticação (SSP/AP).

Assim como acontece com os pacotes de segurança fornecidos pela Microsoft, os usuários do pacote de segurança personalizado acessam os serviços de autenticação interativa usando as [funções de logon do LSA](authentication-functions.md). Os serviços de proteção de mensagens e de autenticação não interativa podem ser acessados diretamente usando a [interface de provedor de suporte de segurança](sspi.md) (SSPI).

Os pacotes de segurança implantados no SSP/APs são totalmente integrados à LSA. Usando as funções de suporte LSA disponíveis para pacotes de segurança personalizados, os desenvolvedores podem implementar recursos avançados de segurança, como a criação de tokens, suporte a [*credenciais complementares*](/windows/desktop/SecGloss/s-gly) e autenticação de passagem. Para obter uma lista dessas funções de suporte, consulte [funções de LSA chamadas por pacotes de autenticação](authentication-functions.md). Para obter informações sobre como implementar pacotes de segurança personalizados, consulte [criando pacotes de segurança personalizados](creating-custom-security-packages.md).

Para obter mais informações sobre pacotes de segurança personalizados, consulte os tópicos a seguir.



| Tópico                                                                                                                                                 | Descrição                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/APs versus SSPs](ssp-aps-versus-ssps.md)<br/>                                                                                                | Informações sobre como determinar se um pacote de segurança deve estar em um SSP/ponto de acesso ou SSP.<br/> |
| [Modo LSA versus modo de usuário](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Os detalhes sobre como o modo LSA e o modo de usuário são diferentes.<br/>                                      |
| [Restrições sobre o registro e a instalação de um pacote de segurança](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Ações por pacotes de segurança que não têm suporte no Windows.<br/>                              |



 

 

