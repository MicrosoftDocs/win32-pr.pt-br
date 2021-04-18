---
description: Fornece um mecanismo para controlar o acesso a objetos protegíveis.
ms.assetid: 5923cb4c-f663-40d2-989a-07d71ac475db
title: Controle de Integridade de Credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c184ba01da0a55309fcb27ace9b0fe156edd6425
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105748955"
---
# <a name="mandatory-integrity-control"></a>Controle de Integridade de Credenciais

O Controle de Integridade de Credenciais (MIC) fornece um mecanismo para controlar o acesso a objetos protegíveis. Esse mecanismo é além do controle de acesso discricional e avalia o acesso antes que as verificações de acesso na [*lista de controle de acesso discricional*](/windows/desktop/SecGloss/d-gly) (DACL) de um objeto sejam avaliadas.

O MIC usa níveis de integridade e política obrigatória para avaliar o acesso. [*Entidades de segurança*](/windows/desktop/SecGloss/s-gly) e objetos protegíveis recebem níveis de integridade que determinam seus níveis de proteção ou acesso. Por exemplo, uma entidade com um nível de baixa integridade não pode gravar em um objeto com um nível de integridade médio, mesmo se a DACL do objeto permitir acesso de gravação à entidade de segurança.

O Windows define quatro níveis de integridade: baixo, médio, alto e sistema. Os usuários padrão recebem alto, os usuários com privilégios elevados recebem alta. Os processos que você inicia e os objetos criados recebem seu nível de integridade (médio ou alto) ou baixo se o nível do arquivo executável for baixo; os serviços do sistema recebem a integridade do sistema. Objetos que não têm um rótulo de integridade são tratados como médios pelo sistema operacional; Isso impede que o código de baixa integridade modifique objetos sem rótulo. Além disso, o Windows garante que os processos em execução com um nível de baixa integridade não possam obter acesso a um processo associado a um contêiner de aplicativo.

## <a name="integrity-labels"></a>Rótulos de integridade

Rótulos de integridade especificam os níveis de integridade de objetos protegíveis e entidades de segurança. Os rótulos de integridade são representados por [*SIDs de integridade*](/windows/desktop/SecGloss/i-gly). O SID de integridade para um objeto protegível é armazenado em sua SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema. A SACL contém uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) de [**\_ \_ rótulo \_ obrigatório do sistema**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) que, por sua vez, contém o Sid de integridade. Qualquer objeto sem um SID de integridade é tratado como se tivesse uma integridade média.

O SID de integridade para uma entidade de segurança é armazenado em seu token de acesso. Um token de acesso pode conter um ou mais SIDs de integridade.

Para obter informações detalhadas sobre os SIDs de integridade definidos, consulte [SIDs conhecidos](well-known-sids.md).

## <a name="process-creation"></a>Criação de processo

Quando um usuário tenta iniciar um arquivo executável, o novo processo é criado com o mínimo do nível de integridade do usuário e o nível de integridade do arquivo. Isso significa que o novo processo nunca será executado com maior integridade do que o arquivo executável. Se o usuário administrador executar um programa de baixa integridade, o token para o novo processo funcionará com o nível de baixa integridade. Isso ajuda a proteger um usuário que inicia código não confiável de atos mal-intencionados executados por esse código. Os dados do usuário, que estão no nível de integridade do usuário típico, são protegidos contra gravação em relação a esse novo processo.

## <a name="mandatory-policy"></a>Política obrigatória

A [**Ace \_ \_ \_ Ace do rótulo obrigatório do sistema**](/windows/desktop/api/Winnt/ns-winnt-system_mandatory_label_ace) na SACL de um objeto protegível contém uma máscara de acesso que especifica o acesso que as entidades de segurança com níveis de integridade inferiores ao objeto são concedidas. Os valores definidos para esta máscara de acesso **são \_ rótulo obrigatório do sistema \_ \_ sem \_ gravação \_**, **\_ rótulo obrigatório do sistema \_ \_ sem \_ leitura \_** e **\_ rótulo obrigatório do sistema \_ \_ não \_ executar \_**. Por padrão, o sistema cria todos os objetos com uma máscara de acesso de **\_ rótulo obrigatório do sistema \_ \_ sem \_ gravação \_**.

Cada token de acesso também especifica uma política obrigatória que é definida pela [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) quando o token é criado. Essa política é especificada por uma estrutura de [**\_ \_ política obrigatória de token**](/windows/desktop/api/Winnt/ns-winnt-token_mandatory_policy) associada ao token. Essa estrutura pode ser consultada chamando-se a função [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) com o valor do parâmetro *TokenInformationClass* definido como **TokenMandatoryPolicy**.

 

 
