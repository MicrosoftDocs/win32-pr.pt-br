---
title: Classe Win32_TSSessionSetting
description: Define as definições de configuração para a classe de terminal do Win32, \_ tais como limites de tempo e ações de desconexão e reconexão.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSSessionSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSSessionSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499774"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="aee53-105">\_Classe Win32 TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="aee53-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="aee53-106">A classe WMI **\_ TSSessionSetting do Win32** define definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , tais como limites de tempo e ações de desconexão e reconexão.</span><span class="sxs-lookup"><span data-stu-id="aee53-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="aee53-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="aee53-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="aee53-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="aee53-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee53-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aee53-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="aee53-110">Membros</span><span class="sxs-lookup"><span data-stu-id="aee53-110">Members</span></span>

<span data-ttu-id="aee53-111">A classe **Win32 \_ TSSessionSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aee53-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="aee53-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="aee53-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="aee53-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aee53-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aee53-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="aee53-114">Methods</span></span>

<span data-ttu-id="aee53-115">A classe **Win32 \_ TSSessionSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="aee53-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="aee53-116">Método</span><span class="sxs-lookup"><span data-stu-id="aee53-116">Method</span></span>                                                              | <span data-ttu-id="aee53-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="aee53-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="aee53-118">**BrokenConnection**</span><span class="sxs-lookup"><span data-stu-id="aee53-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="aee53-119">Define as propriedades de conexão desfeitas incluídas nesta classe.</span><span class="sxs-lookup"><span data-stu-id="aee53-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="aee53-120">**Limite de**</span><span class="sxs-lookup"><span data-stu-id="aee53-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="aee53-121">Define as propriedades de limite de tempo incluídas nesta classe.</span><span class="sxs-lookup"><span data-stu-id="aee53-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="aee53-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aee53-122">Properties</span></span>

<span data-ttu-id="aee53-123">A classe **Win32 \_ TSSessionSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aee53-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aee53-124">**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="aee53-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-127">A quantidade máxima de tempo, em milissegundos, alocada a uma sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="aee53-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="aee53-128">Um valor de 0 especifica uma quantidade infinita de tempo.</span><span class="sxs-lookup"><span data-stu-id="aee53-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="aee53-129">**BrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="aee53-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-132">A ação que o servidor executa na sessão quando uma conexão é interrompida devido a perda de rede ou limites de tempo excedidos.</span><span class="sxs-lookup"><span data-stu-id="aee53-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="aee53-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)</span><span class="sxs-lookup"><span data-stu-id="aee53-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-134">O usuário está desconectado da sessão.</span><span class="sxs-lookup"><span data-stu-id="aee53-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="aee53-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (1)</span><span class="sxs-lookup"><span data-stu-id="aee53-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-136">A sessão é excluída permanentemente do servidor.</span><span class="sxs-lookup"><span data-stu-id="aee53-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-137">**BrokenConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="aee53-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-138">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="aee53-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aee53-140">A política que o servidor usa para determinar quando interromper uma conexão devido à perda de rede ou a limites de tempo excedidos.</span><span class="sxs-lookup"><span data-stu-id="aee53-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="aee53-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)</span><span class="sxs-lookup"><span data-stu-id="aee53-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-142">As configurações da política de desconexão do usuário são substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="aee53-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="aee53-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)</span><span class="sxs-lookup"><span data-stu-id="aee53-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-144">As configurações da política de desconexão do usuário estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="aee53-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-145">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="aee53-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aee53-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee53-148">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="aee53-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="aee53-149">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="aee53-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="aee53-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee53-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee53-151">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aee53-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aee53-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-154">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="aee53-154">Description of the object.</span></span>

<span data-ttu-id="aee53-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee53-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee53-156">**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="aee53-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-159">O intervalo de tempo, em milissegundos, após o qual uma sessão desconectada é encerrada.</span><span class="sxs-lookup"><span data-stu-id="aee53-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="aee53-160">Um valor de 0 especifica uma quantidade infinita de tempo.</span><span class="sxs-lookup"><span data-stu-id="aee53-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="aee53-161">**EnableTimeoutWarning**</span><span class="sxs-lookup"><span data-stu-id="aee53-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="aee53-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aee53-164">Habilita o aviso de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="aee53-164">Enables the timeout warning.</span></span>

