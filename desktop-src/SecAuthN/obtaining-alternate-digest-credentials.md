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
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="f4d75-103">Obtendo credenciais de resumo alternativas</span><span class="sxs-lookup"><span data-stu-id="f4d75-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="f4d75-104">Para obter [*credenciais*](../secgloss/c-gly.md) diferentes das associadas à [*sessão*](../secgloss/s-gly.md)de logon atual, preencha uma estrutura [**de \_ \_ \_ identidade de autenticação do Winnt da SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) com informações para a entidade de [*segurança*](../secgloss/s-gly.md)alternativa.</span><span class="sxs-lookup"><span data-stu-id="f4d75-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="f4d75-105">Passe a estrutura para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) usando o parâmetro *pAuthData* .</span><span class="sxs-lookup"><span data-stu-id="f4d75-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="f4d75-106">A tabela a seguir descreve os membros da estrutura de [**\_ \_ \_ identidade de autenticação WinNT SEC**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="f4d75-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="f4d75-107">Membro</span><span class="sxs-lookup"><span data-stu-id="f4d75-107">Member</span></span>             | <span data-ttu-id="f4d75-108">DESCRIÇÃO</span><span class="sxs-lookup"><span data-stu-id="f4d75-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d75-109">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="f4d75-109">**User**</span></span>           | <span data-ttu-id="f4d75-110">Cadeia de caracteres terminada em nulo que contém o nome da entidade de segurança cujas credenciais serão usadas para estabelecer um contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="f4d75-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="f4d75-111">**Tamanho do**</span><span class="sxs-lookup"><span data-stu-id="f4d75-111">**UserLength**</span></span>     | <span data-ttu-id="f4d75-112">O comprimento do membro do **usuário** , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4d75-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="f4d75-113">Omita o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="f4d75-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="f4d75-114">**Domínio**</span><span class="sxs-lookup"><span data-stu-id="f4d75-114">**Domain**</span></span>         | <span data-ttu-id="f4d75-115">Cadeia de caracteres terminada em nulo que identifica o domínio que contém a conta da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="f4d75-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="f4d75-116">**DomainLength**</span><span class="sxs-lookup"><span data-stu-id="f4d75-116">**DomainLength**</span></span>   | <span data-ttu-id="f4d75-117">O comprimento do membro do **domínio** , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4d75-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="f4d75-118">Omita o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="f4d75-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="f4d75-119">**Senha**</span><span class="sxs-lookup"><span data-stu-id="f4d75-119">**Password**</span></span>       | <span data-ttu-id="f4d75-120">Cadeia de caracteres terminada em nulo que contém a senha da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="f4d75-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="f4d75-121">**PasswordLength**</span><span class="sxs-lookup"><span data-stu-id="f4d75-121">**PasswordLength**</span></span> | <span data-ttu-id="f4d75-122">O comprimento do membro da **senha** , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4d75-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="f4d75-123">Omita o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="f4d75-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="f4d75-124">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="f4d75-124">**Flags**</span></span>          | <span data-ttu-id="f4d75-125">Indica se os membros da cadeia de caracteres estão no formato ANSI ou [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f4d75-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="f4d75-126">A tabela a seguir lista os valores válidos para o membro **flags** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="f4d75-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="f4d75-127">Constante</span><span class="sxs-lookup"><span data-stu-id="f4d75-127">Constant</span></span>                            | <span data-ttu-id="f4d75-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4d75-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d75-129">\_identidade de autenticação WinNT do s \_ \_ \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="f4d75-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="f4d75-130">As cadeias de caracteres nesta estrutura estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f4d75-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="f4d75-131">\_Unicode de \_ identidade de autenticação WinNT \_ s \_</span><span class="sxs-lookup"><span data-stu-id="f4d75-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="f4d75-132">As cadeias de caracteres nesta estrutura estão no formato [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f4d75-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="f4d75-133">A estrutura e as constantes são declaradas no arquivo de cabeçalho rpcdce. h distribuído com o SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="f4d75-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="f4d75-134">O exemplo a seguir demonstra uma chamada do lado do cliente para obter credenciais de resumo para uma conta de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="f4d75-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


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



<span data-ttu-id="f4d75-135">A função **\_ tcslen** retorna o comprimento da seqüência de caracteres em caracteres, sem incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="f4d75-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="f4d75-136">Se seu aplicativo puder usar as credenciais estabelecidas no logon, consulte [obtendo credenciais de resumo padrão](obtaining-default-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="f4d75-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
