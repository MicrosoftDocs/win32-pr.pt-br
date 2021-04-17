---
description: A infraestrutura do VSS requer que os processos de gravação sejam capazes de funcionar como clientes COM e como servidores.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considerações de segurança para gravadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6f88243adbd62d928170a86ed57b91cbebe134
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770544"
---
# <a name="security-considerations-for-writers"></a><span data-ttu-id="88ebe-103">Considerações de segurança para gravadores</span><span class="sxs-lookup"><span data-stu-id="88ebe-103">Security Considerations for Writers</span></span>

<span data-ttu-id="88ebe-104">A infraestrutura do VSS requer que os processos de gravação sejam capazes de funcionar como clientes COM e como servidores.</span><span class="sxs-lookup"><span data-stu-id="88ebe-104">The VSS infrastructure requires writer processes to be able to function both as COM clients and as servers.</span></span>

<span data-ttu-id="88ebe-105">Ao atuar como servidores, gravadores VSS expõem interfaces COM (por exemplo, os manipuladores de eventos do VSS, como [**CVssWriter:: Onidentificate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) e recebem chamadas de entrada com de processos VSS (como solicitantes e o serviço VSS) ou chamadas RPC de processos que são externos ao VSS, geralmente quando esses processos geram eventos VSS (por exemplo, quando um solicitante chama [**IVssBackupComponents:**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)</span><span class="sxs-lookup"><span data-stu-id="88ebe-105">When acting as servers, VSS writers expose COM interfaces (for example, the VSS event handlers such as [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)) and receive incoming COM calls from VSS processes (such as requesters and the VSS service) or RPC calls from processes that are external to VSS, typically when these processes generate VSS events (for example, when a requester calls [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)).</span></span> <span data-ttu-id="88ebe-106">Portanto, um gravador VSS precisa gerenciar com segurança quais clientes COM são capazes de fazer chamadas COM de entrada em seu processo.</span><span class="sxs-lookup"><span data-stu-id="88ebe-106">Therefore, a VSS writer needs to securely manage which COM clients are able to make incoming COM calls into its process.</span></span>

<span data-ttu-id="88ebe-107">Da mesma forma, os gravadores VSS também podem atuar como clientes COM, fazendo chamadas COM de saída COM para os retornos de chamada fornecidos pela infraestrutura do VSS ou chamadas RPC para processos que são externos ao VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-107">Similarly, VSS writers may also act as COM clients, making outgoing COM calls to callbacks supplied by the VSS infrastructure or RPC calls to processes that are external to VSS.</span></span> <span data-ttu-id="88ebe-108">Esses retornos de chamada que são fornecidos por um aplicativo de backup ou pelo serviço VSS permitem que o gravador Execute tarefas como atualizar o documento de componentes de backup por meio da interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .</span><span class="sxs-lookup"><span data-stu-id="88ebe-108">These callbacks that are provided either by a backup application or by the VSS service allow the writer to perform tasks such as updating the Backup Components Document through the [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface.</span></span> <span data-ttu-id="88ebe-109">Portanto, as configurações de segurança do VSS devem permitir que os gravadores façam chamadas COM de saída em outros processos VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-109">Therefore, VSS security settings must allow writers to make outgoing COM calls into other VSS processes.</span></span>

<span data-ttu-id="88ebe-110">O mecanismo mais simples para gerenciar problemas de segurança do gravador envolve a seleção adequada da conta de usuário sob a qual ele é executado.</span><span class="sxs-lookup"><span data-stu-id="88ebe-110">The simplest mechanism for managing writer security issues involves the proper selection of the user account under which it runs.</span></span> <span data-ttu-id="88ebe-111">Normalmente, um gravador precisa ser executado sob um usuário que seja membro do grupo Administradores ou do grupo operadores de backup ou que ele precise ser executado como a conta sistema local.</span><span class="sxs-lookup"><span data-stu-id="88ebe-111">A writer typically needs to run under a user who is a member of either the Administrators group or the Backup Operators group, or it needs to run as the Local System account.</span></span>

<span data-ttu-id="88ebe-112">Por padrão, quando um gravador está agindo como um cliente COM, se ele não for executado nessas contas, qualquer chamada COM ele será rejeitada automaticamente com **E \_ ACCESSDENIED** sem até mesmo chegar à implementação do método com.</span><span class="sxs-lookup"><span data-stu-id="88ebe-112">By default, when a writer is acting as a COM client, if it does not run under these accounts, any COM call it makes is automatically rejected with **E\_ACCESSDENIED** without even getting to the COM method implementation.</span></span>

## <a name="disabling-com-exception-handling"></a><span data-ttu-id="88ebe-113">Desabilitando a manipulação de exceção COM</span><span class="sxs-lookup"><span data-stu-id="88ebe-113">Disabling COM Exception Handling</span></span>

<span data-ttu-id="88ebe-114">Ao desenvolver um gravador, defina o sinalizador COM COMGLB \_ exceção \_ não cercamento \_ manipular opções globais para desabilitar a manipulação de exceções com.</span><span class="sxs-lookup"><span data-stu-id="88ebe-114">When developing a writer, set the COM COMGLB\_EXCEPTION\_DONOT\_HANDLE global options flag to disable COM exception handling.</span></span> <span data-ttu-id="88ebe-115">É importante fazer isso porque a manipulação de exceção COM pode mascarar erros fatais em um aplicativo VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-115">It is important to do this because COM exception handling can mask fatal errors in a VSS application.</span></span> <span data-ttu-id="88ebe-116">O erro mascarado pode deixar o processo em um estado instável e imprevisível, o que pode levar a corrupções e travamentos.</span><span class="sxs-lookup"><span data-stu-id="88ebe-116">The error that is masked can leave the process in an unstable and unpredictable state, which can lead to corruptions and hangs.</span></span> <span data-ttu-id="88ebe-117">Para obter mais informações sobre esse sinalizador, consulte [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span><span class="sxs-lookup"><span data-stu-id="88ebe-117">For more information about this flag, see [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).</span></span>

## <a name="setting-writer-default-com-access-check-permission"></a><span data-ttu-id="88ebe-118">Definindo a permissão de verificação de acesso COM padrão do gravador</span><span class="sxs-lookup"><span data-stu-id="88ebe-118">Setting Writer Default COM Access Check Permission</span></span>

<span data-ttu-id="88ebe-119">Os gravadores precisam estar cientes de que, quando seus processos atuam como um servidor (por exemplo, para manipular eventos VSS), eles devem permitir chamadas de entrada de outros participantes do VSS, como solicitantes ou o serviço VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-119">Writers need to be aware that when their processes act as a server (for example, to handle VSS events), they must allow incoming calls from other VSS participants, such as requesters or the VSS service.</span></span>

<span data-ttu-id="88ebe-120">No entanto, por padrão, um processo permitirá apenas clientes COM que estão em execução na mesma sessão de logon, o SID próprio) ou em execução na conta sistema local.</span><span class="sxs-lookup"><span data-stu-id="88ebe-120">However, by default, a process will allow only COM clients that are running under the same logon session the SELF SID) or running under the Local System account.</span></span> <span data-ttu-id="88ebe-121">Esse é um problema potencial porque esses padrões não são suficientes para dar suporte à infraestrutura do VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-121">This is a potential problem because these defaults are not sufficient to support the VSS infrastructure.</span></span> <span data-ttu-id="88ebe-122">Por exemplo, os solicitantes podem ser executados como uma conta de usuário de "operador de backup" que não esteja na mesma sessão de logon que o processo do gravador nem em uma conta do sistema local.</span><span class="sxs-lookup"><span data-stu-id="88ebe-122">For example, requesters may run as a "Backup Operator" user account that is neither in the same logon session as the writer process nor a Local System account.</span></span>

