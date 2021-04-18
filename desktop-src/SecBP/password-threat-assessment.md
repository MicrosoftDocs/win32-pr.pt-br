---
description: Antes de implementar o código que protege as senhas, é melhor analisar seu ambiente específico de maneiras que um invasor possa tentar penetrar nas defesas de software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Avaliação de ameaças de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48a79d44bda9714083c5dd1085e9d09497e7341
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756691"
---
# <a name="password-threat-assessment"></a>Avaliação de ameaças de senha

Antes de implementar o código que protege as senhas, é melhor analisar seu ambiente específico de maneiras que um invasor possa tentar penetrar nas defesas de software.

Comece analisando sua arquitetura de rede ou de sistema. Estes são alguns exemplos:

-   O número de senhas que devem ser protegidas. É necessária uma senha para fazer logon no computador local? A mesma senha é usada para fazer logon na rede? As senhas são propagadas para mais de um servidor na rede? Quantas senhas devem ser acomodadas?
-   O tipo de rede (se houver) que será usado. A rede é implementada usando um sistema de diretório corporativo (como LDAP) e sua arquitetura de senha é usada? Os objetos estão armazenando senhas não criptografadas?
-   Abrir rede versus fechada. A rede é independente ou está aberta para o exterior? Nesse caso, ele é protegido por um firewall?
-   Acesso remoto. Os usuários precisarão acessar a rede de um local remoto?

Depois de analisar o sistema ou a arquitetura de rede, você pode começar a analisar como um invasor pode tentar atacar. Aqui estão algumas possibilidades:

-   Ler uma senha não criptografada do registro de um computador.
-   Ler uma senha não criptografada que é embutida no software.
-   Ler uma senha não criptografada na página de código trocado de um computador.
-   Ler uma senha do log de eventos de um programa.
-   Leia uma senha de um esquema de serviço de diretório do Microsoft Active Directory estendido que tenha objetos que contenham uma senha de texto sem formatação.
-   Execute um depurador em um programa que exija uma senha.
-   Adivinhe uma senha. Qualquer uma das várias técnicas pode ser usada. Por exemplo, o invasor pode saber algumas informações pessoais sobre um usuário e tentar adivinhar uma senha dessas informações (por exemplo, o nome de um cônjuge ou parceiro ou filho). Ou, um método de força bruta pode ser tentado, onde todas as combinações de letras, números e pontuações são tentadas (somente viáveis onde são usadas senhas curtas).

Comparar as possíveis metodologias de ataque com a arquitetura de rede ou sistema provavelmente revelará os riscos de segurança. Nesse ponto, um fator de risco pode ser estabelecido para cada risco, e os fatores de risco podem ser usados para fazer a triagem de correções.

 

 



