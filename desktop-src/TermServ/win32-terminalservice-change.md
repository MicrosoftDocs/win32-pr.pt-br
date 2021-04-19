---
title: Método Change da classe Win32_Service (Mbnapi. h) (TerminalService)
description: Modifica um TerminalService Win32 \_ .
ms.assetid: 19E43A80-47C9-4C5A-8E73-723F206AA7C0
ms.tgt_platform: multiple
keywords:
- Alterar o método Serviços de Área de Trabalho Remota
- Alterar método Serviços de Área de Trabalho Remota, classe Win32_Service
- Serviços de Área de Trabalho Remota de classe Win32_Service, alterar método
topic_type:
- apiref
api_name:
- Win32_Service.Change
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa34ea0c9c38cd0b11f97a0bbf651f1aebf37a46
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389203"
---
# <a name="change-method-of-the-win32_service-class-mbnapih---terminalservice"></a><span data-ttu-id="b72a2-106">Método Change da classe Win32_Service (Mbnapi. h)-TerminalService</span><span class="sxs-lookup"><span data-stu-id="b72a2-106">Change method of the Win32_Service class (Mbnapi.h) - TerminalService</span></span>

<span data-ttu-id="b72a2-107">O método **Change** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) modifica um [**\_ TerminalService Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="b72a2-107">The **Change** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="b72a2-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b72a2-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b72a2-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b72a2-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b72a2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b72a2-110">Syntax</span></span>


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies,
  [in] string  ServiceDependencies
);
```



## <a name="parameters"></a><span data-ttu-id="b72a2-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b72a2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b72a2-112">*DisplayName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-112">*DisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-113">O nome para exibição do serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-113">The display name of the service.</span></span> <span data-ttu-id="b72a2-114">Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b72a2-114">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="b72a2-115">O nome é, por caso, preservado no Gerenciador de controle de serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-115">The name is case-preserved in the service control manager.</span></span> <span data-ttu-id="b72a2-116">As comparações *DisplayName* sempre diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b72a2-116">*DisplayName* comparisons are always case-insensitive.</span></span>

<span data-ttu-id="b72a2-117">Restrições: aceita o mesmo valor que a propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="b72a2-117">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="b72a2-118">Exemplo, "atdisk".</span><span class="sxs-lookup"><span data-stu-id="b72a2-118">Example, "Atdisk".</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-119">*Nome do caminho* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-119">*PathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-120">O caminho totalmente qualificado para o arquivo executável que implementa o serviço, por exemplo, " \\ systemroot \\ System32 \\ drivers \\afd.sys".</span><span class="sxs-lookup"><span data-stu-id="b72a2-120">The fully qualified path to the executable file that implements the service, for example, "\\SystemRoot\\System32\\drivers\\afd.sys".</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-121">*ServiceType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-121">*ServiceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-122">O tipo de serviços fornecidos aos processos que os chamam.</span><span class="sxs-lookup"><span data-stu-id="b72a2-122">The type of services provided to processes that call them.</span></span>

<dt>

<span data-ttu-id="b72a2-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="b72a2-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-124">Driver de kernel</span><span class="sxs-lookup"><span data-stu-id="b72a2-124">Kernel Driver</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-125">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="b72a2-125">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-126">Driver do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="b72a2-126">File System Driver</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-127">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="b72a2-127">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-128">Adaptador</span><span class="sxs-lookup"><span data-stu-id="b72a2-128">Adapter</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-129">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="b72a2-129">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-130">Driver do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="b72a2-130">Recognizer Driver</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-131">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="b72a2-131">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-132">Próprio processo</span><span class="sxs-lookup"><span data-stu-id="b72a2-132">Own Process</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-133">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="b72a2-133">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-134">Processo de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="b72a2-134">Share Process</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-135">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="b72a2-135">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-136">Processo interativo</span><span class="sxs-lookup"><span data-stu-id="b72a2-136">Interactive Process</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b72a2-137">*ErrorControl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-137">*ErrorControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-138">Severidade do erro se esse serviço não for iniciado durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="b72a2-138">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="b72a2-139">O valor indica a ação tomada pelo programa de inicialização se ocorrer falha.</span><span class="sxs-lookup"><span data-stu-id="b72a2-139">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="b72a2-140">Todos os erros são registrados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-140">All errors are logged by the system.</span></span>

<dt>

<span data-ttu-id="b72a2-141">0</span><span class="sxs-lookup"><span data-stu-id="b72a2-141">0</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-142">**Ignorar**.</span><span class="sxs-lookup"><span data-stu-id="b72a2-142">**Ignore**.</span></span> <span data-ttu-id="b72a2-143">A inicialização continua.</span><span class="sxs-lookup"><span data-stu-id="b72a2-143">Startup continues.</span></span> <span data-ttu-id="b72a2-144">Nenhuma notificação é dada ao usuário de que o serviço falhou.</span><span class="sxs-lookup"><span data-stu-id="b72a2-144">No notification is given to the user that the service failed.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-145">1</span><span class="sxs-lookup"><span data-stu-id="b72a2-145">1</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-146">**Normal.**</span><span class="sxs-lookup"><span data-stu-id="b72a2-146">**Normal.**</span></span> <span data-ttu-id="b72a2-147">A inicialização continua.</span><span class="sxs-lookup"><span data-stu-id="b72a2-147">Startup continues.</span></span> <span data-ttu-id="b72a2-148">Antes que o usuário faça logon, o usuário recebe a notificação, "pelo menos um serviço ou dispositivo falhou durante a inicialização".</span><span class="sxs-lookup"><span data-stu-id="b72a2-148">Before the user logs on, the user receives the notification, "At least one service or device failed during startup."</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-149">2</span><span class="sxs-lookup"><span data-stu-id="b72a2-149">2</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-150">**Muito.**</span><span class="sxs-lookup"><span data-stu-id="b72a2-150">**Severe.**</span></span> <span data-ttu-id="b72a2-151">O computador tenta reiniciar com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="b72a2-151">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="b72a2-152">Se o serviço falhar novamente, a inicialização continuará e a notificação será fornecida ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b72a2-152">If the service fails again, startup continues and notification is given to the user.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-153">3</span><span class="sxs-lookup"><span data-stu-id="b72a2-153">3</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-154">**Drasticamente.**</span><span class="sxs-lookup"><span data-stu-id="b72a2-154">**Critical.**</span></span> <span data-ttu-id="b72a2-155">O computador tenta reiniciar com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="b72a2-155">Computer attempts to restart with last-known good configuration.</span></span> <span data-ttu-id="b72a2-156">Se o serviço falhar novamente, a inicialização será interrompida.</span><span class="sxs-lookup"><span data-stu-id="b72a2-156">If the service fails again, startup stops.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b72a2-157">*StartMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-157">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-158">Modo de início do serviço base do Windows.</span><span class="sxs-lookup"><span data-stu-id="b72a2-158">Start mode of the Windows base service.</span></span> <span data-ttu-id="b72a2-159">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="b72a2-159">For more information, see the Remarks section.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="b72a2-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="b72a2-160"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="b72a2-161">Driver de dispositivo iniciado pelo carregador do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b72a2-161">Device driver started by the operating system loader.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="b72a2-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema**</span><span class="sxs-lookup"><span data-stu-id="b72a2-162"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="b72a2-163">Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b72a2-163">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="b72a2-164">Esse valor só é válido para serviços do driver.</span><span class="sxs-lookup"><span data-stu-id="b72a2-164">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="b72a2-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático**</span><span class="sxs-lookup"><span data-stu-id="b72a2-165"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="b72a2-166">O serviço é iniciado automaticamente pelo Gerenciador de controle de serviço durante a inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-166">Service is started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="b72a2-167">Os serviços de inicialização automática iniciam antes que um usuário faça logon no computador e execute mesmo que nenhum usuário faça logon no computador.</span><span class="sxs-lookup"><span data-stu-id="b72a2-167">Autostart services start before a user logs on to the computer and run even if no user logs on to the computer.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="b72a2-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span><span class="sxs-lookup"><span data-stu-id="b72a2-168"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="b72a2-169">Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="b72a2-169">Service to be started by the service control manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span> <span data-ttu-id="b72a2-170">Embora os serviços manuais devam ser especificamente iniciados por um usuário (ou por um script), eles continuam a ser executados mesmo que o usuário faça logoff.</span><span class="sxs-lookup"><span data-stu-id="b72a2-170">Although manual services must be specifically started by a user (or by a script), they continue to run even if the user logs off.</span></span> <span data-ttu-id="b72a2-171">Os serviços manuais são geralmente chamados de serviços sob demanda.</span><span class="sxs-lookup"><span data-stu-id="b72a2-171">Manual services are often referred to as on-demand services.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b72a2-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**</span><span class="sxs-lookup"><span data-stu-id="b72a2-172"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="b72a2-173">Serviço que não pode mais ser iniciado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-173">Service that can no longer be started.</span></span> <span data-ttu-id="b72a2-174">Para iniciar um serviço desabilitado, você deve primeiro alterar a opção de inicialização para automático ou manual.</span><span class="sxs-lookup"><span data-stu-id="b72a2-174">To start a disabled service, you must first change the startup option to either Auto or Manual.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b72a2-175">*DesktopInteract* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-175">*DesktopInteract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-176">Se **for true**, o serviço poderá criar ou se comunicar com uma janela na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b72a2-176">If **True**, the service can create or communicate with a window on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-177">*Iniciar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-177">*StartName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-178">Nome da conta sob a qual o serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-178">Account name the service runs under.</span></span> <span data-ttu-id="b72a2-179">Dependendo do tipo de serviço, o nome da conta pode estar na forma de nome_do_domínio \\ username ou. \\ Usu.</span><span class="sxs-lookup"><span data-stu-id="b72a2-179">Depending on the service type, the account name may be in the form of DomainName\\Username or .\\Username.</span></span> <span data-ttu-id="b72a2-180">O processo de serviço será registrado usando uma dessas duas formas quando for executado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-180">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="b72a2-181">Se a conta pertencer ao domínio interno,. \\ O nome de usuário pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-181">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="b72a2-182">Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="b72a2-182">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="b72a2-183">Para drivers de nível de kernel ou de sistema, *StartName* contém o nome do objeto de driver (ou seja, \\ FileSystem \\ rdr ou o \\ Driver \\ XNS) que o sistema de entrada e saída (e/s) usa para carregar o driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b72a2-183">For kernel or system-level drivers, *StartName* contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) that the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="b72a2-184">Se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço, por exemplo, "DWDOM \\ admin".</span><span class="sxs-lookup"><span data-stu-id="b72a2-184">If **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name, for example, "DWDOM\\Admin".</span></span>

<span data-ttu-id="b72a2-185">Você também pode usar o formato UPN (nome principal do usuário) para especificar o **StartName**, por exemplo, *Username@DomainName* .</span><span class="sxs-lookup"><span data-stu-id="b72a2-185">You also can use the User Principal Name (UPN) format to specify the **StartName**, for example, *Username@DomainName*.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-186">*StartPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-186">*StartPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-187">Senha para o nome da conta especificada pelo parâmetro *StartName* .</span><span class="sxs-lookup"><span data-stu-id="b72a2-187">Password to the account name specified by the *StartName* parameter.</span></span> <span data-ttu-id="b72a2-188">Especifique **NULL** se você não estiver alterando a senha.</span><span class="sxs-lookup"><span data-stu-id="b72a2-188">Specify **NULL** if you are not changing the password.</span></span> <span data-ttu-id="b72a2-189">Especifique uma cadeia de caracteres vazia se o serviço não tiver nenhuma senha.</span><span class="sxs-lookup"><span data-stu-id="b72a2-189">Specify an empty string if the service has no password.</span></span>

> [!Note]  
> <span data-ttu-id="b72a2-190">Ao alterar um serviço de um sistema local para uma rede, ou de uma rede para um sistema local, *StartPassword* deve ser uma cadeia de caracteres vazia ("") e não **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b72a2-190">When changing a service from a local system to a network, or from a network to a local system, *StartPassword* must be an empty string ("") and not **NULL**.</span></span>

 

</dd> <dt>

<span data-ttu-id="b72a2-191">*OrderGroup* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-191">*LoadOrderGroup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-192">Nome do grupo ao qual ele está associado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-192">Group name that it is associated with.</span></span> <span data-ttu-id="b72a2-193">Os grupos de ordem de carregamento estão contidos no registro do sistema e determinam a sequência na qual os serviços são carregados no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b72a2-193">Load order groups are contained in the system registry, and determine the sequence in which services are loaded into the operating system.</span></span> <span data-ttu-id="b72a2-194">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não pertencerá a um grupo.</span><span class="sxs-lookup"><span data-stu-id="b72a2-194">If the pointer is **NULL**, or if it points to an empty string, the service does not belong to a group.</span></span> <span data-ttu-id="b72a2-195">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="b72a2-195">For more information, see the Remarks section.</span></span>

<span data-ttu-id="b72a2-196">As dependências entre grupos devem ser listadas no parâmetro *LoadOrderGroupDependencies* .</span><span class="sxs-lookup"><span data-stu-id="b72a2-196">Dependencies between groups should be listed in the *LoadOrderGroupDependencies* parameter.</span></span> <span data-ttu-id="b72a2-197">Os serviços na lista de grupos de ordenação de carga são iniciados primeiro, seguidos de serviços em grupos que não estão na lista de grupos de ordenação de carga, seguidos pelos serviços que não pertencem a um grupo.</span><span class="sxs-lookup"><span data-stu-id="b72a2-197">Services in the load-ordering group list are started first, followed by services in groups not in the load-ordering group list, followed by services that do not belong to a group.</span></span> <span data-ttu-id="b72a2-198">O registro do sistema tem uma lista de grupos de ordenação de carga localizados em:</span><span class="sxs-lookup"><span data-stu-id="b72a2-198">The system registry has a list of load ordering groups located at:</span></span>

<span data-ttu-id="b72a2-199">**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **ServiceGroupOrder**</span><span class="sxs-lookup"><span data-stu-id="b72a2-199">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-200">*LoadOrderGroupDependencies* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-200">*LoadOrderGroupDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-201">Lista de grupos de ordenação de carga que devem iniciar antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-201">List of load-ordering groups that must start before this service starts.</span></span> <span data-ttu-id="b72a2-202">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b72a2-202">The array is doubly **null**-terminated.</span></span> <span data-ttu-id="b72a2-203">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="b72a2-203">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="b72a2-204">Os nomes de grupo devem ser prefixados pelo **\_ \_ identificador de grupo SC** (definido no arquivo Winsvc. h) para diferenciá-los dos nomes de serviço, pois serviços e grupos de serviço compartilham o mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="b72a2-204">Group names must be prefixed by the **SC\_GROUP\_IDENTIFIER** (defined in the Winsvc.h file) character to differentiate them from service names because services and service groups share the same namespace.</span></span> <span data-ttu-id="b72a2-205">A dependência de um grupo significa que esse serviço pode ser executado se pelo menos um membro do grupo estiver em execução depois de uma tentativa de iniciar todos os membros do grupo.</span><span class="sxs-lookup"><span data-stu-id="b72a2-205">Dependency on a group means that this service can run if at least one member of the group is running after an attempt to start all of the members of the group.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-206">*Imdependências* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b72a2-206">*ServiceDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-207">Lista que contém os nomes dos serviços que devem ser iniciados antes do início desse serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-207">List that contains the names of services that must start before this service starts.</span></span> <span data-ttu-id="b72a2-208">A matriz é duplamente terminada por **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b72a2-208">The array is doubly **NULL**-terminated.</span></span> <span data-ttu-id="b72a2-209">Se o ponteiro for **nulo** ou se apontar para uma cadeia de caracteres vazia, o serviço não terá dependências.</span><span class="sxs-lookup"><span data-stu-id="b72a2-209">If the pointer is **NULL**, or if it points to an empty string, the service has no dependencies.</span></span> <span data-ttu-id="b72a2-210">A dependência em um serviço indica que esse serviço pode ser executado somente se o serviço do qual ele depende estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="b72a2-210">Dependency on a service indicates that this service can run only if the service it depends on is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b72a2-211">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b72a2-211">Return value</span></span>

<span data-ttu-id="b72a2-212">Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b72a2-212">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="b72a2-213">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b72a2-213">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b72a2-214">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b72a2-214">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b72a2-215">**0**</span><span class="sxs-lookup"><span data-stu-id="b72a2-215">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-216">A solicitação foi aceita.</span><span class="sxs-lookup"><span data-stu-id="b72a2-216">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-217">**1**</span><span class="sxs-lookup"><span data-stu-id="b72a2-217">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-218">A solicitação não terá suporte.</span><span class="sxs-lookup"><span data-stu-id="b72a2-218">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-219">**2**</span><span class="sxs-lookup"><span data-stu-id="b72a2-219">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-220">O usuário não tinha o acesso necessário.</span><span class="sxs-lookup"><span data-stu-id="b72a2-220">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-221">**3**</span><span class="sxs-lookup"><span data-stu-id="b72a2-221">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-222">O serviço não pode ser interrompido, porque outros serviços em execução dependem dele.</span><span class="sxs-lookup"><span data-stu-id="b72a2-222">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-223">**4**</span><span class="sxs-lookup"><span data-stu-id="b72a2-223">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-224">O código de controle pedido não é válido ou é inaceitável para o serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-224">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-225">**5**</span><span class="sxs-lookup"><span data-stu-id="b72a2-225">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-226">O código de controle solicitado não pode ser enviado ao serviço porque o estado do serviço ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* A propriedade State) é igual a 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="b72a2-226">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-227">**6**</span><span class="sxs-lookup"><span data-stu-id="b72a2-227">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-228">O serviço não foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-228">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-229">**7**</span><span class="sxs-lookup"><span data-stu-id="b72a2-229">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-230">O serviço não respondeu à solicitação de início em um tempo oportuno.</span><span class="sxs-lookup"><span data-stu-id="b72a2-230">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-231">**8**</span><span class="sxs-lookup"><span data-stu-id="b72a2-231">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-232">Falha desconhecida ao iniciar o serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-232">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-233">**9**</span><span class="sxs-lookup"><span data-stu-id="b72a2-233">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-234">O caminho do diretório para o arquivo executável do serviço não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-234">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-235">**10**</span><span class="sxs-lookup"><span data-stu-id="b72a2-235">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-236">O serviço já está em execução.</span><span class="sxs-lookup"><span data-stu-id="b72a2-236">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-237">**11**</span><span class="sxs-lookup"><span data-stu-id="b72a2-237">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-238">O banco de dados para adicionar um serviço novo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-238">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-239">**12**</span><span class="sxs-lookup"><span data-stu-id="b72a2-239">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-240">Uma dependência da qual esse serviço depende foi removida do sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-240">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-241">**13**</span><span class="sxs-lookup"><span data-stu-id="b72a2-241">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-242">O serviço não localizou o serviço necessário em um serviço dependente.</span><span class="sxs-lookup"><span data-stu-id="b72a2-242">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-243">**14**</span><span class="sxs-lookup"><span data-stu-id="b72a2-243">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-244">O serviço foi desabilitado do sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-244">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-245">**15**</span><span class="sxs-lookup"><span data-stu-id="b72a2-245">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-246">O serviço não tem a autenticação correta para ser executado no sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-246">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-247">**16**</span><span class="sxs-lookup"><span data-stu-id="b72a2-247">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-248">Este serviço está sendo removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-248">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-249">**17**</span><span class="sxs-lookup"><span data-stu-id="b72a2-249">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-250">O serviço não tem nenhum thread de execução.</span><span class="sxs-lookup"><span data-stu-id="b72a2-250">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-251">**anos**</span><span class="sxs-lookup"><span data-stu-id="b72a2-251">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-252">O serviço tem dependências circulares quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-252">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-253">**aprimora**</span><span class="sxs-lookup"><span data-stu-id="b72a2-253">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-254">Um serviço está sendo executado com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="b72a2-254">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-255">**20**</span><span class="sxs-lookup"><span data-stu-id="b72a2-255">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-256">O nome do serviço tem caracteres inválidos.</span><span class="sxs-lookup"><span data-stu-id="b72a2-256">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-257">**Abril**</span><span class="sxs-lookup"><span data-stu-id="b72a2-257">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-258">Parâmetros inválidos foram passados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-258">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-259">**22**</span><span class="sxs-lookup"><span data-stu-id="b72a2-259">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-260">A conta sob a qual este serviço é executado é inválida ou não tem as permissões para executar o serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-260">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-261">**23**</span><span class="sxs-lookup"><span data-stu-id="b72a2-261">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-262">O serviço existe no banco de dados de serviços disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-262">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b72a2-263">**24**</span><span class="sxs-lookup"><span data-stu-id="b72a2-263">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b72a2-264">O serviço está pausado atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="b72a2-264">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b72a2-265">Comentários</span><span class="sxs-lookup"><span data-stu-id="b72a2-265">Remarks</span></span>

<span data-ttu-id="b72a2-266">Quando um computador é iniciado, todos os serviços de inicialização automática também são iniciados.</span><span class="sxs-lookup"><span data-stu-id="b72a2-266">When a computer starts, all the autostart services also start.</span></span> <span data-ttu-id="b72a2-267">Na ocasião, um desses serviços pode falhar ao iniciar junto com o computador.</span><span class="sxs-lookup"><span data-stu-id="b72a2-267">On occasion, one of these services might fail to start along with the computer.</span></span> <span data-ttu-id="b72a2-268">Quando um serviço falha durante a inicialização do sistema, o computador executa uma ação com base no valor do código de controle de erro do serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-268">When a service fails during system startup, the computer takes action based on the value of the service error control code.</span></span>

<span data-ttu-id="b72a2-269">a maioria dos serviços é instalada usando o código de controle de erro normal.</span><span class="sxs-lookup"><span data-stu-id="b72a2-269">most services are installed using the Normal error control code.</span></span> <span data-ttu-id="b72a2-270">Algumas das exceções, que são instaladas usando o código de erro ignorar, incluem:</span><span class="sxs-lookup"><span data-stu-id="b72a2-270">A few of the exceptions, which are installed using the Ignore error code, include:</span></span>

-   <span data-ttu-id="b72a2-271">Serviço de Replicação de Arquivos</span><span class="sxs-lookup"><span data-stu-id="b72a2-271">File Replication Service</span></span>
-   <span data-ttu-id="b72a2-272">Cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="b72a2-272">Smart Card</span></span>
-   <span data-ttu-id="b72a2-273">Logon Secundário</span><span class="sxs-lookup"><span data-stu-id="b72a2-273">Secondary Logon</span></span>
-   <span data-ttu-id="b72a2-274">WMI</span><span class="sxs-lookup"><span data-stu-id="b72a2-274">WMI</span></span>

<span data-ttu-id="b72a2-275">Para os serviços instalados usando o código de erro de ignorar, nenhuma notificação é dada ao usuário de que o serviço falhou.</span><span class="sxs-lookup"><span data-stu-id="b72a2-275">For the services installed using the Ignore error code, no notification is given to the user that the service has failed.</span></span> <span data-ttu-id="b72a2-276">Se preferir a notificação na tela informando que um serviço não pôde ser iniciado, você poderá usar o WMI para alterar o código de controle de erro.</span><span class="sxs-lookup"><span data-stu-id="b72a2-276">If you prefer on-screen notification that a service could not start, you can use WMI to change the error control code.</span></span> <span data-ttu-id="b72a2-277">Códigos de controle de erro se aplicam somente à inicialização do computador; os códigos de controle de erro não serão usados se você parar e, em seguida, tentar reiniciar um serviço depois que o computador estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="b72a2-277">Error control codes apply only to computer startup; error control codes are not used if you stop and then attempt to restart a service after the computer is running.</span></span>

<span data-ttu-id="b72a2-278">Na ocasião, talvez seja necessário alterar a conta sob a qual um determinado serviço é executado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-278">On occasion, you might need to change the account under which a given service runs.</span></span> <span data-ttu-id="b72a2-279">Por exemplo, você pode executar um serviço em uma conta administrativa.</span><span class="sxs-lookup"><span data-stu-id="b72a2-279">For example, you might run a service under an administrative account.</span></span> <span data-ttu-id="b72a2-280">Como isso pode criar uma vulnerabilidade de segurança, você pode alternar o serviço para uma conta com menos privilégios.</span><span class="sxs-lookup"><span data-stu-id="b72a2-280">Because this can create a security vulnerability, you might switch the service to an account with fewer privileges.</span></span> <span data-ttu-id="b72a2-281">Como alternativa, você pode ter serviços em execução em uma conta que está prestes a ser excluída, ou talvez queira garantir que, em todos os servidores, determinados serviços sejam executados em determinadas contas.</span><span class="sxs-lookup"><span data-stu-id="b72a2-281">Alternatively, you might have services running under an account that is about to be deleted, or you might want to ensure that, on all your servers, certain services run under certain accounts.</span></span> <span data-ttu-id="b72a2-282">Você pode usar o método **Change** da classe [**Win32 \_ TerminalService**](win32-terminalservice.md) para configurar os serviços para serem executados em uma conta de usuário especificada.</span><span class="sxs-lookup"><span data-stu-id="b72a2-282">You can use the **Change** method of the [**Win32\_TerminalService**](win32-terminalservice.md) class to configure services to run under a specified user account.</span></span> <span data-ttu-id="b72a2-283">Ao selecionar uma conta, tenha em mente o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b72a2-283">When selecting an account, keep in mind the following:</span></span>

-   <span data-ttu-id="b72a2-284">A conta que está sendo usada como uma conta de serviço deve ter o direito de fazer logon como um serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-284">The account being used as a service account must have the right to log on as a service.</span></span> <span data-ttu-id="b72a2-285">Esse direito pode ser concedido usando Política de Grupo.</span><span class="sxs-lookup"><span data-stu-id="b72a2-285">This right can be granted by using Group Policy.</span></span>
-   <span data-ttu-id="b72a2-286">A conta que está sendo usada como uma conta de serviço não deve ser membro de um grupo local, de domínio ou de administradores de empresa.</span><span class="sxs-lookup"><span data-stu-id="b72a2-286">The account being used as a service account should not be a member of a local, domain, or enterprise Administrators group.</span></span>
-   <span data-ttu-id="b72a2-287">Cada instância de um serviço deve ser executada em uma conta de usuário exclusiva.</span><span class="sxs-lookup"><span data-stu-id="b72a2-287">Each instance of a service should run under a unique user account.</span></span> <span data-ttu-id="b72a2-288">Isso fornece segurança adicional e habilita a auditoria de instâncias de serviço individuais.</span><span class="sxs-lookup"><span data-stu-id="b72a2-288">This provides additional security, and enables the auditing of individual service instances.</span></span>
-   <span data-ttu-id="b72a2-289">Se o serviço for interativo, o serviço deverá ser executado na conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="b72a2-289">If the service is interactive, then the service must run under the LocalSystem account.</span></span>

    <span data-ttu-id="b72a2-290">O LocalSystem é necessário porque apenas uma estação de janela (WinSta0) pode ser visível e interativa por vez.</span><span class="sxs-lookup"><span data-stu-id="b72a2-290">LocalSystem is required because only one window station (WinSta0) can be visible and interactive at a time.</span></span> <span data-ttu-id="b72a2-291">Se um serviço for executado em uma conta diferente de LocalSystem, ele será executado na estação de janela padrão Service-0x03E7 $ \\ , que é uma janela invisível.</span><span class="sxs-lookup"><span data-stu-id="b72a2-291">If a service runs under an account other than LocalSystem, it runs in the Service-0x03e7$\\Default window station, which is an invisible window.</span></span> <span data-ttu-id="b72a2-292">Os serviços em execução nesta estação de janela não podem receber entrada ou exibir a saída.</span><span class="sxs-lookup"><span data-stu-id="b72a2-292">Services running in this window station cannot receive input or display output.</span></span>

<span data-ttu-id="b72a2-293">Quando você atribui uma conta a um serviço, o SCM requer a senha correta para essa conta antes de fazer a atribuição.</span><span class="sxs-lookup"><span data-stu-id="b72a2-293">When you assign an account to a service, the SCM requires the correct password for that account before it makes the assignment.</span></span> <span data-ttu-id="b72a2-294">Se você fornecer uma senha incorreta, o SCM rejeitará a conta.</span><span class="sxs-lookup"><span data-stu-id="b72a2-294">If you supply an incorrect password, the SCM rejects the account.</span></span> <span data-ttu-id="b72a2-295">Se você configurar uma conta de serviço usando a conta LocalSystem, LocalService ou NetworkService, não será necessário fornecer uma senha de conta, pois essas contas não têm senhas.</span><span class="sxs-lookup"><span data-stu-id="b72a2-295">If you configure a service account using the LocalSystem, LocalService, or NetworkService account, you do not need to supply an account password because these accounts do not have passwords.</span></span>

<span data-ttu-id="b72a2-296">O SCM armazena a senha da conta no banco de dados de serviços.</span><span class="sxs-lookup"><span data-stu-id="b72a2-296">The SCM stores the account password in the services database.</span></span> <span data-ttu-id="b72a2-297">No entanto, depois que a senha é atribuída, o SCM não garante que a senha armazenada no banco de dados de serviços e a senha atribuída à conta de usuário no Active Directory continuem a corresponder.</span><span class="sxs-lookup"><span data-stu-id="b72a2-297">After the password is assigned, however, the SCM does not ensure that the password stored in the services database and the password assigned to the user account in Active Directory continue to match.</span></span> <span data-ttu-id="b72a2-298">Consequentemente, uma situação semelhante à seguinte pode ocorrer:</span><span class="sxs-lookup"><span data-stu-id="b72a2-298">Consequently, a situation similar to the following could occur:</span></span>

-   <span data-ttu-id="b72a2-299">. Você configura um serviço para ser executado em uma conta de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="b72a2-299">.You configure a service to run under a particular user account.</span></span>
-   <span data-ttu-id="b72a2-300">O serviço é iniciado sob essa conta usando a senha da conta atual.</span><span class="sxs-lookup"><span data-stu-id="b72a2-300">The service starts up under that account by using the current account password.</span></span>
-   <span data-ttu-id="b72a2-301">Você altera a senha da conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="b72a2-301">You change the password for the user account.</span></span>
-   <span data-ttu-id="b72a2-302">O serviço continua a ser executado.</span><span class="sxs-lookup"><span data-stu-id="b72a2-302">The service continues to run.</span></span> <span data-ttu-id="b72a2-303">No entanto, se o serviço for interrompido, você não poderá reiniciá-lo porque o SCM continua a usar a senha antiga e inválida.</span><span class="sxs-lookup"><span data-stu-id="b72a2-303">However, if the service stops, you cannot restart it because the SCM continues to use the old, invalid password.</span></span> <span data-ttu-id="b72a2-304">Alterar a senha em Active Directory não altera a senha armazenada no banco de dados de serviços.</span><span class="sxs-lookup"><span data-stu-id="b72a2-304">Changing the password in Active Directory does not change the password stored in the services database.</span></span>

<span data-ttu-id="b72a2-305">Se você executar serviços em contas de usuário regulares, precisará atualizar essas senhas de serviço sempre que a senha da conta de usuário for alterada.</span><span class="sxs-lookup"><span data-stu-id="b72a2-305">If you run services under regular user accounts, you need to update those service passwords each time the user account password changes.</span></span> <span data-ttu-id="b72a2-306">Isso pode ser particularmente demorado se você não tiver certeza de quais serviços estão sendo executados nessa conta ou quais computadores têm serviços em execução nessa conta.</span><span class="sxs-lookup"><span data-stu-id="b72a2-306">This can be particularly time-consuming if you are not sure which services are running under that account or which computers have services running under that account.</span></span> <span data-ttu-id="b72a2-307">Felizmente, você pode usar o WMI para verificar as contas de serviço em todos os seus computadores e, se necessário, alterar a senha da conta de serviço.</span><span class="sxs-lookup"><span data-stu-id="b72a2-307">Fortunately, you can use WMI to check the service accounts on all your computers and, if necessary, change the service account password.</span></span>

<span data-ttu-id="b72a2-308">O parâmetro do [**\_ Sqlorder OrderGroup do Win32**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) representa um grupo de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="b72a2-308">The [**Win32\_LoadOrderGroup**](/windows/desktop/CIMWin32Prov/win32-loadordergroup) parameter represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="b72a2-309">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="b72a2-309">The services must be initiated in the order specified by the Load Order Group because the services depend on each other.</span></span> <span data-ttu-id="b72a2-310">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="b72a2-310">These dependent services require the presence of the antecedent services to function correctly.</span></span>

<span data-ttu-id="b72a2-311">Para alterar um serviço de um serviço de rede para um sistema local, os parâmetros *StartName* e *StartPassword* devem ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b72a2-311">To change a service from a network service to a local system the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



<span data-ttu-id="b72a2-312">Para alterar um serviço de um serviço do sistema local para uma rede, os parâmetros *StartName* e *StartPassword* devem ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="b72a2-312">To change a service from a local system service to a network the *StartName* and *StartPassword* parameters should have the following values:</span></span>


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a><span data-ttu-id="b72a2-313">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b72a2-313">Examples</span></span>

<span data-ttu-id="b72a2-314">O VBScript a seguir altera a conta de serviço para que os serviços sejam executados em uma conta de usuário especificada para LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="b72a2-314">The following VBScript changes the service account for services from running under a specified user account to LocalSystem.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change _
 ( , , , , , , ".\LocalSystem" , "")
Next
```



