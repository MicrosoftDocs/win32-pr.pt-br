---
description: Quando um aplicativo cliente faz logon no Instrumentação de Gerenciamento do Windows (WMI) pela primeira vez, ele deve definir o nível de segurança do processo padrão com uma chamada para CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Definindo o nível de segurança do processo padrão usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506221"
---
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="1ea44-103">Definindo o nível de segurança do processo padrão usando C++</span><span class="sxs-lookup"><span data-stu-id="1ea44-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="1ea44-104">Quando um aplicativo cliente faz logon no Instrumentação de Gerenciamento do Windows (WMI) pela primeira vez, ele deve definir o nível de segurança do processo padrão com uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="1ea44-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="1ea44-105">COM usa as informações na chamada para determinar a quantidade de segurança que outro processo deve ter para acessar o processo do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1ea44-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="1ea44-106">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="1ea44-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="1ea44-107">Alterando as credenciais de autenticação padrão usando C++</span><span class="sxs-lookup"><span data-stu-id="1ea44-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="1ea44-108">Alterando os níveis de representação padrão usando C++</span><span class="sxs-lookup"><span data-stu-id="1ea44-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="1ea44-109">Para a maioria dos aplicativos cliente, os argumentos mostrados no exemplo a seguir definem a segurança padrão para o WMI.</span><span class="sxs-lookup"><span data-stu-id="1ea44-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



<span data-ttu-id="1ea44-110">O código requer as referências a seguir e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="1ea44-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="1ea44-111">Definir o nível de autenticação para o **\_ padrão de \_ \_ nível \_ da autenticação RPC C** permite que o DCOM negocie o nível de autenticação para corresponder às demandas de segurança do computador de destino.</span><span class="sxs-lookup"><span data-stu-id="1ea44-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="1ea44-112">Para obter mais informações, consulte [alterando as credenciais de autenticação padrão usando c++](#changing-the-default-authentication-credentials-using-c) e [alterando as configurações de representação padrão usando c++](#changing-the-default-impersonation-levels-using-c).</span><span class="sxs-lookup"><span data-stu-id="1ea44-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="1ea44-113">Alterando as credenciais de autenticação padrão usando C++</span><span class="sxs-lookup"><span data-stu-id="1ea44-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="1ea44-114">As credenciais de autenticação padrão funcionam para a maioria das situações, mas talvez seja necessário usar credenciais de autenticação diferentes em situações diferentes.</span><span class="sxs-lookup"><span data-stu-id="1ea44-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="1ea44-115">Por exemplo, talvez você queira adicionar criptografia aos procedimentos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="1ea44-116">A tabela a seguir lista e descreve os diferentes níveis de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="1ea44-117">Nível de autenticação</span><span class="sxs-lookup"><span data-stu-id="1ea44-117">Authentication level</span></span>                 | <span data-ttu-id="1ea44-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ea44-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea44-119">\_padrão de \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ea44-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="1ea44-120">Autenticação de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="1ea44-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="1ea44-121">RPC \_ C \_ Authn \_ nível \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="1ea44-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="1ea44-122">Sem autenticação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="1ea44-123">\_conexão em \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ea44-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="1ea44-124">Autenticação somente quando o cliente cria uma relação com o servidor.</span><span class="sxs-lookup"><span data-stu-id="1ea44-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="1ea44-125">\_chamada de \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ea44-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="1ea44-126">Autenticação toda vez que o servidor recebe um RPC.</span><span class="sxs-lookup"><span data-stu-id="1ea44-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="1ea44-127">\_PCT do \_ nível de autenticação RPC C \_ \_</span><span class="sxs-lookup"><span data-stu-id="1ea44-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="1ea44-128">Autenticação toda vez que o servidor recebe dados de um cliente.</span><span class="sxs-lookup"><span data-stu-id="1ea44-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="1ea44-129">\_integridade de \_ pkt do \_ nível \_ de \_ autenticação RPC C</span><span class="sxs-lookup"><span data-stu-id="1ea44-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="1ea44-130">Autenticação que nenhum dado do pacote foi modificado.</span><span class="sxs-lookup"><span data-stu-id="1ea44-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="1ea44-131">\_privacidade do \_ PCT do \_ nível \_ de \_ autenticação RPC C</span><span class="sxs-lookup"><span data-stu-id="1ea44-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="1ea44-132">Inclui todos os níveis de autenticação anteriores e criptografa o valor de cada chamada RPC.</span><span class="sxs-lookup"><span data-stu-id="1ea44-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="1ea44-133">Você pode especificar as credenciais de autenticação padrão para vários usuários usando uma estrutura de **\_ \_ lista de autenticação exclusiva** no parâmetro *pAuthList* de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="1ea44-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="1ea44-134">O exemplo de código a seguir mostra como alterar as credenciais de autenticação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-134">The following code example shows how to change the authentication credentials.</span></span>


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="1ea44-135">Alterando os níveis de representação padrão usando C++</span><span class="sxs-lookup"><span data-stu-id="1ea44-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="1ea44-136">O COM fornece níveis de segurança padrão lidos no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="1ea44-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="1ea44-137">No entanto, a menos que seja especificamente modificado, as configurações do registro definem o nível de representação muito baixo para que o WMI funcione.</span><span class="sxs-lookup"><span data-stu-id="1ea44-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="1ea44-138">Normalmente, o nível de representação padrão é a **identificação do nível de imp do RPC \_ c \_ \_ \_**, mas o WMI precisa de pelo menos a representação de **nível de imp do RPC \_ c \_ \_ \_** para funcionar com a maioria dos provedores, e você pode encontrar uma situação em que você precisa definir um nível mais alto de representação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="1ea44-139">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="1ea44-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="1ea44-140">A tabela a seguir lista os diferentes níveis de representação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="1ea44-141">Nível</span><span class="sxs-lookup"><span data-stu-id="1ea44-141">Level</span></span>                           | <span data-ttu-id="1ea44-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ea44-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea44-143">\_padrão de \_ nível de imp \_ \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="1ea44-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="1ea44-144">O sistema operacional escolhe o nível de representação.</span><span class="sxs-lookup"><span data-stu-id="1ea44-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="1ea44-145">nível de imp do RPC \_ C- \_ \_ \_ anônimo</span><span class="sxs-lookup"><span data-stu-id="1ea44-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="1ea44-146">O servidor pode representar o cliente, mas o token de representação não pode ser usado para nada.</span><span class="sxs-lookup"><span data-stu-id="1ea44-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="1ea44-147">\_identificação de \_ nível de imp \_ \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="1ea44-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="1ea44-148">O servidor pode obter a identidade do cliente e representar o cliente para verificação de ACL.</span><span class="sxs-lookup"><span data-stu-id="1ea44-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="1ea44-149">\_representação de \_ nível de imp \_ \_ do RPC C</span><span class="sxs-lookup"><span data-stu-id="1ea44-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="1ea44-150">O servidor pode representar o cliente em um limite de computador.</span><span class="sxs-lookup"><span data-stu-id="1ea44-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="1ea44-151">\_delegado de \_ nível de imp \_ \_ de RPC C</span><span class="sxs-lookup"><span data-stu-id="1ea44-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="1ea44-152">O servidor pode representar o cliente entre vários limites e pode fazer chamadas em nome do cliente.</span><span class="sxs-lookup"><span data-stu-id="1ea44-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 