<span data-ttu-id="aee53-165">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Esta propriedade não está disponível.</span><span class="sxs-lookup"><span data-stu-id="aee53-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="aee53-166">**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="aee53-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-167">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-169">O intervalo de tempo, em milissegundos, após o qual uma sessão ociosa é encerrada.</span><span class="sxs-lookup"><span data-stu-id="aee53-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="aee53-170">Um valor de 0 especifica uma quantidade infinita de tempo.</span><span class="sxs-lookup"><span data-stu-id="aee53-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="aee53-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aee53-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-172">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aee53-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee53-174">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="aee53-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="aee53-175">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="aee53-175">The date the object was installed.</span></span> <span data-ttu-id="aee53-176">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="aee53-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="aee53-177">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee53-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee53-178">**Nome**</span><span class="sxs-lookup"><span data-stu-id="aee53-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aee53-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-181">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="aee53-181">The name of the object.</span></span>

<span data-ttu-id="aee53-182">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee53-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee53-183">**PolicySourceActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="aee53-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-184">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-186">Indica se a propriedade **ActiveSessionLimit** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="aee53-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="aee53-187">0</span><span class="sxs-lookup"><span data-stu-id="aee53-187">0</span></span>
</dt> <dd>

<span data-ttu-id="aee53-188">Servidor</span><span class="sxs-lookup"><span data-stu-id="aee53-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="aee53-189">1</span><span class="sxs-lookup"><span data-stu-id="aee53-189">1</span></span>
</dt> <dd>

<span data-ttu-id="aee53-190">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="aee53-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="aee53-191">2</span><span class="sxs-lookup"><span data-stu-id="aee53-191">2</span></span>
</dt> <dd>

<span data-ttu-id="aee53-192">Padrão</span><span class="sxs-lookup"><span data-stu-id="aee53-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-193">**PolicySourceBrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="aee53-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-194">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-196">Indica se a propriedade **BrokenConnectionAction** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="aee53-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="aee53-197">0</span><span class="sxs-lookup"><span data-stu-id="aee53-197">0</span></span>
</dt> <dd>

<span data-ttu-id="aee53-198">Servidor</span><span class="sxs-lookup"><span data-stu-id="aee53-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="aee53-199">1</span><span class="sxs-lookup"><span data-stu-id="aee53-199">1</span></span>
</dt> <dd>

<span data-ttu-id="aee53-200">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="aee53-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="aee53-201">2</span><span class="sxs-lookup"><span data-stu-id="aee53-201">2</span></span>
</dt> <dd>

<span data-ttu-id="aee53-202">Padrão</span><span class="sxs-lookup"><span data-stu-id="aee53-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-203">**PolicySourceDisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="aee53-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-204">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-206">Indica se a propriedade **DisconnectedSessionLimit** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="aee53-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="aee53-207">0</span><span class="sxs-lookup"><span data-stu-id="aee53-207">0</span></span>
</dt> <dd>

<span data-ttu-id="aee53-208">Servidor</span><span class="sxs-lookup"><span data-stu-id="aee53-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="aee53-209">1</span><span class="sxs-lookup"><span data-stu-id="aee53-209">1</span></span>
</dt> <dd>

<span data-ttu-id="aee53-210">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="aee53-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="aee53-211">2</span><span class="sxs-lookup"><span data-stu-id="aee53-211">2</span></span>
</dt> <dd>

<span data-ttu-id="aee53-212">Padrão</span><span class="sxs-lookup"><span data-stu-id="aee53-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-213">**PolicySourceIdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="aee53-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-214">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-216">Indica se a propriedade **IdleSessionLimit** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="aee53-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="aee53-217">0</span><span class="sxs-lookup"><span data-stu-id="aee53-217">0</span></span>
</dt> <dd>

<span data-ttu-id="aee53-218">Servidor</span><span class="sxs-lookup"><span data-stu-id="aee53-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="aee53-219">1</span><span class="sxs-lookup"><span data-stu-id="aee53-219">1</span></span>
</dt> <dd>

<span data-ttu-id="aee53-220">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="aee53-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="aee53-221">2</span><span class="sxs-lookup"><span data-stu-id="aee53-221">2</span></span>
</dt> <dd>

<span data-ttu-id="aee53-222">Padrão</span><span class="sxs-lookup"><span data-stu-id="aee53-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-223">**PolicySourceReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="aee53-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-224">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-226">Indica se a propriedade **ReconnectPolicy** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="aee53-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="aee53-227">0</span><span class="sxs-lookup"><span data-stu-id="aee53-227">0</span></span>
</dt> <dd>

<span data-ttu-id="aee53-228">Servidor</span><span class="sxs-lookup"><span data-stu-id="aee53-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="aee53-229">1</span><span class="sxs-lookup"><span data-stu-id="aee53-229">1</span></span>
</dt> <dd>

<span data-ttu-id="aee53-230">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="aee53-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="aee53-231">2</span><span class="sxs-lookup"><span data-stu-id="aee53-231">2</span></span>
</dt> <dd>

