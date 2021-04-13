---
description: A infraestrutura do VSS requer que os solicitantes VSS, como aplicativos de backup, possam funcionar como clientes COM e como um servidor.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considerações de segurança para solicitantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296651"
---
# <a name="security-considerations-for-requesters"></a><span data-ttu-id="cf4d3-103">Considerações de segurança para solicitantes</span><span class="sxs-lookup"><span data-stu-id="cf4d3-103">Security Considerations for Requesters</span></span>

<span data-ttu-id="cf4d3-104">A infraestrutura do VSS requer que os solicitantes VSS, como aplicativos de backup, possam funcionar como clientes COM e como um servidor.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-104">The VSS infrastructure requires VSS requesters, such as backup applications, to be able to function both as COM clients and as a server.</span></span>

<span data-ttu-id="cf4d3-105">Ao atuar como um servidor, um solicitante expõe um conjunto de interfaces de retorno de chamada COM que pode ser invocado a partir de processos externos (como gravadores ou o serviço VSS).</span><span class="sxs-lookup"><span data-stu-id="cf4d3-105">When acting as a server, a requester exposes a set of COM callback interfaces that can be invoked from external processes (such as writers or the VSS service).</span></span> <span data-ttu-id="cf4d3-106">Portanto, os solicitantes precisam gerenciar com segurança quais clientes COM são capazes de fazer chamadas COM de entrada em seu processo.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-106">Therefore, requesters need to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="cf4d3-107">Da mesma forma, os solicitantes podem atuar como um cliente COM para as APIs COM fornecidas por um gravador VSS ou pelo serviço VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-107">Similarly, requesters can act as a COM client for the COM APIs supplied by a VSS writer or by the VSS service.</span></span> <span data-ttu-id="cf4d3-108">As configurações de segurança específicas do solicitante devem permitir chamadas COM de saída do solicitante para esses outros processos.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-108">The requester-specific security settings must allow outgoing COM calls from the requester to these other processes.</span></span>

<span data-ttu-id="cf4d3-109">O mecanismo mais simples para gerenciar os problemas de segurança de um solicitante envolve a seleção adequada da conta de usuário sob a qual ele é executado.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-109">The simplest mechanism for managing a requester's security issues involves proper selection of the user account under which it runs.</span></span>

<span data-ttu-id="cf4d3-110">Normalmente, um solicitante precisa ser executado sob um usuário que seja membro do grupo Administradores ou do grupo operadores de backup ou seja executado como a conta sistema local.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-110">A requester typically needs to run under a user that is a member of either the Administrators group or the Backup Operators group, or run as the Local System account.</span></span>

<span data-ttu-id="cf4d3-111">Por padrão, quando um solicitante estiver agindo como um cliente COM, se ele não for executado nessas contas, qualquer chamada COM será rejeitada automaticamente com **E \_ ACCESSDENIED**, sem até mesmo a implementação do método com.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-111">By default, when a requester is acting as a COM client, if it does not run under these accounts, any COM call is automatically rejected with **E\_ACCESSDENIED**, without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="cf4d3-112">Desabilitando a manipulação de exceção COM</span><span class="sxs-lookup"><span data-stu-id="cf4d3-112">Disabling COM Exception Handling</span></span>

<span data-ttu-id="cf4d3-113">Ao desenvolver um solicitante, defina o sinalizador COM COMGLB \_ exceção \_ não cercamento \_ manipular opções globais para desabilitar a manipulação de exceções com.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-113">When developing a requester, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="cf4d3-114">É importante fazer isso porque a manipulação de exceção COM pode mascarar erros fatais em um aplicativo VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-114">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="cf4d3-115">O erro mascarado pode deixar o processo em um estado instável e imprevisível, o que pode levar a corrupções e travamentos.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-115">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="cf4d3-116">Para obter mais informações sobre esse sinalizador, consulte [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="cf4d3-116">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-requester-default-com-access-check-permission"></a><span data-ttu-id="cf4d3-117">Definindo permissão de verificação de acesso COM COM padrão do solicitante</span><span class="sxs-lookup"><span data-stu-id="cf4d3-117">Setting Requester Default COM Access Check Permission</span></span>

<span data-ttu-id="cf4d3-118">Os solicitantes precisam estar cientes de que, quando o processo atua como um servidor (por exemplo, permitindo que os gravadores modifiquem o documento de componentes de backup), eles devem permitir chamadas de entrada de outros participantes do VSS, como gravadores ou o serviço VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-118">Requesters need to be aware that when their process acts as a server (for example, allowing writers to modify the Backup Components Document), they must allow incoming calls from other VSS participants, such as writers or the VSS service.</span></span>