<span data-ttu-id="88ebe-123">Para lidar com esse tipo de problema, cada processo de servidor COM pode exercer mais controle sobre se um cliente RPC ou COM tem permissão para executar um método COM no qual o servidor (um gravador, nesse caso) implementa, usando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir uma permissão de verificação de acesso com em todo o processo.</span><span class="sxs-lookup"><span data-stu-id="88ebe-123">To handle this type of problem, every COM server process can exercise further control over whether an RPC or COM client is allowed to perform a COM method the server (a writer in this case) implements by using [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to set a process-wide default COM access check permission.</span></span>

<span data-ttu-id="88ebe-124">Os gravadores podem fazer o seguinte explicitamente:</span><span class="sxs-lookup"><span data-stu-id="88ebe-124">Writers can explicitly do the following:</span></span>

-   <span data-ttu-id="88ebe-125">Permitir que todos os processos acessem para chamar o processo do gravador.</span><span class="sxs-lookup"><span data-stu-id="88ebe-125">Allow all processes access to call into the writer process.</span></span>

    <span data-ttu-id="88ebe-126">Essa opção pode ser adequada para muitos gravadores e é usada por outros servidores COM — por exemplo, todos os serviços do Windows baseados em SVCHOST já estão usando essa opção, assim como todos os serviços COM+ por padrão.</span><span class="sxs-lookup"><span data-stu-id="88ebe-126">This option may be adequate for many writers, and is used by other COM servers—for example, all SVCHOST-based Windows services are already using this option, as are all COM+ Services by default.</span></span>

    <span data-ttu-id="88ebe-127">Permitir que todos os processos executem chamadas COM de entrada não é necessariamente uma vulnerabilidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="88ebe-127">Allowing all processes to perform incoming COM calls is not necessarily a security weakness.</span></span> <span data-ttu-id="88ebe-128">Um gravador agindo como um servidor COM, como todos os outros servidores COM, sempre retém a opção de autorizar seus clientes em cada método COM implementado em seu processo.</span><span class="sxs-lookup"><span data-stu-id="88ebe-128">A writer acting as a COM server, like all other COM servers, always retains the option of authorizing its clients on every COM method implemented in its process.</span></span>

    <span data-ttu-id="88ebe-129">Para permitir que todos os processos COM acesso a um gravador, você pode passar um descritor de segurança **nulo** como o primeiro parâmetro de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="88ebe-129">To allow all processes COM access to a writer, you can pass a **NULL** security descriptor as the first parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="88ebe-130">(Observe que **CoInitializeSecurity** deve ser chamado no máximo uma vez para todo o processo.</span><span class="sxs-lookup"><span data-stu-id="88ebe-130">(Note that **CoInitializeSecurity** must be called at most once for the entire process.</span></span> <span data-ttu-id="88ebe-131">Consulte a documentação COM para obter mais detalhes sobre **CoInitializeSecurity**.)</span><span class="sxs-lookup"><span data-stu-id="88ebe-131">Please see the COM documentation for more details on **CoInitializeSecurity**.)</span></span>

    <span data-ttu-id="88ebe-132">Veja a seguir um exemplo de código que inclui uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span><span class="sxs-lookup"><span data-stu-id="88ebe-132">The following is a code example that includes a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):</span></span>

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    <span data-ttu-id="88ebe-133">Ao definir explicitamente a segurança de nível de COM de um gravador com [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="88ebe-133">When explicitly setting a writer's COM-level security with [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), you should do the following:</span></span>

    -   <span data-ttu-id="88ebe-134">Defina o nível de autenticação para pelo menos o **RPC \_ C \_ Authn \_ nível \_ Connect**.</span><span class="sxs-lookup"><span data-stu-id="88ebe-134">Set the authentication level to at least **RPC\_C\_AUTHN\_LEVEL\_CONNECT**.</span></span>

        <span data-ttu-id="88ebe-135">Para obter mais segurança, considere usar a **privacidade do PCT do \_ nível de \_ autenticação \_ \_ \_ RPC C**.</span><span class="sxs-lookup"><span data-stu-id="88ebe-135">For better security, consider using **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span>

    -   <span data-ttu-id="88ebe-136">Defina o nível de representação para o **nível de imp do RPC \_ C \_ \_ \_** , a menos que o processo do gravador precise permitir a representação de chamadas RPC ou com específicas que não estejam relacionadas ao VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-136">Set the impersonation level to **RPC\_C\_IMP\_LEVEL\_IDENTIFY** unless the writer process needs to allow impersonation for specific RPC or COM calls that are unrelated to VSS.</span></span>

-   <span data-ttu-id="88ebe-137">Permitir que somente processos especificados acessem para chamar o processo do gravador.</span><span class="sxs-lookup"><span data-stu-id="88ebe-137">Allow only specified processes access to call into the writer process.</span></span>

    <span data-ttu-id="88ebe-138">Um servidor COM (como um gravador) que está chamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) com um descritor de segurança não **nulo** pode usar o descritor para se configurar para aceitar chamadas de entrada somente de usuários que pertencem a um conjunto específico de contas.</span><span class="sxs-lookup"><span data-stu-id="88ebe-138">A COM server (such as a writer) that is calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) with a non-**NULL** security descriptor can use the descriptor to configure itself to accept incoming calls only from users that belong to a specific set of accounts.</span></span>

    <span data-ttu-id="88ebe-139">Um gravador deve garantir que clientes COM em execução em usuários válidos estejam autorizados a chamar seu processo.</span><span class="sxs-lookup"><span data-stu-id="88ebe-139">A writer must ensure that COM clients running under valid users are authorized to call into its process.</span></span> <span data-ttu-id="88ebe-140">Um gravador que especifica um descritor de segurança no primeiro parâmetro deve permitir que os seguintes usuários executem chamadas de entrada no processo do solicitante:</span><span class="sxs-lookup"><span data-stu-id="88ebe-140">A writer that specifies a Security Descriptor in the first parameter must allow the following users to perform incoming calls into the requester process:</span></span>

    -   <span data-ttu-id="88ebe-141">Sistema Local</span><span class="sxs-lookup"><span data-stu-id="88ebe-141">Local System</span></span>
    -   <span data-ttu-id="88ebe-142">Membros do grupo Administradores local</span><span class="sxs-lookup"><span data-stu-id="88ebe-142">Members of the local Administrators group</span></span>
    -   <span data-ttu-id="88ebe-143">Membros do grupo operadores de backup local</span><span class="sxs-lookup"><span data-stu-id="88ebe-143">Members of the local Backup Operators group</span></span>
    -   <span data-ttu-id="88ebe-144">A conta sob a qual o gravador está sendo executado</span><span class="sxs-lookup"><span data-stu-id="88ebe-144">The account under which the writer is running</span></span>

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a><span data-ttu-id="88ebe-145">Controlando explicitamente o acesso de conta de usuário a um gravador</span><span class="sxs-lookup"><span data-stu-id="88ebe-145">Explicitly Controlling User Account Access to a Writer</span></span>

