---
description: O WMI usa um descritor de segurança padrão do Windows para controlar o acesso aos namespaces do WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Acesso a namespaces WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922602"
---
# <a name="access-to-wmi-namespaces"></a><span data-ttu-id="b1590-103">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-103">Access to WMI Namespaces</span></span>

<span data-ttu-id="b1590-104">O WMI usa um *descritor de segurança* padrão do Windows para controlar o acesso aos namespaces do WMI.</span><span class="sxs-lookup"><span data-stu-id="b1590-104">WMI uses a standard Windows *security descriptor* to control access to WMI namespaces.</span></span> <span data-ttu-id="b1590-105">Quando você se conecta ao WMI, por meio do moniker "winmgmts" do WMI ou de uma chamada para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) ou [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), você se conecta a um namespace específico.</span><span class="sxs-lookup"><span data-stu-id="b1590-105">When you connect to WMI, either through the WMI "winmgmts" moniker or a call to [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) or [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md), you connect to a specific namespace.</span></span>

<span data-ttu-id="b1590-106">As informações a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="b1590-106">The following information is discussed in this topic:</span></span>

-   [<span data-ttu-id="b1590-107">Segurança do namespace WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-107">WMI Namespace Security</span></span>](#wmi-namespace-security)
-   [<span data-ttu-id="b1590-108">Auditoria de namespace do WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-108">WMI Namespace Auditing</span></span>](#wmi-namespace-auditing)
-   [<span data-ttu-id="b1590-109">Tipos de eventos de namespace</span><span class="sxs-lookup"><span data-stu-id="b1590-109">Types of Namespace Events</span></span>](#types-of-namespace-events)
-   [<span data-ttu-id="b1590-110">Configurações de acesso de namespace</span><span class="sxs-lookup"><span data-stu-id="b1590-110">Namespace Access Settings</span></span>](#namespace-access-settings)
-   [<span data-ttu-id="b1590-111">Permissões padrão em namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-111">Default Permissions on WMI Namespaces</span></span>](#default-permissions-on-wmi-namespaces)
-   [<span data-ttu-id="b1590-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1590-112">Related topics</span></span>](#related-topics)

## <a name="wmi-namespace-security"></a><span data-ttu-id="b1590-113">Segurança do namespace WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-113">WMI Namespace Security</span></span>

<span data-ttu-id="b1590-114">O WMI mantém a segurança do namespace comparando o [*token de acesso*](/windows/desktop/SecGloss/a-gly) do usuário que se conecta ao namespace com o [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) do namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-114">WMI maintains namespace security by comparing the [*access token*](/windows/desktop/SecGloss/a-gly) of the user connecting to the namespace with the [*security descriptor*](/windows/desktop/SecGloss/s-gly) of the namespace.</span></span> <span data-ttu-id="b1590-115">Para obter mais informações sobre a segurança do Windows, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-115">For more information about Windows security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="b1590-116">Lembre-se de que, a partir do Windows Vista, o [UAC (controle de conta de usuário)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) afeta o acesso aos dados do WMI e o que pode ser configurado com o [*controle WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-116">Be aware that, starting with Windows Vista, [User Account Control (UAC)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="b1590-117">Para obter mais informações, consulte [permissões padrão em namespaces do WMI](#default-permissions-on-wmi-namespaces) e [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-117">For more information, see [Default Permissions on WMI Namespaces](#default-permissions-on-wmi-namespaces) and [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="b1590-118">O acesso aos namespaces do WMI também é afetado quando a conexão é de um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="b1590-118">Access to WMI namespaces is also affected when the connection is from a remote computer.</span></span> <span data-ttu-id="b1590-119">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md), [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md)e [conectando por meio do firewall do Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span><span class="sxs-lookup"><span data-stu-id="b1590-119">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md), [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md), and [Connecting Through Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).</span></span>

<span data-ttu-id="b1590-120">Os provedores devem contar com a configuração de representação para a conexão para determinar se o script do cliente ou o aplicativo deve receber dados.</span><span class="sxs-lookup"><span data-stu-id="b1590-120">Providers must rely on the impersonation setting for the connection to determine if the client script or application should receive data.</span></span> <span data-ttu-id="b1590-121">Para obter mais informações sobre scripts e aplicativos cliente, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-121">For more information about script and client applications, see [Setting Client Application Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="b1590-122">Para obter mais informações sobre a representação do [*provedor*](gloss-p.md) , consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-122">For more information about [*provider*](gloss-p.md) impersonation, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

## <a name="wmi-namespace-auditing"></a><span data-ttu-id="b1590-123">Auditoria de namespace do WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-123">WMI Namespace Auditing</span></span>

<span data-ttu-id="b1590-124">O WMI usa a [*SACL (listas de controle de acesso) do sistema*](/windows/desktop/SecGloss/s-gly) de namespace para auditar a atividade de namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-124">WMI uses the namespace [*System access control lists (SACL)*](/windows/desktop/SecGloss/s-gly) to audit namespace activity.</span></span> <span data-ttu-id="b1590-125">Para habilitar a auditoria de namespaces do WMI, use a guia **segurança** no [*controle WMI*](gloss-w.md) para alterar as configurações de auditoria para o namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-125">To enable auditing of WMI namespaces, use the **Security** tab on the [*WMI Control*](gloss-w.md) to change the auditing settings for the namespace.</span></span>

<span data-ttu-id="b1590-126">A auditoria não é habilitada durante a instalação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b1590-126">Auditing is not enabled during the installation of the operating system.</span></span> <span data-ttu-id="b1590-127">Para habilitar a auditoria, clique na guia **auditoria** na janela **segurança** padrão.</span><span class="sxs-lookup"><span data-stu-id="b1590-127">To enable auditing, click the **Auditing** tab in the standard **Security** window.</span></span> <span data-ttu-id="b1590-128">Em seguida, você pode adicionar uma entrada de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b1590-128">Then you can add an auditing entry.</span></span>

<span data-ttu-id="b1590-129">Política de Grupo para o computador local deve ser definido para permitir a auditoria.</span><span class="sxs-lookup"><span data-stu-id="b1590-129">Group Policy for the local computer must be set to allow auditing.</span></span> <span data-ttu-id="b1590-130">Você pode habilitar a auditoria executando o snap-in do MMC gpedit. msc e definindo o **acesso a objetos de auditoria** em configuração do **computador** configurações do Windows configurações de  >    >  **segurança**  >  **políticas locais**  >  **política de auditoria**.</span><span class="sxs-lookup"><span data-stu-id="b1590-130">You can enable auditing by running the Gpedit.msc MMC snap-in and setting **Audit Object Access** under **Computer Configuration** > **Windows Settings** > **Security Settings** > **Local Policies** > **Audit Policy**.</span></span>

<span data-ttu-id="b1590-131">Uma entrada de auditoria edita a SACL do namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-131">An auditing entry edits the SACL of the namespace.</span></span> <span data-ttu-id="b1590-132">Quando você adiciona uma entrada de auditoria, ela é um usuário, grupo, computador ou entidade de segurança interna.</span><span class="sxs-lookup"><span data-stu-id="b1590-132">When you add an auditing entry, it is either a user, group, computer, or built-in security principal.</span></span> <span data-ttu-id="b1590-133">Depois de adicionar a entrada, você pode definir as operações de acesso que resultam em eventos de log de segurança.</span><span class="sxs-lookup"><span data-stu-id="b1590-133">After adding the entry, you can set the access operations that result in Security Log events.</span></span> <span data-ttu-id="b1590-134">Por exemplo, para os usuários autenticados do grupo, você pode clicar em executar métodos.</span><span class="sxs-lookup"><span data-stu-id="b1590-134">For example, for the group Authenticated Users, you can click Execute Methods.</span></span> <span data-ttu-id="b1590-135">Essa configuração resulta em eventos de log de segurança sempre que um membro do grupo usuários autenticados executa um método nesse namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-135">This setting results in Security Log events whenever a member of the Authenticated Users group executes a method in that namespace.</span></span> <span data-ttu-id="b1590-136">A ID do evento para eventos WMI é 4662.</span><span class="sxs-lookup"><span data-stu-id="b1590-136">The Event ID for WMI events is 4662.</span></span>

<span data-ttu-id="b1590-137">Sua conta deve estar no grupo Administradores e em execução com privilégios elevados para alterar as configurações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b1590-137">Your account must be in the Administrators group and running under elevated privilege to change the auditing settings.</span></span> <span data-ttu-id="b1590-138">A conta interna de administrador também pode alterar a segurança ou a auditoria de um namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-138">The built-in Administrator account can also change the security or auditing for a namespace.</span></span> <span data-ttu-id="b1590-139">Para obter mais informações sobre como executar no modo elevado, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-139">For more information about running in elevated mode, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="b1590-140">A auditoria WMI gera eventos de êxito ou falha para tentativas de acessar namespaces do WMI.</span><span class="sxs-lookup"><span data-stu-id="b1590-140">WMI auditing generates success or failure events for attempts to access WMI namespaces.</span></span> <span data-ttu-id="b1590-141">O serviço não audita o êxito ou a falha das operações do provedor.</span><span class="sxs-lookup"><span data-stu-id="b1590-141">The service does not audit the success or failure of provider operations.</span></span> <span data-ttu-id="b1590-142">Por exemplo, quando um script se conecta ao WMI e a um namespace, ele pode falhar porque a conta sob a qual o script está sendo executado não tem acesso a esse namespace ou pode tentar uma operação, como editar a DACL, que não é concedida.</span><span class="sxs-lookup"><span data-stu-id="b1590-142">For example, when a script connects to WMI and a namespace, it may fail because the account under which the script is running does not have access to that the namespace or may attempt an operation, such as editing the DACL, that is not granted.</span></span>

<span data-ttu-id="b1590-143">Se você estiver executando sob uma conta no grupo Administradores, poderá exibir os eventos de auditoria de namespace na interface do usuário do **Visualizador de eventos** .</span><span class="sxs-lookup"><span data-stu-id="b1590-143">If you are running under an account in the Administrators group, you can view the namespace auditing events in the **Event Viewer** user interface.</span></span>

## <a name="types-of-namespace-events"></a><span data-ttu-id="b1590-144">Tipos de eventos de namespace</span><span class="sxs-lookup"><span data-stu-id="b1590-144">Types of Namespace Events</span></span>

<span data-ttu-id="b1590-145">O WMI rastreia os seguintes tipos de eventos no log de eventos de segurança:</span><span class="sxs-lookup"><span data-stu-id="b1590-145">WMI traces the following types of events in the Security Event Log:</span></span>

-   <span data-ttu-id="b1590-146">Êxito na auditoria</span><span class="sxs-lookup"><span data-stu-id="b1590-146">Audit Success</span></span>

    <span data-ttu-id="b1590-147">A operação deve concluir com êxito duas etapas para um êxito de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b1590-147">The operation must successfully complete two steps for an Audit Success.</span></span> <span data-ttu-id="b1590-148">Primeiro, o WMI concede acesso ao aplicativo cliente ou script com base no SID do cliente e na DACL do namespace.</span><span class="sxs-lookup"><span data-stu-id="b1590-148">First, WMI grants access to the client application or script based on the client SID and the namespace DACL.</span></span> <span data-ttu-id="b1590-149">Em segundo lugar, a operação solicitada corresponde aos direitos de acesso na SACL de namespace para esse usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="b1590-149">Second, the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

-   <span data-ttu-id="b1590-150">Falha de auditoria</span><span class="sxs-lookup"><span data-stu-id="b1590-150">Audit Failure</span></span>

    <span data-ttu-id="b1590-151">O WMI nega o acesso ao namespace, mas a operação solicitada corresponde aos direitos de acesso na SACL de namespace para esse usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="b1590-151">WMI denies access to the namespace, but the requested operation matches the access rights in the namespace SACL for that user or group.</span></span>

## <a name="namespace-access-settings"></a><span data-ttu-id="b1590-152">Configurações de acesso de namespace</span><span class="sxs-lookup"><span data-stu-id="b1590-152">Namespace Access Settings</span></span>

<span data-ttu-id="b1590-153">Você pode exibir os direitos de acesso do namespace para várias contas no controle WMI.</span><span class="sxs-lookup"><span data-stu-id="b1590-153">You can view the namespace access rights for various accounts on the WMI Control.</span></span> <span data-ttu-id="b1590-154">Essas constantes são descritas em [**constantes direitos de acesso de namespace**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-154">These constants are described in [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span> <span data-ttu-id="b1590-155">Você pode alterar o acesso a um namespace do WMI usando o controle WMI ou programaticamente.</span><span class="sxs-lookup"><span data-stu-id="b1590-155">You can change the access to a WMI namespace using the WMI Control or programmatically.</span></span> <span data-ttu-id="b1590-156">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-156">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="b1590-157">As auditorias do WMI são alteradas em todas as permissões de acesso listadas na lista a seguir, exceto para a permissão habilitar remotamente.</span><span class="sxs-lookup"><span data-stu-id="b1590-157">WMI audits changes in all of the access permissions listed in the following list except for the Remote Enable permission.</span></span> <span data-ttu-id="b1590-158">As alterações são registradas como êxito de auditoria ou falha correspondentes à permissão Editar segurança.</span><span class="sxs-lookup"><span data-stu-id="b1590-158">The changes are logged as audit success or failure corresponding to the Edit Security permission.</span></span>

<dl> <dt>

<span data-ttu-id="b1590-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Métodos de execução</span><span class="sxs-lookup"><span data-stu-id="b1590-159"><span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Execute Methods</span></span>
</dt> <dd>

<span data-ttu-id="b1590-160">Permite que o usuário execute métodos definidos em classes WMI.</span><span class="sxs-lookup"><span data-stu-id="b1590-160">Permits the user to execute methods defined on WMI classes.</span></span> <span data-ttu-id="b1590-161">Corresponde à constante de permissão de acesso de **\_ \_ execução do método WBEM** .</span><span class="sxs-lookup"><span data-stu-id="b1590-161">Corresponds to the **WBEM\_METHOD\_EXECUTE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Gravação completa</span><span class="sxs-lookup"><span data-stu-id="b1590-162"><span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Full Write</span></span>
</dt> <dd>

<span data-ttu-id="b1590-163">Permite o acesso completo de leitura, gravação e exclusão a classes WMI e instâncias de classe, tanto estática quanto dinâmica.</span><span class="sxs-lookup"><span data-stu-id="b1590-163">Permits full read, write, and delete access to WMI classes and class instances, both static and dynamic.</span></span> <span data-ttu-id="b1590-164">Corresponde à constante de permissão de acesso do **\_ \_ \_ representante de gravação completa do WBEM** .</span><span class="sxs-lookup"><span data-stu-id="b1590-164">Corresponds to the **WBEM\_FULL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Gravação parcial</span><span class="sxs-lookup"><span data-stu-id="b1590-165"><span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Partial Write</span></span>
</dt> <dd>

<span data-ttu-id="b1590-166">Permite o acesso de gravação a instâncias de classe WMI estáticas.</span><span class="sxs-lookup"><span data-stu-id="b1590-166">Permits write access to static WMI class instances.</span></span> <span data-ttu-id="b1590-167">Corresponde à constante de permissão de acesso do **\_ \_ \_ representante de gravação parcial do WBEM** .</span><span class="sxs-lookup"><span data-stu-id="b1590-167">Corresponds to the **WBEM\_PARTIAL\_WRITE\_REP** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Gravação do provedor</span><span class="sxs-lookup"><span data-stu-id="b1590-168"><span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Provider Write</span></span>
</dt> <dd>

<span data-ttu-id="b1590-169">Permite o acesso de gravação a instâncias de classe WMI dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="b1590-169">Permits write access to dynamic WMI class instances.</span></span> <span data-ttu-id="b1590-170">Corresponde à constante de permissão de acesso do **\_ \_ provedor de gravação WBEM** .</span><span class="sxs-lookup"><span data-stu-id="b1590-170">Corresponds to the **WBEM\_WRITE\_PROVIDER** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Habilitar conta</span><span class="sxs-lookup"><span data-stu-id="b1590-171"><span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Enable Account</span></span>
</dt> <dd>

<span data-ttu-id="b1590-172">Permite acesso de leitura a instâncias de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="b1590-172">Permits read access to WMI class instances.</span></span> <span data-ttu-id="b1590-173">Corresponde à constante de permissão **\_ habilitar** acesso do WBEM.</span><span class="sxs-lookup"><span data-stu-id="b1590-173">Corresponds to the **WBEM\_ENABLE** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Habilitação remota</span><span class="sxs-lookup"><span data-stu-id="b1590-174"><span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Remote Enable</span></span>
</dt> <dd>

<span data-ttu-id="b1590-175">Permite o acesso ao namespace por computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="b1590-175">Permits access to the namespace by remote computers.</span></span> <span data-ttu-id="b1590-176">Corresponde à constante de permissão de acesso de acesso **\_ \_ remoto WBEM** .</span><span class="sxs-lookup"><span data-stu-id="b1590-176">Corresponds to the **WBEM\_REMOTE\_ACCESS** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Ler segurança</span><span class="sxs-lookup"><span data-stu-id="b1590-177"><span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Read Security</span></span>
</dt> <dd>

<span data-ttu-id="b1590-178">Permite o acesso somente leitura às configurações de DACL.</span><span class="sxs-lookup"><span data-stu-id="b1590-178">Permits read-only access to DACL settings.</span></span> <span data-ttu-id="b1590-179">Corresponde à constante de permissão de acesso do **\_ controle de leitura** .</span><span class="sxs-lookup"><span data-stu-id="b1590-179">Corresponds to the **READ\_CONTROL** access permission constant.</span></span>

</dd> <dt>

<span data-ttu-id="b1590-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Editar segurança</span><span class="sxs-lookup"><span data-stu-id="b1590-180"><span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Edit Security</span></span>
</dt> <dd>

<span data-ttu-id="b1590-181">Permite o acesso de gravação às configurações de DACL.</span><span class="sxs-lookup"><span data-stu-id="b1590-181">Permits write access to DACL settings.</span></span> <span data-ttu-id="b1590-182">Corresponde à constante de permissão gravar acesso de **\_ DAC** .</span><span class="sxs-lookup"><span data-stu-id="b1590-182">Corresponds to the **WRITE\_DAC** access permission constant.</span></span>

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a><span data-ttu-id="b1590-183">Permissões padrão em namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-183">Default Permissions on WMI Namespaces</span></span>

<span data-ttu-id="b1590-184">Os grupos de segurança padrão são:</span><span class="sxs-lookup"><span data-stu-id="b1590-184">The default security groups are:</span></span>

-   <span data-ttu-id="b1590-185">Usuários Autenticados</span><span class="sxs-lookup"><span data-stu-id="b1590-185">Authenticated Users</span></span>
-   <span data-ttu-id="b1590-186">LOCAL SERVICE</span><span class="sxs-lookup"><span data-stu-id="b1590-186">LOCAL SERVICE</span></span>
-   <span data-ttu-id="b1590-187">SERVIÇO DE REDE</span><span class="sxs-lookup"><span data-stu-id="b1590-187">NETWORK SERVICE</span></span>
-   <span data-ttu-id="b1590-188">Administradores (no computador local)</span><span class="sxs-lookup"><span data-stu-id="b1590-188">Administrators (on the local computer)</span></span>

<span data-ttu-id="b1590-189">As permissões de acesso padrão para os usuários autenticados, o serviço LOCAL e o serviço de rede são:</span><span class="sxs-lookup"><span data-stu-id="b1590-189">The default access permissions for the Authenticated Users, LOCAL SERVICE, and NETWORK SERVICE are:</span></span>

-   <span data-ttu-id="b1590-190">Executar métodos</span><span class="sxs-lookup"><span data-stu-id="b1590-190">Execute Methods</span></span>
-   <span data-ttu-id="b1590-191">Gravação completa</span><span class="sxs-lookup"><span data-stu-id="b1590-191">Full Write</span></span>
-   <span data-ttu-id="b1590-192">Habilitar conta</span><span class="sxs-lookup"><span data-stu-id="b1590-192">Enable Account</span></span>

<span data-ttu-id="b1590-193">As contas no grupo Administradores têm todos os direitos disponíveis, incluindo a edição de descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="b1590-193">Accounts in the Administrators group have all rights available to them, including editing security descriptors.</span></span> <span data-ttu-id="b1590-194">No entanto, devido ao UAC (controle de conta de usuário), o controle WMI ou o script deve estar sendo executado com segurança elevada.</span><span class="sxs-lookup"><span data-stu-id="b1590-194">However, because of User Account Control (UAC), the WMI Control or the script must be running at elevated security.</span></span> <span data-ttu-id="b1590-195">Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-195">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

<span data-ttu-id="b1590-196">Às vezes, um script ou aplicativo deve habilitar um privilégio de administrador, como **SeSecurityPrivilege**, para realizar uma operação.</span><span class="sxs-lookup"><span data-stu-id="b1590-196">Sometimes a script or application must enable an administrator privilege, such as **SeSecurityPrivilege**, to carry out an operation.</span></span> <span data-ttu-id="b1590-197">Por exemplo, um script pode executar o método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) da classe [**de \_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) sem **SeSecurityPrivilege** e obter as informações de segurança na [*DACL (lista de controle de acesso discricionário)*](/windows/desktop/SecGloss/d-gly) do [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)do objeto da impressora.</span><span class="sxs-lookup"><span data-stu-id="b1590-197">For example, a script can execute the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class without **SeSecurityPrivilege** and get the security information in the [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) of the printer object [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="b1590-198">No entanto, as informações de SACL não são retornadas para o script, a menos que o privilégio **SeSecurityPrivilege** esteja disponível e habilitado para a conta.</span><span class="sxs-lookup"><span data-stu-id="b1590-198">However, the SACL information is not returned to the script unless the **SeSecurityPrivilege** privilege is available and enabled for the account.</span></span> <span data-ttu-id="b1590-199">Se a conta não tiver o privilégio disponível, ela não poderá ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="b1590-199">If the account does not have the privilege available, then it cannot be enabled.</span></span> <span data-ttu-id="b1590-200">Para obter mais informações, consulte [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="b1590-200">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1590-201">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1590-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1590-202">Sobre o WMI</span><span class="sxs-lookup"><span data-stu-id="b1590-202">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
