---
description: Um SID (identificador de segurança) é um valor exclusivo de comprimento variável usado para identificar um usuário confiável.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Identificadores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6acaaeacfbc77b2dc814062c4254c5f08e58869e0b6d8b2fbb64e8511dc31e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413486"
---
# <a name="security-identifiers"></a>Identificadores de segurança

Um [*SID (identificador de*](/windows/desktop/SecGloss/s-gly) segurança) é um valor exclusivo de comprimento variável usado para identificar um usuário [confiável.](trustees.md) Cada conta tem um SID exclusivo emitido por uma autoridade, como um Windows de domínio e armazenado em um banco de dados de segurança. Sempre que um usuário faz login, o sistema recupera o SID desse usuário do banco de dados e o coloca no token de [*acesso*](/windows/desktop/SecGloss/a-gly) para esse usuário. O sistema usa o SID no token de acesso para identificar o usuário em todas as interações subsequentes com Windows segurança. Quando um SID tiver sido usado como o identificador exclusivo de um usuário ou grupo, ele não poderá ser usado novamente para identificar outro usuário ou grupo.

Windows segurança usa SIDs nos seguintes elementos de segurança:

-   Em [descritores de segurança](security-descriptors.md) para identificar o proprietário de um objeto e grupo primário
-   Em [entradas de controle de acesso](access-control-entries.md), para identificar o usuário confiável para quem o acesso é permitido, negado ou auditado
-   Em [tokens de acesso](access-tokens.md), para identificar o usuário e os grupos aos quais o usuário pertence

Além dos SIDs específicos de domínio criados exclusivamente atribuídos a usuários e grupos [específicos, há SIDs](well-known-sids.md) conhecidos que identificam grupos genéricos e usuários genéricos. Por exemplo, os SIDs conhecidos, Todos e Mundo, identificam um grupo que inclui todos os usuários.

A maioria dos aplicativos nunca precisa trabalhar com SIDs. Como os nomes de [SIDs](well-known-sids.md) conhecidos podem variar, você deve usar as funções para criar o SID de constantes predefinidos em vez de usar o nome do SID conhecido. Por exemplo, a versão em inglês dos EUA do sistema operacional Windows tem um SID conhecido chamado "Administradores BUILTIN" que pode ter um nome diferente em versões internacionais do \\ sistema. Para ver um exemplo que cria um SID conhecido, consulte Pesquisando um SID em um [Token de Acesso no C++.](searching-for-a-sid-in-an-access-token-in-c--.md)

Se você precisar trabalhar com SIDs, não manipule-os diretamente. Em vez disso, use as funções a seguir.



| Função                                                       | Descrição                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Aloca e inicializa um SID com o número especificado de subautoridades.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Converte um SID em um formato de cadeia de caracteres adequado para exibição, armazenamento ou transporte.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Converte um SID de formato de cadeia de caracteres em um SID funcional válido.                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copia um SID de origem para um buffer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Testa dois valores de prefixo SID em busca de igualdade. Um prefixo SID é o SID inteiro, exceto pelo último valor de subautoridade.                                          |
| [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Testa dois SIDs em busca de igualdade. Eles devem corresponder exatamente para serem considerados iguais.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libera um SID alocado anteriormente usando a [**função AllocateAndInitializeSid.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Recupera o comprimento de um SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Recupera um ponteiro para a autoridade de identificador de um SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Recupera o tamanho do buffer necessário para armazenar um SID com um número especificado de subautoridades.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Recupera um ponteiro para uma subautoridade especificada em um SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Recupera o número de subautoridades em um SID.                                                                                                          |
| [**InitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Inicializa uma estrutura [**SID.**](/windows/desktop/api/Winnt/ns-winnt-sid)                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Testa a validade de um SID verificando se o número de revisão está dentro de um intervalo conhecido e se o número de subautoridades é menor que o máximo. |
| [**Lookupaccountname**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Recupera o SID que corresponde a um nome de conta especificado.                                                                                           |
| [**Lookupaccountsid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Recupera o nome da conta que corresponde a um SID especificado.                                                                                           |



 

 

 