<span data-ttu-id="88ebe-146">Há casos em que restringir o acesso a um gravador para processos em execução como sistema local ou nos grupos locais de administradores locais ou de operadores de backup locais pode ser muito restritivo.</span><span class="sxs-lookup"><span data-stu-id="88ebe-146">There are cases where restricting access to a writer to processes running as Local System, or under the local Administrators or local Backup Operators local groups, may be too restrictive.</span></span>

<span data-ttu-id="88ebe-147">Por exemplo, um processo de gravação (talvez um gravador que não seja de sistema) pode, normalmente, ser executado em uma conta de administrador ou de operador de backup.</span><span class="sxs-lookup"><span data-stu-id="88ebe-147">For example, a writer process (perhaps a third-party non-system writer) might not ordinarily need to be run under an Administrator or Backup Operator account.</span></span> <span data-ttu-id="88ebe-148">Por motivos de segurança, seria melhor não promover artificialmente os privilégios do processo para dar suporte ao VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-148">For security reasons, it would be best not to artificially promote the process's privileges to support VSS.</span></span>

<span data-ttu-id="88ebe-149">Nesses casos, a chave de registro **HKEY \_ local \_** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **VSS** \\ **VssAccessControl** deve ser modificada para instruir o VSS de que um usuário especificado é seguro para executar um gravador VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-149">In these cases, the **HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**VSS**\\**VssAccessControl** registry key must be modified to instruct VSS that a specified user is safe to run a VSS writer.</span></span>