<span data-ttu-id="aee53-232">Padrão</span><span class="sxs-lookup"><span data-stu-id="aee53-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-233">**ReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="aee53-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-234">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-235">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="aee53-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aee53-236">Especifica se um usuário deve usar o cliente anterior para se reconectar a uma sessão desconectada.</span><span class="sxs-lookup"><span data-stu-id="aee53-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="aee53-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Qualquer cliente** (0)</span><span class="sxs-lookup"><span data-stu-id="aee53-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-238">Qualquer cliente será usado para se reconectar.</span><span class="sxs-lookup"><span data-stu-id="aee53-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="aee53-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Cliente anterior** (1)</span><span class="sxs-lookup"><span data-stu-id="aee53-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-240">O cliente anterior usado em uma conexão será usado para se reconectar.</span><span class="sxs-lookup"><span data-stu-id="aee53-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-241">**Status**</span><span class="sxs-lookup"><span data-stu-id="aee53-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aee53-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aee53-244">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="aee53-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="aee53-245">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="aee53-245">Current status of the object.</span></span> <span data-ttu-id="aee53-246">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="aee53-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aee53-247">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="aee53-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aee53-248">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="aee53-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aee53-249">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="aee53-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aee53-250">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="aee53-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aee53-251">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aee53-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="aee53-252">("OK")</span><span class="sxs-lookup"><span data-stu-id="aee53-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-253">("Erro")</span><span class="sxs-lookup"><span data-stu-id="aee53-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-254">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="aee53-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-255">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="aee53-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-256">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="aee53-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-257">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="aee53-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-258">("Parando")</span><span class="sxs-lookup"><span data-stu-id="aee53-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="aee53-259">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="aee53-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aee53-260">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="aee53-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aee53-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aee53-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aee53-263">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="aee53-263">The name of the terminal.</span></span>

<span data-ttu-id="aee53-264">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="aee53-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="aee53-265">**TimeLimitPolicy**</span><span class="sxs-lookup"><span data-stu-id="aee53-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aee53-266">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aee53-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aee53-267">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="aee53-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aee53-268">A política que o servidor usa para determinar os limites de tempo para sessões de usuário.</span><span class="sxs-lookup"><span data-stu-id="aee53-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="aee53-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)</span><span class="sxs-lookup"><span data-stu-id="aee53-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-270">As configurações de política de limites de tempo do usuário estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="aee53-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="aee53-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Substituição do servidor** (1)</span><span class="sxs-lookup"><span data-stu-id="aee53-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="aee53-272">As configurações de política de limites de tempo do usuário são substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="aee53-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aee53-273">Comentários</span><span class="sxs-lookup"><span data-stu-id="aee53-273">Remarks</span></span>

<span data-ttu-id="aee53-274">Lembre-se de que o WinStations associado à sessão de console não pode acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="aee53-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="aee53-275">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade Terminalname, os métodos desse objeto retornarão o **WBEM \_ E não \_ terão \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="aee53-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="aee53-276">Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto com a finalidade de adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="aee53-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="aee53-277">Para se conectar ao namespace " \\ \\ terminal cimv2" raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="aee53-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="aee53-278">Para chamadas C/C++, isso seria um nível de autenticação de **privacidade do PCT no nível do RPC \_ C \_ Authn \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="aee53-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="aee53-279">Para chamadas de script e de Visual Basic, isso seria um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="aee53-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="aee53-280">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="aee53-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="aee53-281">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="aee53-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aee53-282">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="aee53-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aee53-283">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="aee53-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aee53-284">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aee53-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aee53-285">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee53-285">Requirements</span></span>



| <span data-ttu-id="aee53-286">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee53-286">Requirement</span></span> | <span data-ttu-id="aee53-287">Valor</span><span class="sxs-lookup"><span data-stu-id="aee53-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee53-288">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee53-288">Minimum supported client</span></span><br/> | <span data-ttu-id="aee53-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aee53-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aee53-290">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aee53-290">Minimum supported server</span></span><br/> | <span data-ttu-id="aee53-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aee53-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aee53-292">Namespace</span><span class="sxs-lookup"><span data-stu-id="aee53-292">Namespace</span></span><br/>                | <span data-ttu-id="aee53-293">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="aee53-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="aee53-294">MOF</span><span class="sxs-lookup"><span data-stu-id="aee53-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aee53-295"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aee53-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="aee53-296">DLL</span><span class="sxs-lookup"><span data-stu-id="aee53-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee53-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee53-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee53-298">Confira também</span><span class="sxs-lookup"><span data-stu-id="aee53-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee53-299">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="aee53-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="aee53-300">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="aee53-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

