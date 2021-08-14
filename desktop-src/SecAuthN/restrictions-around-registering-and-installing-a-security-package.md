---
description: Ações por pacotes de segurança que não têm suporte no Windows.
ms.assetid: E2BF8041-DF2F-4282-A3CC-A15FF2D7F4A2
title: Restrições em relação ao registro e instalação de um pacote de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce9f2d81a0a724d232e39c6e6fd7565b946ca319ba9f134041f6865b4bb2450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918902"
---
# <a name="restrictions-around-registering-and-installing-a-security-package"></a>Restrições em relação ao registro e instalação de um pacote de segurança

A remoção, substituição ou quebra automática de pacotes de segurança de caixa de entrada (por exemplo, Kerberos ou NTLM) não é uma ação com suporte no Windows e, a partir de 10 de janeiro de 2017, ela é impedida. Pacotes de segurança de terceiros (SSPs/APs) podem ser adicionados; no entanto, Windows não dá suporte à remoção de SSPs/APs pré-configurados. Especificamente, nunca houve suporte para a edição da configuração de registro Pacotes de Segurança **\\ \\ \\ \\ Lsa \\ OSConfig \\ do controle HKLM SYSTEM CurrentControlSet.**

A partir do Windows 8.1, os clientes que querem fornecer funcionalidade adicional podem adicionar seus Pacotes de Segurança usando a configuração do Registro Pacotes de Segurança **do HKLM SYSTEM CurrentControlSet Pacotes de Segurança \\ \\ \\ \\ Lsa \\** ( Registrando [DLLs SSP/AP](registering-ssp-ap-dlls.md)) e a configuração de registro associada **SecurityProviders** ( Writing [and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md)), se aplicável. Além disso, a [](../secgloss/s-gly.md#_security_security_package_gly) finalidade dos Pacotes de Segurança é implementar novos *protocolos* de segurança que podem estar na forma de um SSP (provedor de suporte de segurança) ou um AP [(pacote](../secgloss/a-gly.md#_security_authentication_package_gly) de autenticação). A finalidade de um SSP é fornecer serviços  de conexão autenticada, integridade de mensagem e criptografia de mensagem  que ainda não têm suporte no sistema, enquanto uma AP é usada para adicionar uma nova lógica de autenticação usada para determinar se um usuário deve fazer logon. 

A Microsoft está investindo na segurança do cliente e está tentando garantir que processos críticos, como SSPs e APs, não sejam facilmente removíveis do sistema. Portanto, a configuração de registro pacotes de segurança **\\ \\ \\ \\ Lsa \\ OSConfig \\ Security Packages** do controle HKLM SYSTEM Foi restrita a partir do Windows 8.1 para evitar alterações nele. Para facilitar pacotes de segurança de terceiros, os pacotes de segurança Lsa do controle **\\ \\ \\ \\ Lsa \\ do HKLM SYSTEM Foram** feitos a configuração designada para SSPs/APs personalizados. Além disso, é recomendável que qualquer funcionalidade em SSPs/APs personalizados que está fora do escopo dos Pacotes de Segurança definidos pela Microsoft seja removida desses SSPs/APs personalizados e que os Pacotes de Segurança de caixa de entrada não sejam removidos por nenhum produto.

 

 
