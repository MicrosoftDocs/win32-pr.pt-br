---
title: Controle de acesso (plataforma de filtragem do Windows)
description: Na WFP (Windows Filtering Platform), o serviço BFE (mecanismo de filtragem base) implementa o modelo de controle de acesso padrão do Windows com base em tokens de acesso e descritores de segurança.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104297846"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="ce40f-103">Controle de acesso (plataforma de filtragem do Windows)</span><span class="sxs-lookup"><span data-stu-id="ce40f-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="ce40f-104">Na WFP (Windows Filtering Platform), o serviço BFE (mecanismo de filtragem base) implementa o [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model) padrão do Windows com base em tokens de acesso e descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="ce40f-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="ce40f-105">Modelo de controle de acesso</span><span class="sxs-lookup"><span data-stu-id="ce40f-105">Access Control Model</span></span>

<span data-ttu-id="ce40f-106">Descritores de segurança podem ser especificados ao adicionar novos objetos WFP, como filtros e subcamadas.</span><span class="sxs-lookup"><span data-stu-id="ce40f-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="ce40f-107">Descritores de segurança são gerenciados usando as funções de gerenciamento de WFP **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0**, em que \* *\** _ significa o nome do objeto WFP.</span><span class="sxs-lookup"><span data-stu-id="ce40f-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="ce40f-108">Essas funções são semanticamente idênticas às funções Windows [_ *GetSecurityInfo* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) e [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="ce40f-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="ce40f-109">As funções **Fwpm \* SetSecurityInfo0** não podem ser chamadas de dentro de uma transação explícita.</span><span class="sxs-lookup"><span data-stu-id="ce40f-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="ce40f-110">As funções **Fwpm \* SetSecurityInfo0** só podem ser chamadas de dentro de uma sessão dinâmica se estiverem sendo usadas para gerenciar um objeto dinâmico criado dentro da mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="ce40f-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="ce40f-111">O descritor de segurança padrão para o mecanismo de filtro (o objeto do mecanismo raiz no diagrama abaixo) é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ce40f-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="ce40f-112">Conceda direitos de acesso **genéricos a \_ todos** (GA) ao grupo interno de administradores.</span><span class="sxs-lookup"><span data-stu-id="ce40f-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="ce40f-113">Conceda direitos de **acesso genérico de gravação \_** (GR) generic **\_ Write** (GW) genérico de **\_ execução** (GX) a operadores de configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="ce40f-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="ce40f-114">Conceda direitos de acesso **GRGWGX** aos seguintes SSIDs (identificadores de segurança de serviço): MPSSVC (firewall do Windows), NapAgent (agente de proteção de acesso à rede), policyagent (agente de diretiva IPSec), RPCSS (chamada de procedimento remoto) e WdiServiceHost (host do serviço de diagnóstico).</span><span class="sxs-lookup"><span data-stu-id="ce40f-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="ce40f-115">Grant **FWPM \_ ACTRL \_ Open** e **FWPM \_ ACTRL \_ classificar** para todos.</span><span class="sxs-lookup"><span data-stu-id="ce40f-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="ce40f-116">(Estes são direitos de acesso específicos da WFP, descritos na tabela abaixo.)</span><span class="sxs-lookup"><span data-stu-id="ce40f-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="ce40f-117">Os descritores de segurança padrão restantes são derivados por meio de herança.</span><span class="sxs-lookup"><span data-stu-id="ce40f-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="ce40f-118">Há algumas verificações de acesso, como para **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** function Calls, que não podem ser feitas no nível de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="ce40f-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="ce40f-119">Para essas funções, há objetos de contêiner para cada tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ce40f-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="ce40f-120">Para os tipos de objeto padrão (por exemplo, provedores, textos explicativos, filtros), as funções **Fwpm \* GetSecurityInfo0** e **Fwpm \* SetSecurityInfo0** existentes são sobrecarregadas, de modo que um parâmetro **GUID** nulo identifica o contêiner associado.</span><span class="sxs-lookup"><span data-stu-id="ce40f-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="ce40f-121">Para os outros tipos de objeto (por exemplo, eventos de rede e associações de segurança IPsec), há funções explícitas para gerenciar as informações de segurança do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ce40f-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="ce40f-122">O BFE dá suporte à herança automática de ACEs (entradas de controle de acesso) da DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="ce40f-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="ce40f-123">O BFE não dá suporte a ACEs da lista de controle de acesso (SACL) do sistema.</span><span class="sxs-lookup"><span data-stu-id="ce40f-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="ce40f-124">Os objetos herdam ACEs de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="ce40f-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="ce40f-125">Os contêineres herdam ACEs do mecanismo de filtro.</span><span class="sxs-lookup"><span data-stu-id="ce40f-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="ce40f-126">Os caminhos de propagação são mostrados no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce40f-126">The propagation paths are shown in the diagram below.</span></span>

![Diagrama que mostra os caminhos de propagação da ACE, começando com ' Engine '.](images/access-control.jpg)

<span data-ttu-id="ce40f-128">Para os tipos de objeto padrão, o BFE impõe todos os direitos de acesso genérico e padrão.</span><span class="sxs-lookup"><span data-stu-id="ce40f-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="ce40f-129">Além disso, a WFP define os direitos de acesso específicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce40f-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="ce40f-130">Direito de acesso de WFP</span><span class="sxs-lookup"><span data-stu-id="ce40f-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="ce40f-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce40f-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce40f-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="ce40f-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="ce40f-133">Necessário para adicionar um objeto a um contêiner.</span><span class="sxs-lookup"><span data-stu-id="ce40f-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="ce40f-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Add \_ link**</span><span class="sxs-lookup"><span data-stu-id="ce40f-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="ce40f-135">Necessário para criar uma associação a um objeto.</span><span class="sxs-lookup"><span data-stu-id="ce40f-135">Required to create an association to an object.</span></span> <span data-ttu-id="ce40f-136">Por exemplo, para adicionar um filtro que faz referência a um texto explicativo, o chamador deve ter o acesso de adicionar \_ link ao texto explicativo.</span><span class="sxs-lookup"><span data-stu-id="ce40f-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="ce40f-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ begin \_ Read \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="ce40f-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="ce40f-138">Necessário para iniciar uma transação de leitura explícita.</span><span class="sxs-lookup"><span data-stu-id="ce40f-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ce40f-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="ce40f-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="ce40f-140">Necessário para iniciar uma transação de gravação explícita.</span><span class="sxs-lookup"><span data-stu-id="ce40f-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="ce40f-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM \_ ACTRL \_ classificar**</span><span class="sxs-lookup"><span data-stu-id="ce40f-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="ce40f-142">Necessário para classificar em uma camada de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="ce40f-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ce40f-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL \_ enum**</span><span class="sxs-lookup"><span data-stu-id="ce40f-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="ce40f-144">Necessário para enumerar os objetos em um contêiner.</span><span class="sxs-lookup"><span data-stu-id="ce40f-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="ce40f-145">No entanto, o enumerador retorna somente os objetos aos quais o chamador tem \_ acesso de leitura FWPM ACTRL \_ .</span><span class="sxs-lookup"><span data-stu-id="ce40f-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="ce40f-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="ce40f-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="ce40f-147">Necessário para abrir uma sessão com o BFE.</span><span class="sxs-lookup"><span data-stu-id="ce40f-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="ce40f-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="ce40f-149">Necessário para ler as propriedades de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ce40f-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="ce40f-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ Read \_ stats**</span><span class="sxs-lookup"><span data-stu-id="ce40f-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="ce40f-151">Necessário para ler estatísticas.</span><span class="sxs-lookup"><span data-stu-id="ce40f-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="ce40f-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM \_ ACTRL \_ assinatura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="ce40f-153">Necessário para assinar notificações.</span><span class="sxs-lookup"><span data-stu-id="ce40f-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="ce40f-154">Os assinantes só receberão notificações para objetos aos quais eles têm acesso de leitura do FWPM \_ ACTRL \_ .</span><span class="sxs-lookup"><span data-stu-id="ce40f-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="ce40f-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="ce40f-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="ce40f-156">Necessário para definir as opções do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="ce40f-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="ce40f-157">O BFE ignora todas as verificações de acesso para chamadores de modo kernel.</span><span class="sxs-lookup"><span data-stu-id="ce40f-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="ce40f-158">Para impedir que os administradores bloqueiem o BFE, os membros do grupo de administradores internos sempre recebem **FWPM \_ ACTRL \_ abrir** para o objeto Engine.</span><span class="sxs-lookup"><span data-stu-id="ce40f-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="ce40f-159">Portanto, um administrador pode obter acesso por meio das etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce40f-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="ce40f-160">Habilite o privilégio **se \_ obter \_ \_ nome de propriedade** .</span><span class="sxs-lookup"><span data-stu-id="ce40f-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="ce40f-161">Chame [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="ce40f-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="ce40f-162">A chamada é realizada com sucesso porque o chamador é membro de administradores internos.</span><span class="sxs-lookup"><span data-stu-id="ce40f-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="ce40f-163">Apropriar-se do objeto do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="ce40f-163">Take ownership of the engine object.</span></span> <span data-ttu-id="ce40f-164">Isso é executado com sucesso porque o chamador tem o privilégio **se \_ obter \_ \_ nome de propriedade** .</span><span class="sxs-lookup"><span data-stu-id="ce40f-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="ce40f-165">Atualize a DACL.</span><span class="sxs-lookup"><span data-stu-id="ce40f-165">Update the DACL.</span></span> <span data-ttu-id="ce40f-166">Isso é executado com sucesso porque o proprietário sempre tem acesso de **gravação de \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="ce40f-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="ce40f-167">Como o BFE dá suporte a sua própria auditoria personalizada, ele não gera auditorias de acesso a objetos genéricos.</span><span class="sxs-lookup"><span data-stu-id="ce40f-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="ce40f-168">Portanto, a SACL é ignorada.</span><span class="sxs-lookup"><span data-stu-id="ce40f-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="ce40f-169">Direitos de acesso exigidos pelo WFP</span><span class="sxs-lookup"><span data-stu-id="ce40f-169">WFP Required Access Rights</span></span>

<span data-ttu-id="ce40f-170">A tabela a seguir mostra os direitos de acesso exigidos pelas funções WFP para acessar vários objetos de plataforma de filtragem.</span><span class="sxs-lookup"><span data-stu-id="ce40f-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="ce40f-171">As **\* *funções FwpmFilter _ são listadas como um exemplo para acessar os objetos padrão. Todas as outras funções que acessam objetos padrão seguem o modelo de acesso _* FwpmFilter \*** functions.</span><span class="sxs-lookup"><span data-stu-id="ce40f-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="ce40f-172">Função</span><span class="sxs-lookup"><span data-stu-id="ce40f-172">Function</span></span>

<span data-ttu-id="ce40f-173">Objeto marcado</span><span class="sxs-lookup"><span data-stu-id="ce40f-173">Object Checked</span></span>

<span data-ttu-id="ce40f-174">Acesso necessário</span><span class="sxs-lookup"><span data-stu-id="ce40f-174">Access Required</span></span>

[<span data-ttu-id="ce40f-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="ce40f-176">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="ce40f-176">Engine</span></span>

<span data-ttu-id="ce40f-177">**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="ce40f-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="ce40f-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="ce40f-179">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="ce40f-179">Engine</span></span>

<span data-ttu-id="ce40f-180">**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ce40f-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="ce40f-182">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="ce40f-182">Engine</span></span>

<span data-ttu-id="ce40f-183">**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="ce40f-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="ce40f-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="ce40f-185">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="ce40f-185">Engine</span></span>

<span data-ttu-id="ce40f-186">**FWPM \_ ACTRL \_ enum**</span><span class="sxs-lookup"><span data-stu-id="ce40f-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="ce40f-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="ce40f-188">Mecanismo</span><span class="sxs-lookup"><span data-stu-id="ce40f-188">Engine</span></span>

<span data-ttu-id="ce40f-189">**FWPM \_ ACTRL \_ begin \_ Read \_ TXN**  &  **FWPM \_ ACTRL \_ begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="ce40f-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="ce40f-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="ce40f-191">Provedor de contêiner</span><span class="sxs-lookup"><span data-stu-id="ce40f-191">Container Provider</span></span><br/> <span data-ttu-id="ce40f-192">Camada</span><span class="sxs-lookup"><span data-stu-id="ce40f-192">Layer</span></span><br/> <span data-ttu-id="ce40f-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="ce40f-193">Sub-Layer</span></span><br/> <span data-ttu-id="ce40f-194">Balão</span><span class="sxs-lookup"><span data-stu-id="ce40f-194">Callout</span></span><br/> <span data-ttu-id="ce40f-195">Contexto do provedor</span><span class="sxs-lookup"><span data-stu-id="ce40f-195">Provider Context</span></span><br/>

<span data-ttu-id="ce40f-196">**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Adicionar \_ link**</span><span class="sxs-lookup"><span data-stu-id="ce40f-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ce40f-197">**FWPM \_ ACTRL \_ Add \_ link**</span><span class="sxs-lookup"><span data-stu-id="ce40f-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ce40f-198">**FWPM \_ ACTRL \_ Add \_ link**</span><span class="sxs-lookup"><span data-stu-id="ce40f-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ce40f-199">**FWPM \_ ACTRL \_ Add \_ link**</span><span class="sxs-lookup"><span data-stu-id="ce40f-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ce40f-200">**FWPM \_ ACTRL \_ Add \_ link**</span><span class="sxs-lookup"><span data-stu-id="ce40f-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="ce40f-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="ce40f-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="ce40f-202">Filtrar</span><span class="sxs-lookup"><span data-stu-id="ce40f-202">Filter</span></span>

<span data-ttu-id="ce40f-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ce40f-203">**DELETE**</span></span>

<span data-ttu-id="ce40f-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="ce40f-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="ce40f-205">Filtrar</span><span class="sxs-lookup"><span data-stu-id="ce40f-205">Filter</span></span>

<span data-ttu-id="ce40f-206">**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ce40f-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="ce40f-208">Filtro de contêiner</span><span class="sxs-lookup"><span data-stu-id="ce40f-208">Container Filter</span></span><br/>

<span data-ttu-id="ce40f-209">**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="ce40f-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="ce40f-211">Contêiner</span><span class="sxs-lookup"><span data-stu-id="ce40f-211">Container</span></span>

<span data-ttu-id="ce40f-212">**FWPM \_ ACTRL \_ assinatura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="ce40f-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="ce40f-214">Contêiner</span><span class="sxs-lookup"><span data-stu-id="ce40f-214">Container</span></span>

<span data-ttu-id="ce40f-215">**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ce40f-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="ce40f-217">BANCO de segurança SA IPsec</span><span class="sxs-lookup"><span data-stu-id="ce40f-217">IPsec SA DB</span></span>

<span data-ttu-id="ce40f-218">**FWPM \_ ACTRL \_ Read \_ stats**</span><span class="sxs-lookup"><span data-stu-id="ce40f-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="ce40f-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="ce40f-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="ce40f-220">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="ce40f-221">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="ce40f-222">BANCO de segurança SA IPsec</span><span class="sxs-lookup"><span data-stu-id="ce40f-222">IPsec SA DB</span></span>

<span data-ttu-id="ce40f-223">**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="ce40f-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="ce40f-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="ce40f-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="ce40f-225">BANCO de segurança SA IPsec</span><span class="sxs-lookup"><span data-stu-id="ce40f-225">IPsec SA DB</span></span>

<span data-ttu-id="ce40f-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ce40f-226">**DELETE**</span></span>

[<span data-ttu-id="ce40f-227">**IPsecSaContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="ce40f-228">BANCO de segurança SA IPsec</span><span class="sxs-lookup"><span data-stu-id="ce40f-228">IPsec SA DB</span></span>

<span data-ttu-id="ce40f-229">**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="ce40f-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="ce40f-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="ce40f-231">BANCO de segurança SA IPsec</span><span class="sxs-lookup"><span data-stu-id="ce40f-231">IPsec SA DB</span></span>

<span data-ttu-id="ce40f-232">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="ce40f-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ce40f-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="ce40f-234">BD SA DE IKE</span><span class="sxs-lookup"><span data-stu-id="ce40f-234">IKE SA DB</span></span>

<span data-ttu-id="ce40f-235">**FWPM \_ ACTRL \_ Read \_ stats**</span><span class="sxs-lookup"><span data-stu-id="ce40f-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="ce40f-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="ce40f-237">BD SA DE IKE</span><span class="sxs-lookup"><span data-stu-id="ce40f-237">IKE SA DB</span></span>

<span data-ttu-id="ce40f-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ce40f-238">**DELETE**</span></span>

[<span data-ttu-id="ce40f-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="ce40f-240">BD SA DE IKE</span><span class="sxs-lookup"><span data-stu-id="ce40f-240">IKE SA DB</span></span>

<span data-ttu-id="ce40f-241">**FWPM \_ ACTRL \_ leitura**</span><span class="sxs-lookup"><span data-stu-id="ce40f-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ce40f-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="ce40f-243">BD SA DE IKE</span><span class="sxs-lookup"><span data-stu-id="ce40f-243">IKE SA DB</span></span>

<span data-ttu-id="ce40f-244">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="ce40f-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ce40f-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ce40f-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="ce40f-246">Contêiner</span><span class="sxs-lookup"><span data-stu-id="ce40f-246">Container</span></span>

<span data-ttu-id="ce40f-247">**FWPM \_ ACTRL \_ enum**</span><span class="sxs-lookup"><span data-stu-id="ce40f-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="ce40f-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="ce40f-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="ce40f-249">Nenhuma verificação de acesso adicional além daquela para os filtros individuais e contextos de provedor</span><span class="sxs-lookup"><span data-stu-id="ce40f-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="ce40f-250">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce40f-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce40f-251">**Direitos de acesso padrão**</span><span class="sxs-lookup"><span data-stu-id="ce40f-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="ce40f-252">Modelo de controle de acesso do Windows</span><span class="sxs-lookup"><span data-stu-id="ce40f-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="ce40f-253">**Identificadores de direitos de acesso da plataforma de filtragem do Windows**</span><span class="sxs-lookup"><span data-stu-id="ce40f-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 

