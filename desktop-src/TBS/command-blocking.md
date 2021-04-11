---
title: Bloqueio de comando
description: Para preservar a integridade das operações, determinados comandos do TPM não podem ser executados pelo software na plataforma.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104365796"
---
# <a name="command-blocking"></a><span data-ttu-id="f218f-103">Bloqueio de comando</span><span class="sxs-lookup"><span data-stu-id="f218f-103">Command Blocking</span></span>

<span data-ttu-id="f218f-104">Para preservar a integridade das operações, determinados comandos do TPM não podem ser executados pelo software na plataforma.</span><span class="sxs-lookup"><span data-stu-id="f218f-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="f218f-105">Por exemplo, alguns comandos são executados apenas pelo software do sistema.</span><span class="sxs-lookup"><span data-stu-id="f218f-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="f218f-106">Quando o TBS bloqueia um comando, um erro é retornado conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="f218f-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="f218f-107">Por padrão, o TBS bloqueia comandos que poderiam afetar a privacidade, a segurança e a estabilidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="f218f-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="f218f-108">O TBS também pressupõe que outras partes da pilha de software possam restringir o acesso a determinados comandos a entidades autorizadas.</span><span class="sxs-lookup"><span data-stu-id="f218f-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="f218f-109">Para comandos do TPM versão 1,2, há três listas de comandos bloqueados: uma lista controlada pela política de grupo, uma lista controlada por administradores locais e uma lista padrão.</span><span class="sxs-lookup"><span data-stu-id="f218f-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="f218f-110">Um comando do TPM será bloqueado se estiver em qualquer uma das listas.</span><span class="sxs-lookup"><span data-stu-id="f218f-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="f218f-111">No entanto, há sinalizadores de política de grupo para permitir que o TBS ignore a lista local e a lista padrão.</span><span class="sxs-lookup"><span data-stu-id="f218f-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="f218f-112">Os sinalizadores de política de grupo podem ser editados diretamente ou acessados por meio do Editor de Objeto de Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="f218f-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="f218f-113">A lista de comandos bloqueados localmente não é preservada após uma atualização para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="f218f-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="f218f-114">Os comandos que são bloqueados na lista de Política de Grupo são preservados.</span><span class="sxs-lookup"><span data-stu-id="f218f-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="f218f-115">Para comandos do TPM versão 2,0, a lógica para o bloqueio é invertida; Ele usa uma lista de comandos permitidos.</span><span class="sxs-lookup"><span data-stu-id="f218f-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="f218f-116">Essa lógica bloqueará automaticamente os comandos que não eram conhecidos quando a lista foi feita pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="f218f-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="f218f-117">Quando os comandos são adicionados à especificação do TPM após a entrega de uma versão do Windows, esses novos comandos são bloqueados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f218f-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="f218f-118">Somente uma atualização do registro adicionará esses novos comandos à lista de comandos permitidos.</span><span class="sxs-lookup"><span data-stu-id="f218f-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="f218f-119">A partir do Windows 10 1809 (Windows Server 2019), os comandos permitidos do TPM 2,0 não podem mais ser manipulados por meio de configurações do registro.</span><span class="sxs-lookup"><span data-stu-id="f218f-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="f218f-120">Para essas versões do Windows 10, os comandos do TPM 2,0 permitidos são corrigidos no driver do TPM.</span><span class="sxs-lookup"><span data-stu-id="f218f-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="f218f-121">Os comandos do TPM 1,2 ainda podem ser bloqueados e desbloqueados por meio de alterações no registro.</span><span class="sxs-lookup"><span data-stu-id="f218f-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="f218f-122">Acesso direto ao registro</span><span class="sxs-lookup"><span data-stu-id="f218f-122">Direct Registry Access</span></span>

<span data-ttu-id="f218f-123">Os sinalizadores de política de grupo estão na chave do registro **HKEY \_ local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.</span><span class="sxs-lookup"><span data-stu-id="f218f-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="f218f-124">Para determinar quais listas devem ser usadas para bloquear comandos do TPM, há dois valores **DWORD** que são usados como sinalizadores boolianos:</span><span class="sxs-lookup"><span data-stu-id="f218f-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="f218f-125">"IgnoreDefaultList"</span><span class="sxs-lookup"><span data-stu-id="f218f-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="f218f-126">Se definido (o valor existe e é diferente de zero), o TBS ignora a lista de comandos bloqueados padrão.</span><span class="sxs-lookup"><span data-stu-id="f218f-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="f218f-127">"IgnoreLocalList"</span><span class="sxs-lookup"><span data-stu-id="f218f-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="f218f-128">Se definido (o valor existe e é diferente de zero), o TBS ignora a lista de comandos bloqueados locais.</span><span class="sxs-lookup"><span data-stu-id="f218f-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="f218f-129">Editor de objeto de política de grupo</span><span class="sxs-lookup"><span data-stu-id="f218f-129">Group Policy Object Editor</span></span>

