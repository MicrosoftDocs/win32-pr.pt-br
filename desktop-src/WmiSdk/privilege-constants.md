---
description: O parâmetro strPrivilege do método SWbemPrivilegeSet. AddAsString e o parâmetro iPrivilege para SWbemPrivilegeSet. Add exigem cadeias de caracteres de privilégio de WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Constantes de privilégio (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663244"
---
# <a name="privilege-constants"></a><span data-ttu-id="d7898-103">Constantes de privilégio</span><span class="sxs-lookup"><span data-stu-id="d7898-103">Privilege Constants</span></span>

<span data-ttu-id="d7898-104">O parâmetro *strPrivilege* do método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) e o parâmetro *iPrivilege* para [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) exigem cadeias de caracteres de privilégio de [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="d7898-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="d7898-105">Para obter mais informações sobre como usar constantes de privilégio, consulte [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d7898-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="d7898-106">As constantes a seguir são definidas em [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="d7898-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="d7898-107">A lista a seguir inclui as constantes equivalentes para C++ e cadeias de caracteres para scripts.</span><span class="sxs-lookup"><span data-stu-id="d7898-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="d7898-108">Para formar o nome curto do script, remova o "se" e o "privilégio" do nome da constante do C++.</span><span class="sxs-lookup"><span data-stu-id="d7898-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="d7898-109">O exemplo de código VBScript a seguir mostra como habilitar o privilégio RemoteShutdown em um script.</span><span class="sxs-lookup"><span data-stu-id="d7898-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="d7898-110">Muitos métodos WMI exigem que uma ou mais permissões sejam habilitadas.</span><span class="sxs-lookup"><span data-stu-id="d7898-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="d7898-111">Se uma conta não tiver recebido um privilégio, ela não poderá ser habilitada para a chamada de método.</span><span class="sxs-lookup"><span data-stu-id="d7898-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="d7898-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span><span class="sxs-lookup"><span data-stu-id="d7898-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d7898-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-114">Constante de C++: se criar cadeia de caracteres  de **\_ \_ \_ nome de token** : SeCreateTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="d7898-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="d7898-115">Nome curto do script: **Createtoken**</span><span class="sxs-lookup"><span data-stu-id="d7898-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="d7898-116">Necessário para criar um objeto de token primário.</span><span class="sxs-lookup"><span data-stu-id="d7898-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="d7898-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-118">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d7898-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-119">Constante de C++: **SeAssignPrimaryTokenPrivilege** String: **SeAssignPrimaryTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="d7898-120">Nome curto de script: **AssignPrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="d7898-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="d7898-121">Necessário para substituir um token de nível de processo.</span><span class="sxs-lookup"><span data-stu-id="d7898-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span><span class="sxs-lookup"><span data-stu-id="d7898-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-123">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="d7898-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-124">Constante de C++: cadeia de **nome da memória de bloqueio do se \_ \_ \_** : **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="d7898-125">Nome curto de script: **LockMemory**</span><span class="sxs-lookup"><span data-stu-id="d7898-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="d7898-126">Necessário para bloquear páginas na memória.</span><span class="sxs-lookup"><span data-stu-id="d7898-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span><span class="sxs-lookup"><span data-stu-id="d7898-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d7898-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-129">Constante de C++: se aumentar a cadeia de  caracteres do **\_ \_ \_ nome da cota** : SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="d7898-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="d7898-130">Nome curto de script: **IncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="d7898-131">Necessário para ajustar as cotas de memória de um processo.</span><span class="sxs-lookup"><span data-stu-id="d7898-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span><span class="sxs-lookup"><span data-stu-id="d7898-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-133">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="d7898-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-134">Constante de C++ **: \_ máquina \_ \_ nome da conta de se** cadeia de caracteres: **SeMachineAccountPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="d7898-135">Nome curto de script: **MachineAccount**</span><span class="sxs-lookup"><span data-stu-id="d7898-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="d7898-136">Necessário para adicionar estações de trabalho a um domínio.</span><span class="sxs-lookup"><span data-stu-id="d7898-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span><span class="sxs-lookup"><span data-stu-id="d7898-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-138">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="d7898-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-139">C Constant: **se \_ o \_ nome do TCB** String: **SeTcbPrivilege;**</span><span class="sxs-lookup"><span data-stu-id="d7898-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="d7898-140">Nome curto do script: **TCB**</span><span class="sxs-lookup"><span data-stu-id="d7898-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="d7898-141">Necessário para atuar como parte do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d7898-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="d7898-142">O detentor é parte da base de computadores confiáveis.</span><span class="sxs-lookup"><span data-stu-id="d7898-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span><span class="sxs-lookup"><span data-stu-id="d7898-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-144">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="d7898-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-145">Constante de C++: cadeia de **\_ \_ nome de segurança se** : **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="d7898-146">Nome curto do script: **segurança**</span><span class="sxs-lookup"><span data-stu-id="d7898-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="d7898-147">Necessário para gerenciar a auditoria e o log de segurança do NT.</span><span class="sxs-lookup"><span data-stu-id="d7898-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="d7898-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-149">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d7898-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-150">Constante de C++: se obter cadeia de caracteres  de **\_ \_ \_ nome de propriedade** : SeTakeOwnershipPrivilege</span><span class="sxs-lookup"><span data-stu-id="d7898-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="d7898-151">Nome curto de script: **TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="d7898-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="d7898-152">Necessário para assumir a propriedade de arquivos ou outros objetos sem ter uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL (lista de controle de *acesso discricionário* ).</span><span class="sxs-lookup"><span data-stu-id="d7898-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span><span class="sxs-lookup"><span data-stu-id="d7898-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-154">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="d7898-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-155">Constante de C++: se carregar cadeia de caracteres de **\_ \_ Driver** : **SeLoadDriverPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="d7898-156">Nome curto da script: **LoadDriver**</span><span class="sxs-lookup"><span data-stu-id="d7898-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="d7898-157">Necessário para carregar ou descarregar um driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7898-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="d7898-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-159">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="d7898-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-160">Constante de C++: **nome do perfil do sistema se cadeia de caracteres do \_ \_ \_ Name** : **SeSystemProfilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="d7898-161">Nome curto de script: **SystemProfile**</span><span class="sxs-lookup"><span data-stu-id="d7898-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="d7898-162">Necessário para coletar informações de perfil sobre o desempenho do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7898-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span><span class="sxs-lookup"><span data-stu-id="d7898-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-164">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="d7898-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-165">Constante de C++: **se \_ SYSTEMTIME** \_ nome cadeia de caracteres: **SeSystemtimePrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="d7898-166">Nome curto de script: **SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="d7898-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="d7898-167">Necessário para alterar a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7898-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="d7898-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-169">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="d7898-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-170">Constante do C++: **se Prof cadeia de \_ \_ \_ \_ nome de processo único** : **SeProfileSingleProcessPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="d7898-171">Nome curto de script: **ProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="d7898-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="d7898-172">Necessário para coletar informações de perfil para um único processo.</span><span class="sxs-lookup"><span data-stu-id="d7898-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="d7898-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-174">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="d7898-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-175">Constante de C++: de **\_ \_ \_ \_ nome de prioridade base do se Inc** : **SeIncreaseBasePriorityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="d7898-176">Nome curto de script: **IncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="d7898-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="d7898-177">Necessário para aumentar a prioridade de agendamento.</span><span class="sxs-lookup"><span data-stu-id="d7898-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="d7898-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-179">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="d7898-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-180">Constante C++: **se \_ criar \_ \_ nome de arquivo de paginação** cadeia de caracteres: **SeCreatePagefilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="d7898-181">Nome curto de script: **CreatePageFile**</span><span class="sxs-lookup"><span data-stu-id="d7898-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="d7898-182">Necessário para criar um arquivo de paginação.</span><span class="sxs-lookup"><span data-stu-id="d7898-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="d7898-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-184">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="d7898-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-185">Constante de C++: **se criar cadeia de \_ \_ \_ nome permanente** : **SeCreatePermanentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="d7898-186">Nome curto de script: **Createpermanent**</span><span class="sxs-lookup"><span data-stu-id="d7898-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="d7898-187">Necessário para criar objetos compartilhados permanentes.</span><span class="sxs-lookup"><span data-stu-id="d7898-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span><span class="sxs-lookup"><span data-stu-id="d7898-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-189">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d7898-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-190">Constante de C++ **: \_ se \_ nome de backup** cadeia de caracteres: **SeBackupPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="d7898-191">Nome curto do script: **backup**</span><span class="sxs-lookup"><span data-stu-id="d7898-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="d7898-192">Necessário para fazer backup de arquivos e diretórios, independentemente da ACL especificada para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d7898-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span><span class="sxs-lookup"><span data-stu-id="d7898-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-194">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="d7898-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-195">Constante de C++ **: \_ se \_ nome de restauração** da cadeia de caracteres: **SeRestorePrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="d7898-196">Nome curto da script: **restaurar**</span><span class="sxs-lookup"><span data-stu-id="d7898-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="d7898-197">Necessário para restaurar arquivos e diretórios, independentemente da ACL especificada para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="d7898-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span><span class="sxs-lookup"><span data-stu-id="d7898-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-199">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="d7898-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-200">Constante C++: **se \_ \_ nome do desligamento** da cadeia de caracteres: **SeShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="d7898-201">Nome curto do script: **desligamento**</span><span class="sxs-lookup"><span data-stu-id="d7898-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="d7898-202">Necessário para desligar o sistema local.</span><span class="sxs-lookup"><span data-stu-id="d7898-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span><span class="sxs-lookup"><span data-stu-id="d7898-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-204">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="d7898-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-205">Constante de C++ **: \_ se \_ nome de depuração** cadeia de caracteres: **SeDebugPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="d7898-206">Nome curto do script: **depuração**</span><span class="sxs-lookup"><span data-stu-id="d7898-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="d7898-207">Necessário para depurar e ajustar a memória de um processo de propriedade de outra conta.</span><span class="sxs-lookup"><span data-stu-id="d7898-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span><span class="sxs-lookup"><span data-stu-id="d7898-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-209">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="d7898-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-210">Constante de C++ **: \_ se \_ nome de auditoria** String: **SeAuditPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="d7898-211">Nome curto da script: **auditoria**</span><span class="sxs-lookup"><span data-stu-id="d7898-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="d7898-212">Necessário para gerar entradas de auditoria no log de segurança do NT.</span><span class="sxs-lookup"><span data-stu-id="d7898-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="d7898-213">Somente servidores seguros devem ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="d7898-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d7898-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-215">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="d7898-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-216">Constante de C++: cadeia de **nome de \_ ambiente de sistema \_ \_ se** : **SeSystemEnvironmentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="d7898-217">Nome curto de script: **SystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="d7898-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="d7898-218">Necessário para modificar a RAM não volátil de sistemas que usam esse tipo de memória para armazenar dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="d7898-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="d7898-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-220">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="d7898-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-221">Constante de C++: **se alterar String de \_ \_ \_ nome de notificação** : **SeChangeNotifyPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="d7898-222">Nome curto de script: **ChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="d7898-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="d7898-223">Necessário para receber notificações de alterações em arquivos ou diretórios e ignorar verificações de acesso de passagem.</span><span class="sxs-lookup"><span data-stu-id="d7898-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="d7898-224">Esse privilégio é habilitado por padrão para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="d7898-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="d7898-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-226">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="d7898-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-227">Constante de C++: se a cadeia de **\_ \_ \_ nome de desligamento remoto** : **SeRemoteShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="d7898-228">Nome curto de script: **RemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="d7898-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="d7898-229">Necessário para desligar um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d7898-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span><span class="sxs-lookup"><span data-stu-id="d7898-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-231">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="d7898-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-232">C Constant: **se \_ \_ desencaixar** cadeia de caracteres de nome: **SeUndockPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="d7898-233">Nome curto do script: **desencaixar**</span><span class="sxs-lookup"><span data-stu-id="d7898-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="d7898-234">Necessário para remover um laptop de uma estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="d7898-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span><span class="sxs-lookup"><span data-stu-id="d7898-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-236">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="d7898-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-237">Constante de C++ **: \_ se \_ \_ nome do agente de sincronização** cadeia de caracteres: **SeSyncAgentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="d7898-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="d7898-238">Nome curto de script: **SyncAgent**</span><span class="sxs-lookup"><span data-stu-id="d7898-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="d7898-239">Necessário para sincronizar os dados do serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="d7898-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="d7898-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-241">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="d7898-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-242">Constante de C++: se habilitar a cadeia de  **\_ \_ \_ nome de delegação** : seenabledelegationprivilege foi</span><span class="sxs-lookup"><span data-stu-id="d7898-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="d7898-243">Nome curto de script: **EnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="d7898-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="d7898-244">Necessário para permitir que contas de computador e de usuário sejam confiáveis para delegação.</span><span class="sxs-lookup"><span data-stu-id="d7898-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d7898-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span><span class="sxs-lookup"><span data-stu-id="d7898-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7898-246">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="d7898-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="d7898-247">Constante de C++: se gerenciar a cadeia de  caracteres do **\_ \_ \_ nome do volume** : SeManageVolumePrivilege</span><span class="sxs-lookup"><span data-stu-id="d7898-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="d7898-248">Nome curto de script: **ManageVolume**</span><span class="sxs-lookup"><span data-stu-id="d7898-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="d7898-249">Necessário para executar tarefas de manutenção de volume.</span><span class="sxs-lookup"><span data-stu-id="d7898-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7898-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7898-250">Requirements</span></span>



| <span data-ttu-id="d7898-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7898-251">Requirement</span></span> | <span data-ttu-id="d7898-252">Valor</span><span class="sxs-lookup"><span data-stu-id="d7898-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7898-253">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7898-253">Minimum supported client</span></span><br/> | <span data-ttu-id="d7898-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7898-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7898-255">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7898-255">Minimum supported server</span></span><br/> | <span data-ttu-id="d7898-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7898-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7898-257">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7898-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7898-258"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7898-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7898-259">INSERI</span><span class="sxs-lookup"><span data-stu-id="d7898-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7898-260"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7898-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7898-261">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7898-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7898-262">Constantes de API de script</span><span class="sxs-lookup"><span data-stu-id="d7898-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="d7898-263">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="d7898-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="d7898-264">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="d7898-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="d7898-265">Executando operações privilegiadas</span><span class="sxs-lookup"><span data-stu-id="d7898-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="d7898-266">Executando operações privilegiadas usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="d7898-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

