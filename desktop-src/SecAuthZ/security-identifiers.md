---
description: Um SID (identificador de segurança) é um valor exclusivo de comprimento variável usado para identificar um confiável.
ms.assetid: 7cb07bcd-70f4-43dd-8382-320fcff151c7
title: Identificadores de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368b2484cd8766aa7fa74c24679e82b10854e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752219"
---
# <a name="security-identifiers"></a>Identificadores de segurança

Um SID ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) é um valor exclusivo de comprimento variável usado para identificar um [confiável](trustees.md). Cada conta tem um SID exclusivo emitido por uma autoridade, como um controlador de domínio do Windows, e é armazenado em um banco de dados de segurança. Cada vez que um usuário faz logon, o sistema recupera o SID para esse usuário do banco de dados e o coloca no [*token de acesso*](/windows/desktop/SecGloss/a-gly) para esse usuário. O sistema usa o SID no token de acesso para identificar o usuário em todas as interações subsequentes com a segurança do Windows. Quando um SID é usado como o identificador exclusivo para um usuário ou grupo, ele não pode nunca ser usado novamente para identificar outro usuário ou grupo.

A segurança do Windows usa SIDs nos seguintes elementos de segurança:

-   Em [descritores de segurança](security-descriptors.md) para identificar o proprietário de um objeto e um grupo primário
-   Em [entradas de controle de acesso](access-control-entries.md), para identificar o confiável para quem o acesso é permitido, negado ou auditado
-   Em [tokens de acesso](access-tokens.md), para identificar o usuário e os grupos aos quais o usuário pertence

Além dos SIDs específicos de domínio criados com exclusividade atribuídos a usuários e grupos específicos, há [SIDs conhecidos](well-known-sids.md) que identificam grupos genéricos e usuários genéricos. Por exemplo, os SIDs conhecidos, todos e mundo, identificam um grupo que inclui todos os usuários.

A maioria dos aplicativos nunca precisa trabalhar com SIDs. Como os nomes de [SIDs bem conhecidos](well-known-sids.md) podem variar, você deve usar as funções para criar o Sid de constantes predefinidas em vez de usar o nome do SID conhecido. Por exemplo, a versão em inglês dos EUA do sistema operacional Windows tem um SID conhecido chamado "administradores internos \\ " que pode ter um nome diferente em versões internacionais do sistema. Para obter um exemplo que cria um SID conhecido, consulte [pesquisando um SID em um token de acesso em C++](searching-for-a-sid-in-an-access-token-in-c--.md).

Se você precisar trabalhar com SIDs, não os manipule diretamente. Em vez disso, use as funções a seguir.



| Função                                                       | Descrição                                                                                                                                               |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid)   | Aloca e inicializa um SID com o número especificado de subautons.                                                                              |
| [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida)         | Converte um SID em um formato de cadeia de caracteres adequado para exibição, armazenamento ou transporte.                                                                            |
| [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)         | Converte um SID de formato de cadeia de caracteres em um SID funcional válido.                                                                                                  |
| [**CopySid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-copysid)                                     | Copia um SID de origem para um buffer.                                                                                                                          |
| [**EqualPrefixSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalprefixsid)                       | Testa dois valores de prefixo SID para igualdade. Um prefixo SID é o SID inteiro, exceto o último valor de subautoridade.                                          |
| [**Equalid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid)                                   | Testa dois SIDs para igualdade. Eles devem corresponder exatamente para serem considerados iguais.                                                                              |
| [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid)                                     | Libera um SID alocado anteriormente usando a função [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) .                                      |
| [**GetLengthSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getlengthsid)                           | Recupera o comprimento de um SID.                                                                                                                            |
| [**GetSidIdentifierAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsididentifierauthority) | Recupera um ponteiro para a autoridade de identificador de um SID.                                                                                                |
| [**GetSidLengthRequired**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidlengthrequired)           | Recupera o tamanho do buffer necessário para armazenar um SID com um número especificado de subautons.                                                       |
| [**GetSidSubAuthority**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority)               | Recupera um ponteiro para uma subautoridade especificada em um SID.                                                                                                 |
| [**GetSidSubAuthorityCount**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsidsubauthoritycount)     | Recupera o número de subautorizações em um SID.                                                                                                          |
| [**Inicializaid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializesid)                         | Inicializa uma estrutura de [**Sid**](/windows/desktop/api/Winnt/ns-winnt-sid) .                                                                                                               |
| [**IsValidSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-isvalidsid)                               | Testa a validade de um SID verificando se o número de revisão está dentro de um intervalo conhecido e se o número de subautons é menor que o máximo. |
| [**LookupAccountName**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountnamea)                 | Recupera o SID que corresponde a um nome de conta especificado.                                                                                           |
| [**LookupAccountSid**](/windows/desktop/api/Winbase/nf-winbase-lookupaccountsida)                   | Recupera o nome da conta que corresponde a um SID especificado.                                                                                           |



 

 

 