<span data-ttu-id="b72a2-315">O VBScript a seguir altera a senha da conta de serviço para todos os scripts em execução em netsvc</span><span class="sxs-lookup"><span data-stu-id="b72a2-315">The following VBScript changes the service account password for all scripts running under Netsvc</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colServiceList = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a><span data-ttu-id="b72a2-316">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b72a2-316">Requirements</span></span>



| <span data-ttu-id="b72a2-317">Requisito</span><span class="sxs-lookup"><span data-stu-id="b72a2-317">Requirement</span></span> | <span data-ttu-id="b72a2-318">Valor</span><span class="sxs-lookup"><span data-stu-id="b72a2-318">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b72a2-319">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b72a2-319">Minimum supported client</span></span><br/> | <span data-ttu-id="b72a2-320">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b72a2-320">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b72a2-321">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b72a2-321">Minimum supported server</span></span><br/> | <span data-ttu-id="b72a2-322">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b72a2-322">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b72a2-323">Namespace</span><span class="sxs-lookup"><span data-stu-id="b72a2-323">Namespace</span></span><br/>                | <span data-ttu-id="b72a2-324">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="b72a2-324">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b72a2-325">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b72a2-325">Header</span></span><br/>                   | <dl> <span data-ttu-id="b72a2-326"><dt>Mbnapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b72a2-326"><dt>Mbnapi.h</dt></span></span> </dl>     |
| <span data-ttu-id="b72a2-327">MOF</span><span class="sxs-lookup"><span data-stu-id="b72a2-327">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b72a2-328"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b72a2-328"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b72a2-329">DLL</span><span class="sxs-lookup"><span data-stu-id="b72a2-329">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b72a2-330"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b72a2-330"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72a2-331">Confira também</span><span class="sxs-lookup"><span data-stu-id="b72a2-331">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72a2-332">**\_Serviço Win32**</span><span class="sxs-lookup"><span data-stu-id="b72a2-332">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="b72a2-333">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="b72a2-333">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="b72a2-334">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="b72a2-334">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="b72a2-335">Tarefas do WMI: serviços</span><span class="sxs-lookup"><span data-stu-id="b72a2-335">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