<span data-ttu-id="cf4d3-119">No entanto, por padrão, um processo do Windows permitirá apenas clientes COM em execução na mesma sessão de logon (o SID próprio) ou em execução na conta sistema local.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-119">However, by default, a Windows process will allow only COM clients that are running under the same logon session (the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="cf4d3-120">Esse é um problema potencial porque esses padrões não são adequados para a infraestrutura do VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-120">This is a potential problem because these defaults are not adequate for the VSS infrastructure.</span></span> <span data-ttu-id="cf4d3-121">Por exemplo, os gravadores podem ser executados como uma conta de usuário de "operador de backup" que não esteja na mesma sessão de logon que o processo do solicitante nem uma conta do sistema local.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-121">For example, writers might run as a "Backup Operator" user account that is neither in the same logon session as the requester process nor a Local System account.</span></span>

<span data-ttu-id="cf4d3-122">Para lidar com esse tipo de problema, cada processo de servidor COM pode exercer mais controle sobre se um cliente RPC ou COM tem permissão para executar um método COM implementado pelo servidor (um solicitante, nesse caso), usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir uma "permissão de verificação de acesso com" padrão de todo o processo.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-122">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method implemented by the server (a requester in this case) by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide "Default COM Access Check Permission".</span></span>

<span data-ttu-id="cf4d3-123">Os solicitantes podem fazer o seguinte explicitamente:</span><span class="sxs-lookup"><span data-stu-id="cf4d3-123">Requesters can explicitly do the following:</span></span>

