---
description: Para obter credenciais diferentes das associadas à sessão de logon atual, preencha uma estrutura de \_ identidade de autenticação do Winnt da SEC \_ \_ com informações para a entidade de segurança alternativa.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Obtendo credenciais de resumo alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170805"
---
# <a name="obtaining-alternate-digest-credentials"></a>Obtendo credenciais de resumo alternativas

Para obter [*credenciais*](../secgloss/c-gly.md) diferentes das associadas à [*sessão*](../secgloss/s-gly.md)de logon atual, preencha uma estrutura [**de \_ \_ \_ identidade de autenticação do Winnt da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) com informações para a entidade de [*segurança*](../secgloss/s-gly.md)alternativa. Passe a estrutura para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) usando o parâmetro *pAuthData* .

A tabela a seguir descreve os membros da estrutura de [**\_ \_ \_ identidade de autenticação WinNT SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .



| Membro             | DESCRIÇÃO                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Usuário**           | Cadeia de caracteres terminada em nulo que contém o nome da entidade de segurança cujas credenciais serão usadas para estabelecer um contexto de segurança. |
| **Tamanho do**     | O comprimento do membro do **usuário** , em caracteres. Omita o nulo de terminação.                                                         |
| **Domínio**         | Cadeia de caracteres terminada em nulo que identifica o domínio que contém a conta da entidade de segurança.                                  |
| **DomainLength**   | O comprimento do membro do **domínio** , em caracteres. Omita o nulo de terminação.                                                       |
| **Senha**       | Cadeia de caracteres terminada em nulo que contém a senha da entidade de segurança.                                                            |
| **PasswordLength** | O comprimento do membro da **senha** , em caracteres. Omita o nulo de terminação.                                                     |
| **Sinalizadores**          | Indica se os membros da cadeia de caracteres estão no formato ANSI ou [*Unicode*](../secgloss/u-gly.md) .  |



 

A tabela a seguir lista os valores válidos para o membro **flags** da estrutura.



| Constante                            | Descrição                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| \_identidade de autenticação WinNT do s \_ \_ \_ ANSI    | As cadeias de caracteres nesta estrutura estão no formato ANSI.                                                                    |
| \_Unicode de \_ identidade de autenticação WinNT \_ s \_ | As cadeias de caracteres nesta estrutura estão no formato [*Unicode*](../secgloss/u-gly.md) . |



 

A estrutura e as constantes são declaradas no arquivo de cabeçalho rpcdce. h distribuído com o SDK (Software Development Kit) da plataforma.

O exemplo a seguir demonstra uma chamada do lado do cliente para obter credenciais de resumo para uma conta de usuário específica.


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



A função **\_ tcslen** retorna o comprimento da seqüência de caracteres em caracteres, sem incluir o caractere nulo de terminação.

Se seu aplicativo puder usar as credenciais estabelecidas no logon, consulte [obtendo credenciais de resumo padrão](obtaining-default-digest-credentials.md).

 

 