<span data-ttu-id="88ebe-150">Sob essa chave, você deve criar uma subchave que tenha o mesmo nome que a conta que terá acesso concedido ou negado.</span><span class="sxs-lookup"><span data-stu-id="88ebe-150">Under this key, you must create a subkey that has the same name as the account that is to be granted or denied access.</span></span> <span data-ttu-id="88ebe-151">Essa subchave deve ser definida como um dos valores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="88ebe-151">This subkey must be set to one of the values in the following table.</span></span>

| <span data-ttu-id="88ebe-152">Valor</span><span class="sxs-lookup"><span data-stu-id="88ebe-152">Value</span></span> | <span data-ttu-id="88ebe-153">Significado</span><span class="sxs-lookup"><span data-stu-id="88ebe-153">Meaning</span></span>                                             |
|-------|-----------------------------------------------------|
| <span data-ttu-id="88ebe-154">0</span><span class="sxs-lookup"><span data-stu-id="88ebe-154">0</span></span>     | <span data-ttu-id="88ebe-155">Negue ao usuário acesso ao seu gravador e solicitante.</span><span class="sxs-lookup"><span data-stu-id="88ebe-155">Deny the user access to your writer and requester.</span></span>  |
| <span data-ttu-id="88ebe-156">1</span><span class="sxs-lookup"><span data-stu-id="88ebe-156">1</span></span>     | <span data-ttu-id="88ebe-157">Conceda ao usuário acesso ao seu gravador.</span><span class="sxs-lookup"><span data-stu-id="88ebe-157">Grant the user access to your writer.</span></span>               |
| <span data-ttu-id="88ebe-158">2</span><span class="sxs-lookup"><span data-stu-id="88ebe-158">2</span></span>     | <span data-ttu-id="88ebe-159">Conceda ao usuário acesso ao solicitante.</span><span class="sxs-lookup"><span data-stu-id="88ebe-159">Grant the user access to your requester.</span></span>            |
| <span data-ttu-id="88ebe-160">3</span><span class="sxs-lookup"><span data-stu-id="88ebe-160">3</span></span>     | <span data-ttu-id="88ebe-161">Conceda ao usuário acesso ao seu gravador e solicitante.</span><span class="sxs-lookup"><span data-stu-id="88ebe-161">Grant the user access to your writer and requester.</span></span> |



 

<span data-ttu-id="88ebe-162">O exemplo a seguir concede acesso à conta "mydomain \\ myuser":</span><span class="sxs-lookup"><span data-stu-id="88ebe-162">The following example grants access to the "MyDomain\\MyUser" account:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

<span data-ttu-id="88ebe-163">Esse mecanismo também pode ser usado para restringir explicitamente um usuário permitido da execução de um gravador VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-163">This mechanism can also be used to explicitly restrict an otherwise permitted user from running a VSS writer.</span></span> <span data-ttu-id="88ebe-164">O exemplo a seguir restringirá o acesso da conta "administrador do ThatDomain \\ ":</span><span class="sxs-lookup"><span data-stu-id="88ebe-164">The following example will restrict access from the "ThatDomain\\Administrator" account:</span></span>

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

<span data-ttu-id="88ebe-165">O administrador do ThatDomain do usuário \\ não poderá executar um gravador VSS.</span><span class="sxs-lookup"><span data-stu-id="88ebe-165">The user ThatDomain\\Administrator would not be able to run a VSS writer.</span></span>

 

 