-   <span data-ttu-id="cf4d3-124">Permitir que todos os processos acessem para chamar o processo do solicitante.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-124">Allow all processes access to call into the requester process.</span></span>

    <span data-ttu-id="cf4d3-125">Essa opção pode ser adequada para a grande maioria dos solicitantes e é usada por outros servidores COM — por exemplo, todos os serviços do Windows baseados em SVCHOST já estão usando essa opção, assim como todos os serviços COM+ por padrão.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-125">This option may be adequate for the vast majority of requesters, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="cf4d3-126">Permitir que todos os processos executem chamadas COM de entrada não é necessariamente uma vulnerabilidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-126">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="cf4d3-127">Um solicitante atuando como um servidor COM, como todos os outros servidores COM, sempre retém a opção de autorizar seus clientes em cada método COM implementado em seu processo.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-127">A requester acting as a COM server, like all other COM servers, always retains the option to authorize its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="cf4d3-128">Observe que os retornos de chamada COM internos implementados pelo VSS são protegidos por padrão.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-128">Note that internal COM callbacks implemented by VSS are secured by default.</span></span>

    <span data-ttu-id="cf4d3-129">Para permitir que todos os processos acessem COM um solicitante, você pode passar um descritor de segurança **nulo** como o primeiro parâmetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="cf4d3-129">To allow all processes COM access to a requester, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="cf4d3-130">(Observe que **CoInitializeSecurity** deve ser chamado no máximo uma vez para todo o processo.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="cf4d3-131">Consulte a documentação COM ou o MSDN para obter mais informações sobre as chamadas **CoInitializeSecurity** .)</span><span class="sxs-lookup"><span data-stu-id="cf4d3-131">Please see the COM documentation or MSDN for more information on **CoInitializeSecurity** calls.)</span></span>

    <span data-ttu-id="cf4d3-132">O exemplo de código a seguir mostra como um solicitante deve chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) no Windows 8 e no windows Server 2012 e posterior para ser compatível com o VSS para compartilhamentos de arquivos remotos (RVSS):</span><span class="sxs-lookup"><span data-stu-id="cf4d3-132">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 8 and Windows Server 2012 and later, in order to be compatible with VSS for remote file shares (RVSS):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="cf4d3-133">Ao definir explicitamente a segurança de nível COM de um solicitante com [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cf4d3-133">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="cf4d3-134">Defina o nível de autenticação para pelo menos a **integridade de pkt do \_ nível de \_ autenticação \_ \_ \_ RPC C**.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**.</span></span> <span data-ttu-id="cf4d3-135">Para obter mais segurança, considere usar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C**.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="cf4d3-136">Defina o nível de representação para a representação do **nível de imp do RPC \_ \_ \_ \_ C**.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IMPERSONATE**.</span></span>
    -   <span data-ttu-id="cf4d3-137">Defina os recursos de segurança de encobrimento como **\_ estático EOAC**.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-137">Set the cloaking security capabilities to **EOAC\_STATIC**.</span></span> <span data-ttu-id="cf4d3-138">Para obter mais informações sobre a segurança de encobrimento, consulte [encobrindo](../com/cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="cf4d3-138">For more information about cloaking security, see [Cloaking](../com/cloaking.md).</span></span>

    <span data-ttu-id="cf4d3-139">O exemplo de código a seguir mostra como um solicitante deve chamar [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) no Windows 7 e no windows Server 2008 R2 e versões anteriores (ou no Windows 8 e no windows Server 2012 e posteriores, se a compatibilidade do RVSS não for necessária):</span><span class="sxs-lookup"><span data-stu-id="cf4d3-139">The following code example shows how a requester should call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) in Windows 7 and Windows Server 2008 R2 and earlier (or in Windows 8 and Windows Server 2012 and later, if RVSS compatibility is not needed):</span></span>

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    <span data-ttu-id="cf4d3-140">Ao definir explicitamente a segurança de nível COM de um solicitante com [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cf4d3-140">When explicitly setting a requester's COM level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="cf4d3-141">Defina o nível de autenticação para pelo menos o **RPC \_ C \_ Authn \_ nível \_ Connect**.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-141">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span> <span data-ttu-id="cf4d3-142">Para obter mais segurança, considere usar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C**.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-142">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>
    -   <span data-ttu-id="cf4d3-143">Defina o nível de representação para o **nível de imp do RPC \_ C \_ \_ \_** , a menos que o processo do solicitante precise permitir a representação para chamadas RPC ou com específicas que não estejam relacionadas ao VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-143">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the requester process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="cf4d3-144">Permitir que somente processos especificados acessem para chamar o processo do solicitante.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-144">Allow only specified processes access to call into the requester process.</span></span>

    <span data-ttu-id="cf4d3-145">Um servidor COM (como um solicitante) que está chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) com um descritor de segurança não **nulo** como o primeiro parâmetro pode usar o descritor para se configurar para aceitar chamadas de entrada somente de usuários que pertencem a um conjunto específico de contas.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-145">A COM server (such as a requester) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor as the first parameter can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="cf4d3-146">Um solicitante deve garantir que clientes COM em execução em usuários válidos estejam autorizados a chamar seu processo.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-146">A requester must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="cf4d3-147">Um solicitante que especifica um descritor de segurança no primeiro parâmetro deve permitir que os seguintes usuários executem chamadas de entrada no processo do solicitante:</span><span class="sxs-lookup"><span data-stu-id="cf4d3-147">A requester that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="cf4d3-148">Sistema Local</span><span class="sxs-lookup"><span data-stu-id="cf4d3-148">Local System</span></span>
    -   <span data-ttu-id="cf4d3-149">Serviço Local</span><span class="sxs-lookup"><span data-stu-id="cf4d3-149">Local Service</span></span>

        <span data-ttu-id="cf4d3-150">**Windows XP:** Não há suporte para esse valor até o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-150">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="cf4d3-151">Serviço de Rede</span><span class="sxs-lookup"><span data-stu-id="cf4d3-151">Network Service</span></span>

        <span data-ttu-id="cf4d3-152">**Windows XP:** Não há suporte para esse valor até o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-152">**Windows XP:** This value is not supported until Windows Server 2003.</span></span>

    -   <span data-ttu-id="cf4d3-153">Membros do grupo Administradores local</span><span class="sxs-lookup"><span data-stu-id="cf4d3-153">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="cf4d3-154">Membros do grupo operadores de backup local</span><span class="sxs-lookup"><span data-stu-id="cf4d3-154">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="cf4d3-155">Usuários especiais que são especificados no local do registro abaixo, com "1" como seu valor de REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="cf4d3-155">Special users that are specified in the registry location below, with "1" as their REG\_DWORD value</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a><span data-ttu-id="cf4d3-156">Controlando explicitamente o acesso de conta de usuário a um solicitante</span><span class="sxs-lookup"><span data-stu-id="cf4d3-156">Explicitly Controlling User Account Access to a Requester</span></span>

<span data-ttu-id="cf4d3-157">Há casos em que restringir o acesso a um solicitante para processos em execução como sistema local ou nos grupos Administradores locais ou operadores de backup locais pode ser muito restritivo.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-157">There are cases where restricting access to a requester to processes running as Local System, or under the local Administrators or local Backup Operators groups, may be too restrictive.</span></span>

<span data-ttu-id="cf4d3-158">Por exemplo, um processo de solicitante especificado pode, normalmente, não precisar ser executado em uma conta de administrador ou de operador de backup.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-158">For example, a specified requester process might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="cf4d3-159">Por motivos de segurança, seria melhor não promover artificialmente os privilégios de processos para dar suporte ao VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-159">For security reasons, it would be best not to artificially promote the processes privileges to support VSS.</span></span>

