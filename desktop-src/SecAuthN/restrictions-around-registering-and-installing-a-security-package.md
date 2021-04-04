---
description: Ações por pacotes de segurança que não têm suporte no Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restrições sobre o registro e a instalação de um pacote de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd10cd8e2e98d4dccfc3a6230c3daecaeb8fec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646677"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restrições sobre o registro e a instalação de um pacote de segurança

A remoção, substituição ou encapsulamento de pacotes de segurança de caixa de entrada (por exemplo, Kerberos ou NTLM) não é uma ação com suporte no Windows e a partir de 10 de janeiro de 2017, ele é impedido. Pacotes de segurança de terceiros (SSPs/APs) podem ser adicionados; no entanto, o Windows não oferece suporte à remoção de SSPs/APs pré-configurados. Especificamente, a edição da configuração do registro de **pacotes de \\ \\ \\ \\ \\ \\ segurança de OSConfig do sistema HKLM do System CurrentControlSet** nunca foi suportada.

A partir do Windows 8.1, os clientes que desejam fornecer funcionalidade adicional podem adicionar seus pacotes de segurança usando a configuração do registro **HKLM \\ sistema \\ CurrentControlSet \\ controle \\ LSA \\ pacotes de segurança** ([registrando as DLLs do SSP/AP](registering-ssp-ap-dlls.md)) e a configuração do registro associada **SecurityProviders** ([gravando e instalando um provedor de suporte de segurança](writing-and-installing-a-security-support-provider.md)), se aplicável. Além disso, a finalidade dos [pacotes de segurança](../secgloss/s-gly.md#_security_security_package_gly) é implementar novos protocolos de *segurança* que podem estar na forma de um SSP (provedor de suporte de segurança) ou de um pacote de [autenticação](../secgloss/a-gly.md#_security_authentication_package_gly) (AP). A finalidade de um SSP é fornecer *conexão autenticada*, *integridade da mensagem* e serviços de *criptografia de mensagens* que ainda não têm suporte no sistema, enquanto um AP é usado para adicionar uma nova lógica de *autenticação* usada para determinar se deve permitir que um usuário faça logon.

A Microsoft investiu na segurança do cliente e está tentando garantir que processos críticos, como SSPs e APs, não sejam facilmente removíveis do sistema. Portanto, a configuração do registro de **\\ pacotes de segurança do sistema HKLM \\ \\ \\ \\ OSConfig \\ LSA** foi restrita a partir de Windows 8.1 para evitar alterações nele. Para facilitar os pacotes de segurança de terceiros, os **pacotes de segurança do sistema de HKLM \\ controlados pelo System \\ CurrentControlSet \\ \\ \\ Packages** foram feitas na configuração designada para SSPs/APS personalizados. É recomendável que qualquer funcionalidade em SSPs/APs personalizados que esteja fora do escopo dos pacotes de segurança definidos pela Microsoft seja removida de SSPs/APs personalizados, e que os pacotes de segurança de caixa de entrada não sejam removidos por nenhum produto.

 

 
