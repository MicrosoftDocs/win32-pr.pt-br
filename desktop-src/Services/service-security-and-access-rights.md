---
description: O modelo de segurança do Windows permite controlar o acesso ao SCM (Gerenciador de controle de serviço) e aos objetos de serviço.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Segurança do serviço e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769185"
---
# <a name="service-security-and-access-rights"></a><span data-ttu-id="87754-103">Segurança do serviço e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-103">Service Security and Access Rights</span></span>

<span data-ttu-id="87754-104">O modelo de segurança do Windows permite controlar o acesso ao SCM (Gerenciador de controle de serviço) e aos objetos de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="87754-105">As seções a seguir fornecem informações detalhadas:</span><span class="sxs-lookup"><span data-stu-id="87754-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="87754-106">Direitos de acesso para o Gerenciador de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="87754-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="87754-107">Direitos de acesso para um serviço</span><span class="sxs-lookup"><span data-stu-id="87754-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="87754-108">Direitos de acesso para o Gerenciador de controle de serviço</span><span class="sxs-lookup"><span data-stu-id="87754-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="87754-109">A seguir estão os direitos de acesso específicos para o SCM.</span><span class="sxs-lookup"><span data-stu-id="87754-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="87754-110">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-110">Access right</span></span>                                   | <span data-ttu-id="87754-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="87754-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87754-112">**Sc \_ MANAGER \_ All \_ Access** (0xF003F)</span><span class="sxs-lookup"><span data-stu-id="87754-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="87754-113">Inclui **\_ direitos padrão \_ necessários**, além de todos os direitos de acesso nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="87754-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="87754-114">**Sc \_ \_ \_ Serviço de criação do Gerenciador** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="87754-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="87754-115">Necessário para chamar a função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para criar um objeto de serviço e adicioná-lo ao banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87754-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="87754-116">**Sc \_ \_Conexão do Gerenciador** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="87754-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="87754-117">Necessário para se conectar ao Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="87754-118">**Sc \_ \_ \_ Serviço de enumeração do Gerenciador** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="87754-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="87754-119">Necessário para chamar a função [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) ou [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) para listar os serviços que estão no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87754-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="87754-120">Necessário para chamar a função [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para receber notificação quando qualquer serviço for criado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="87754-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="87754-121">**Sc \_ \_Bloqueio do Gerenciador** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="87754-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="87754-122">Necessário para chamar a função [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) para adquirir um bloqueio no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87754-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="87754-123">**Sc \_ MANAGER \_ Modify \_ \_ config boot** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="87754-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="87754-124">Necessário para chamar a função [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="87754-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="87754-125">**Sc \_ \_Status de \_ bloqueio \_ de consulta do Gerenciador** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="87754-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="87754-126">Necessário para chamar a função [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) para recuperar as informações de status de bloqueio do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="87754-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="87754-127">A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para o SCM.</span><span class="sxs-lookup"><span data-stu-id="87754-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="87754-128">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-128">Access right</span></span></th>
<th><span data-ttu-id="87754-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="87754-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87754-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="87754-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="87754-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="87754-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="87754-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="87754-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="87754-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87754-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87754-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="87754-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="87754-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="87754-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="87754-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="87754-144">Um processo com os direitos de acesso corretos pode abrir um identificador para o SCM que pode ser usado nas funções [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)e [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .</span><span class="sxs-lookup"><span data-stu-id="87754-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="87754-145">Somente processos com privilégios de administrador são capazes de abrir identificadores para o SCM que pode ser usado pelas funções [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) e [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .</span><span class="sxs-lookup"><span data-stu-id="87754-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="87754-146">O sistema cria o descritor de segurança para o SCM.</span><span class="sxs-lookup"><span data-stu-id="87754-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="87754-147">Para obter ou definir o descritor de segurança para o SCM, use as funções [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) com um identificador para o objeto SCManager.</span><span class="sxs-lookup"><span data-stu-id="87754-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="87754-148">**Windows Server 2003 e Windows XP:** Ao contrário da maioria dos outros objetos protegíveis, o descritor de segurança para o SCM não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="87754-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="87754-149">Esse comportamento foi alterado a partir do Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="87754-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="87754-150">Os direitos de acesso a seguir são concedidos.</span><span class="sxs-lookup"><span data-stu-id="87754-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="87754-151">Conta</span><span class="sxs-lookup"><span data-stu-id="87754-151">Account</span></span></th>
<th><span data-ttu-id="87754-152">Direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87754-153">Usuários autenticados remotamente</span><span class="sxs-lookup"><span data-stu-id="87754-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="87754-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="87754-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-155">Usuários autenticados locais (incluindo LocalService e NetworkService)</span><span class="sxs-lookup"><span data-stu-id="87754-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="87754-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="87754-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="87754-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="87754-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="87754-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="87754-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87754-160">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="87754-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="87754-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="87754-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="87754-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="87754-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87754-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="87754-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="87754-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="87754-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-166">Administradores</span><span class="sxs-lookup"><span data-stu-id="87754-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="87754-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="87754-168">Observe que os usuários remotos autenticados pela rede, mas não conectados interativamente, podem se conectar ao SCM, mas não executar operações que exigem outros direitos de acesso.</span><span class="sxs-lookup"><span data-stu-id="87754-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="87754-169">Para executar essas operações, o usuário deve fazer logon interativamente ou o serviço deve usar uma das contas de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="87754-170">**Windows Server 2003 e Windows XP:** Os usuários remotos autenticados recebem o serviço de enumeração SC Manager **\_ \_ Connect**, **sc \_ Manager \_ \_**, o **status de bloqueio de \_ \_ consulta SC \_ \_ Manager** e direitos padrão de acesso de **\_ \_ leitura de direitos** .</span><span class="sxs-lookup"><span data-stu-id="87754-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="87754-171">Esses direitos de acesso são restritos conforme descrito na tabela anterior a partir do Windows Server 2003 com SP1</span><span class="sxs-lookup"><span data-stu-id="87754-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="87754-172">Quando um processo usa a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para abrir um identificador para um banco de dados de serviços instalados, ele pode solicitar direitos de acesso.</span><span class="sxs-lookup"><span data-stu-id="87754-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="87754-173">O sistema executa uma verificação de segurança no descritor de segurança do SCM antes de conceder os direitos de acesso solicitados.</span><span class="sxs-lookup"><span data-stu-id="87754-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="87754-174">Direitos de acesso para um serviço</span><span class="sxs-lookup"><span data-stu-id="87754-174">Access Rights for a Service</span></span>

<span data-ttu-id="87754-175">A seguir estão os direitos de acesso específicos para um serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="87754-176">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-176">Access right</span></span>                                | <span data-ttu-id="87754-177">Descrição</span><span class="sxs-lookup"><span data-stu-id="87754-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87754-178">**Serviço \_ do Todos os \_ acessos** (0xF01FF)</span><span class="sxs-lookup"><span data-stu-id="87754-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="87754-179">Inclui **\_ direitos padrão \_ necessários** além de todos os direitos de acesso nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="87754-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="87754-180">**Serviço \_ do ALTERAR \_ configuração** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="87754-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="87754-181">Necessário para chamar a função [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) para alterar a configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="87754-182">Como isso concede ao chamador o direito de alterar o arquivo executável que o sistema executa, ele deve ser concedido somente aos administradores.</span><span class="sxs-lookup"><span data-stu-id="87754-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="87754-183">**Serviço \_ do ENUMERAr \_ dependentes** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="87754-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="87754-184">Necessário para chamar a função [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) para enumerar todos os serviços dependentes do serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="87754-185">**Serviço \_ do INTERROGAte** (0x0080)</span><span class="sxs-lookup"><span data-stu-id="87754-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="87754-186">Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para solicitar que o serviço relate seu status imediatamente.</span><span class="sxs-lookup"><span data-stu-id="87754-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="87754-187">**Serviço \_ do Pausar \_ continuar** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="87754-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="87754-188">Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para pausar ou continuar o serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="87754-189">**Serviço \_ do \_Configuração de consulta** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="87754-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="87754-190">Necessário para chamar as funções [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) para consultar a configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="87754-191">**Serviço \_ do \_Status da consulta** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="87754-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="87754-192">Necessário para chamar a função [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) ou [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) para perguntar ao Gerenciador de controle de serviço sobre o status do serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="87754-193">Necessário para chamar a função [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) para receber notificação quando um serviço altera o status.</span><span class="sxs-lookup"><span data-stu-id="87754-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="87754-194">**Serviço \_ do Iniciar** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="87754-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="87754-195">Necessário para chamar a função [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) para iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="87754-196">**Serviço \_ do PARAR** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="87754-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="87754-197">Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para interromper o serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="87754-198">**Serviço \_ do \_ \_ Controle definido pelo usuário**(0x0100)</span><span class="sxs-lookup"><span data-stu-id="87754-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="87754-199">Necessário para chamar a função [**chamada ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) para especificar um código de controle definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="87754-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="87754-200">A seguir estão os [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) para um serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="87754-201">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-201">Access right</span></span>                 | <span data-ttu-id="87754-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="87754-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87754-203">**\_segurança do sistema de acesso \_**</span><span class="sxs-lookup"><span data-stu-id="87754-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="87754-204">Necessário para chamar a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) ou [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para acessar a SACL.</span><span class="sxs-lookup"><span data-stu-id="87754-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="87754-205">A maneira apropriada de obter esse acesso é habilitar o [**privilégio**](/windows/desktop/SecAuthZ/privileges) **\_ \_ nome de segurança se** no token de acesso atual do chamador, abrir o identificador para acessar acesso à **\_ \_ segurança do sistema** e, em seguida, desabilitar o privilégio.</span><span class="sxs-lookup"><span data-stu-id="87754-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="87754-206">**Excluir**   (0x10000)</span><span class="sxs-lookup"><span data-stu-id="87754-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="87754-207">Necessário para chamar a função [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) para excluir o serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="87754-208">**Ler \_ CONTROL**  (0x20000)</span><span class="sxs-lookup"><span data-stu-id="87754-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="87754-209">Necessário para chamar a função [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) para consultar o descritor de segurança do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="87754-210">**Gravar \_ DAC**  (0x40000)</span><span class="sxs-lookup"><span data-stu-id="87754-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="87754-211">Necessário para chamar a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar o membro **DACL** do descritor de segurança do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="87754-212">**Gravar \_ PROPRIETÁRIO** (0x80000)</span><span class="sxs-lookup"><span data-stu-id="87754-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="87754-213">Necessário para chamar a função [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) para modificar o **proprietário** e os membros do **grupo** do descritor de segurança do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="87754-214">A seguir estão os [direitos de acesso genéricos](/windows/desktop/SecAuthZ/generic-access-rights) para um serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="87754-215">Direito de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-215">Access right</span></span></th>
<th><span data-ttu-id="87754-216">Descrição</span><span class="sxs-lookup"><span data-stu-id="87754-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87754-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="87754-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="87754-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="87754-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87754-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="87754-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="87754-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="87754-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="87754-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87754-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87754-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="87754-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="87754-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="87754-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="87754-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="87754-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="87754-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="87754-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="87754-232">O SCM cria um descritor de segurança do objeto de serviço quando o serviço é instalado pela função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="87754-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="87754-233">O descritor de segurança padrão de um objeto de serviço concede o acesso a seguir.</span><span class="sxs-lookup"><span data-stu-id="87754-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="87754-234">Conta</span><span class="sxs-lookup"><span data-stu-id="87754-234">Account</span></span></th>
<th><span data-ttu-id="87754-235">Direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="87754-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="87754-236">Usuários autenticados remotamente</span><span class="sxs-lookup"><span data-stu-id="87754-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="87754-237">Não concedido por padrão. <strong>Windows Server 2003 com SP1: SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="87754-238"><strong>Windows Server 2003 e Windows XP:</strong> Os direitos de acesso para usuários autenticados remotos são os mesmos para usuários autenticados locais.</span><span class="sxs-lookup"><span data-stu-id="87754-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-239">Usuários autenticados locais (incluindo LocalService e NetworkService)</span><span class="sxs-lookup"><span data-stu-id="87754-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="87754-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="87754-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="87754-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="87754-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87754-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="87754-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="87754-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="87754-246">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="87754-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="87754-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="87754-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="87754-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="87754-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="87754-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="87754-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="87754-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="87754-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="87754-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="87754-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="87754-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="87754-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="87754-256">Administradores</span><span class="sxs-lookup"><span data-stu-id="87754-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="87754-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="87754-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="87754-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="87754-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="87754-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="87754-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="87754-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="87754-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="87754-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="87754-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="87754-262">Para executar qualquer operação, o usuário deve fazer logon interativamente ou o serviço deve usar uma das contas de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="87754-263">Para obter ou definir o descritor de segurança para um objeto de serviço, use as funções [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) e [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="87754-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="87754-264">Para obter mais informações, consulte [modificando a DACL de um serviço](modifying-the-dacl-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="87754-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="87754-265">Quando um processo usa a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , o sistema verifica os direitos de acesso solicitados em relação ao descritor de segurança do objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="87754-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="87754-266">A concessão de determinados direitos de acesso a usuários não confiáveis (como **\_ \_ configuração de alteração de serviço** ou **\_ parada de serviço**) pode permitir que eles interfiram na execução do serviço e, possivelmente, permitir que eles executem aplicativos na conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="87754-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="87754-267">Quando a [**função EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) for chamada, se o chamador não tiver o direito de acesso de **status de \_ consulta \_ de serviço** a um serviço, o serviço será silenciosamente omitido da lista de serviços retornada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="87754-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 