<span data-ttu-id="cf4d3-160">Nesses casos, a chave de registro **HKEY \_ \_ local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** deve ser modificada para instruir o VSS de que um usuário especificado é seguro para executar um solicitante VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-160">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS requester.</span></span>

<span data-ttu-id="cf4d3-161">Sob essa chave, você deve criar uma subchave que tenha o mesmo nome que a conta que terá acesso concedido ou negado.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-161">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="cf4d3-162">Essa subchave deve ser definida como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-162">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="cf4d3-163">Valor</span><span class="sxs-lookup"><span data-stu-id="cf4d3-163">Value</span></span> | <span data-ttu-id="cf4d3-164">Significado</span><span class="sxs-lookup"><span data-stu-id="cf4d3-164">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="cf4d3-165">0</span><span class="sxs-lookup"><span data-stu-id="cf4d3-165">0</span></span>     | <span data-ttu-id="cf4d3-166">Negue ao usuário acesso ao seu gravador e solicitante.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-166">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="cf4d3-167">1</span><span class="sxs-lookup"><span data-stu-id="cf4d3-167">1</span></span>     | <span data-ttu-id="cf4d3-168">Conceda ao usuário acesso ao seu gravador.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-168">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="cf4d3-169">2</span><span class="sxs-lookup"><span data-stu-id="cf4d3-169">2</span></span>     | <span data-ttu-id="cf4d3-170">Conceda ao usuário acesso ao solicitante.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-170">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="cf4d3-171">3</span><span class="sxs-lookup"><span data-stu-id="cf4d3-171">3</span></span>     | <span data-ttu-id="cf4d3-172">Conceda ao usuário acesso ao seu gravador e solicitante.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-172">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="cf4d3-173">O exemplo a seguir concede acesso à conta "mydomain \\ myuser":</span><span class="sxs-lookup"><span data-stu-id="cf4d3-173">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="cf4d3-174">Esse mecanismo também pode ser usado para restringir explicitamente um usuário permitido da execução de um solicitante VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-174">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS requester.</span></span> <span data-ttu-id="cf4d3-175">O exemplo a seguir restringirá o acesso da conta "administrador do ThatDomain \\ ":</span><span class="sxs-lookup"><span data-stu-id="cf4d3-175">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="cf4d3-176">O administrador do ThatDomain do usuário \\ não poderá executar um solicitante do VSS.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-176">The user ThatDomain\\Administrator would not be able to run a VSS requester.</span></span>

## <a name="performing-a-file-backup-of-the-system-state"></a><span data-ttu-id="cf4d3-177">Executando um backup de arquivo do estado do sistema</span><span class="sxs-lookup"><span data-stu-id="cf4d3-177">Performing a File Backup of the System State</span></span>

<span data-ttu-id="cf4d3-178">Se um solicitante executar o backup de estado do sistema fazendo backup de arquivos individuais em vez de usar uma imagem de volume para o backup, ele deverá chamar as funções [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) para enumerar links físicos em arquivos localizados nos seguintes diretórios:</span><span class="sxs-lookup"><span data-stu-id="cf4d3-178">If a requester performs system-state backup by backing up individual files instead of using a volume image for the backup, it must call the [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions to enumerate hard links on files that are located in the following directories:</span></span>

-   <span data-ttu-id="cf4d3-179">Perftrack do Windows \\ System32 \\ WDI </span><span class="sxs-lookup"><span data-stu-id="cf4d3-179">Windows\\system32\\WDI\\perftrack</span></span>\\\\
-   <span data-ttu-id="cf4d3-180">WINSXS do Windows </span><span class="sxs-lookup"><span data-stu-id="cf4d3-180">Windows\\WINSXS</span></span>\\\\

<span data-ttu-id="cf4d3-181">Esses diretórios só podem ser acessados por membros do grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-181">These directories can only be accessed by members of the Administrators group.</span></span> <span data-ttu-id="cf4d3-182">Por esse motivo, esse solicitante deve ser executado na conta do sistema ou em uma conta de usuário que seja membro do grupo Administradores.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-182">For this reason, such a requester must run under the system account or a user account that is a member of the Administrators group.</span></span>

<span data-ttu-id="cf4d3-183">**Windows XP e Windows Server 2003:** As funções [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) e [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) não têm suporte até o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cf4d3-183">**Windows XP and Windows Server 2003:** The [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) and [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) functions are not supported until Windows Vista and Windows Server 2008.</span></span>

 

 
