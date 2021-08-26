---
description: Antes de implementar o código que protege senhas, é melhor analisar seu ambiente específico para ver maneiras pelas quais um invasor pode tentar atacar as defesas de software.
ms.assetid: 4ebf7185-0179-4754-80da-63b0002c883f
title: Avaliação de Ameaças de Senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9042efa524b0503a648a195e77669b19231fec0445c4b0c8347b802b323076
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977146"
---
# <a name="password-threat-assessment"></a>Avaliação de Ameaças de Senha

Antes de implementar o código que protege senhas, é melhor analisar seu ambiente específico para ver maneiras pelas quais um invasor pode tentar atacar as defesas de software.

Comece analisando sua arquitetura de rede ou sistema. Estes são alguns exemplos:

-   O número de senhas que devem ser protegidas. Uma senha é necessária para fazer logoff no computador local? A mesma senha é usada para fazer logoff na rede? As senhas são propagadas para mais de um servidor na rede? Quantas senhas devem ser acomodadas?
-   O tipo de rede (se algum) que será usado. A rede é implementada usando um sistema de diretório corporativo (como LDAP) e sua arquitetura de senha é usada? Algum objeto está armazenar senhas não criptografadas?
-   Rede aberta versus fechada. A rede é autossu contida ou está aberta para o exterior? Se sim, ele é protegido por um firewall?
-   Acesso remoto. Os usuários precisarão acessar a rede de um local remoto?

Depois de analisar sua arquitetura de sistema ou rede, você pode começar a analisar como um invasor pode tentar atacar. Aqui estão algumas possibilidades:

-   Leia uma senha não criptografada do registro de um computador.
-   Leia uma senha não criptografada em código no software.
-   Leia uma senha não criptografada da página de código trocado de um computador.
-   Leia uma senha do log de eventos de um programa.
-   Leia uma senha de um esquema de serviço estendido do Microsoft Active Directory Directory que tem objetos que contêm uma senha de texto não criptografado.
-   Execute um depurador em um programa que requer uma senha.
-   Adivinhar uma senha. Qualquer uma das várias técnicas pode ser usada. Por exemplo, o invasor pode saber algumas informações pessoais sobre um usuário e tentar adivinhar uma senha com essas informações (por exemplo, o nome de um parceiro/parceiro ou filho). Ou um método de força bruta pode ser tentado, em que todas as combinações de letras, números e pontuação são tentadas (somente viável quando senhas curtas são usadas).

Comparar as possíveis metodologias de ataque com a arquitetura do sistema ou da rede provavelmente revelará riscos de segurança. Nesse ponto, um fator de risco pode ser estabelecido para cada risco e os fatores de risco podem ser usados para correções de triagem.

 

 