<span data-ttu-id="f218f-130">**Para acessar o editor de objeto de Política de Grupo**</span><span class="sxs-lookup"><span data-stu-id="f218f-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="f218f-131">Clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="f218f-131">Click **Start**.</span></span>
2.  <span data-ttu-id="f218f-132">Clique em **Executar**.</span><span class="sxs-lookup"><span data-stu-id="f218f-132">Click **Run**.</span></span>
3.  <span data-ttu-id="f218f-133">Na caixa **Abrir** , digite **gpedit.msc**.</span><span class="sxs-lookup"><span data-stu-id="f218f-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="f218f-134">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="f218f-134">Click **OK**.</span></span> <span data-ttu-id="f218f-135">O editor de objeto Política de Grupo é aberto.</span><span class="sxs-lookup"><span data-stu-id="f218f-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="f218f-136">Expanda **configuração do computador**.</span><span class="sxs-lookup"><span data-stu-id="f218f-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="f218f-137">Expanda **modelos administrativos**.</span><span class="sxs-lookup"><span data-stu-id="f218f-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="f218f-138">Expanda **sistema**.</span><span class="sxs-lookup"><span data-stu-id="f218f-138">Expand **System**.</span></span>
7.  <span data-ttu-id="f218f-139">Expanda **serviços Trusted Platform modules**.</span><span class="sxs-lookup"><span data-stu-id="f218f-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="f218f-140">As listas de comandos do TPM 1.2 bloqueados específicos podem ser editadas diretamente nos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="f218f-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="f218f-141">Lista de políticas de Grupo:</span><span class="sxs-lookup"><span data-stu-id="f218f-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="f218f-142">Lista local:</span><span class="sxs-lookup"><span data-stu-id="f218f-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="f218f-143">Lista padrão:</span><span class="sxs-lookup"><span data-stu-id="f218f-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="f218f-144">Em cada uma dessas chaves do registro, há uma lista de valores do registro do \_ tipo reg sz.</span><span class="sxs-lookup"><span data-stu-id="f218f-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="f218f-145">Cada valor representa um comando bloqueado do TPM.</span><span class="sxs-lookup"><span data-stu-id="f218f-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="f218f-146">Cada chave do registro tem um campo "nome do valor" e um campo "dados do valor".</span><span class="sxs-lookup"><span data-stu-id="f218f-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="f218f-147">Os dois campos ("nome do valor" e "dados do valor") devem corresponder exatamente ao valor decimal do ordinal do comando do TPM a ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f218f-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="f218f-148">A lista de comandos específicos do TPM 2,0 permitidos pode ser editada diretamente no seguinte local.</span><span class="sxs-lookup"><span data-stu-id="f218f-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="f218f-149">Na chave do registro, há uma lista de valores do registro do \_ tipo reg DWORD.</span><span class="sxs-lookup"><span data-stu-id="f218f-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="f218f-150">Cada valor representa um comando do TPM 2,0 permitido.</span><span class="sxs-lookup"><span data-stu-id="f218f-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="f218f-151">Cada valor de registro tem um **nome** e um campo de **valor** .</span><span class="sxs-lookup"><span data-stu-id="f218f-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="f218f-152">O **nome** corresponde ao ordinal de comando do TPM 2,0 hexadecimal que deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="f218f-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="f218f-153">O **valor** terá um valor de 1 se o comando for permitido.</span><span class="sxs-lookup"><span data-stu-id="f218f-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="f218f-154">Se um ordinal de comando não estiver presente ou tiver um valor de 0, o comando será bloqueado.</span><span class="sxs-lookup"><span data-stu-id="f218f-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="f218f-155">Lista padrão:</span><span class="sxs-lookup"><span data-stu-id="f218f-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="f218f-156">Para o Windows 8, o Windows Server 2012 e posterior, as chaves do registro **BlockedCommands** e **AllowedW8Commands** respectivamente determinam os comandos do TPM bloqueados ou permitidos para contas de administrador.</span><span class="sxs-lookup"><span data-stu-id="f218f-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="f218f-157">As contas de usuário têm uma lista de comandos do TPM bloqueados ou permitidos nas chaves do registro **BlockedUserCommands** e **AllowedW8UserCommands** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f218f-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="f218f-158">No Windows 10, versão 1607, novas chaves do registro foram introduzidas para aplicativos do AppContainer: **BlockedAppContainerCommands** e **AllowedW8AppContainerCommands**.</span><span class="sxs-lookup"><span data-stu-id="f218f-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




