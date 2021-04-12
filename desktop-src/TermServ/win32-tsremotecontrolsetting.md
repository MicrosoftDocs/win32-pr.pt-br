---
title: Classe Win32_TSRemoteControlSetting
description: Define as definições de configuração de controle remoto para a \_ classe terminal do Win32.
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSRemoteControlSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSRemoteControlSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455265"
---
# <a name="win32_tsremotecontrolsetting-class"></a><span data-ttu-id="edbf6-105">\_Classe Win32 TSRemoteControlSetting</span><span class="sxs-lookup"><span data-stu-id="edbf6-105">Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="edbf6-106">A classe WMI **\_ TSRemoteControlSetting do Win32** define as definições de configuração de controle remoto para a classe [**\_ terminal do Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="edbf6-106">The **Win32\_TSRemoteControlSetting** WMI class defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

<span data-ttu-id="edbf6-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="edbf6-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="edbf6-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="edbf6-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbf6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edbf6-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a><span data-ttu-id="edbf6-110">Membros</span><span class="sxs-lookup"><span data-stu-id="edbf6-110">Members</span></span>

<span data-ttu-id="edbf6-111">A classe **Win32 \_ TSRemoteControlSetting** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="edbf6-111">The **Win32\_TSRemoteControlSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="edbf6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="edbf6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="edbf6-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="edbf6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="edbf6-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="edbf6-114">Methods</span></span>

<span data-ttu-id="edbf6-115">A classe **Win32 \_ TSRemoteControlSetting** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="edbf6-115">The **Win32\_TSRemoteControlSetting** class has these methods.</span></span>



| <span data-ttu-id="edbf6-116">Método</span><span class="sxs-lookup"><span data-stu-id="edbf6-116">Method</span></span>                                                              | <span data-ttu-id="edbf6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="edbf6-117">Description</span></span>                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="edbf6-118">**RemoteControl**</span><span class="sxs-lookup"><span data-stu-id="edbf6-118">**RemoteControl**</span></span>](win32-tsremotecontrolsetting-remotecontrol.md) | <span data-ttu-id="edbf6-119">Define a propriedade **LevelOfControl** dessa classe.</span><span class="sxs-lookup"><span data-stu-id="edbf6-119">Sets the **LevelOfControl** property of this class.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="edbf6-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="edbf6-120">Properties</span></span>

<span data-ttu-id="edbf6-121">A classe **Win32 \_ TSRemoteControlSetting** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="edbf6-121">The **Win32\_TSRemoteControlSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="edbf6-122">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="edbf6-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edbf6-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-125">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="edbf6-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-126">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="edbf6-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="edbf6-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="edbf6-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="edbf6-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edbf6-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-131">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="edbf6-131">Description of the object.</span></span>

<span data-ttu-id="edbf6-132">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="edbf6-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="edbf6-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-134">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="edbf6-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-136">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="edbf6-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-137">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="edbf6-137">The date the object was installed.</span></span> <span data-ttu-id="edbf6-138">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="edbf6-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="edbf6-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="edbf6-140">**LevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="edbf6-140">**LevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="edbf6-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-143">Nível de controle da sessão, que especifica se a sessão só será exibida pelo usuário remoto ou exibida e controlada por meio de um teclado e mouse.</span><span class="sxs-lookup"><span data-stu-id="edbf6-143">Level of control for the session, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="edbf6-144">Para obter mais informações, consulte a seção comentários do método [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="edbf6-144">For more information, see the Remarks section of the [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) method.</span></span> <span data-ttu-id="edbf6-145">Os valores a seguir têm suporte.</span><span class="sxs-lookup"><span data-stu-id="edbf6-145">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="edbf6-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** (0)</span><span class="sxs-lookup"><span data-stu-id="edbf6-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-147">O controle remoto está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="edbf6-147">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="edbf6-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="edbf6-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-149">O usuário do controle remoto tem controle total da sessão do usuário, com a permissão do usuário.</span><span class="sxs-lookup"><span data-stu-id="edbf6-149">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="edbf6-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="edbf6-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-151">O usuário do controle remoto tem controle total da sessão do usuário; a permissão do usuário não é necessária.</span><span class="sxs-lookup"><span data-stu-id="edbf6-151">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="edbf6-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="edbf6-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-153">O usuário do controle remoto pode exibir a sessão remotamente, com a permissão do usuário; o usuário remoto não pode controlar ativamente a sessão.</span><span class="sxs-lookup"><span data-stu-id="edbf6-153">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="edbf6-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="edbf6-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-155">O usuário do controle remoto pode exibir a sessão remotamente, mas não controlar ativamente a sessão; a permissão do usuário não é necessária.</span><span class="sxs-lookup"><span data-stu-id="edbf6-155">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="edbf6-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="edbf6-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edbf6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-159">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="edbf6-159">The name of the object.</span></span>

<span data-ttu-id="edbf6-160">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="edbf6-161">**PolicySourceLevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="edbf6-161">**PolicySourceLevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="edbf6-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-164">Indica se a propriedade **LevelOfControl** é configurada pelo servidor, pela política de grupo ou por padrão.</span><span class="sxs-lookup"><span data-stu-id="edbf6-164">Indicates whether the **LevelOfControl** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="edbf6-165">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="edbf6-165">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="edbf6-166">Servidor</span><span class="sxs-lookup"><span data-stu-id="edbf6-166">Server</span></span>

</dd> <dt>

<span data-ttu-id="edbf6-167">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="edbf6-167">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="edbf6-168">Política de grupo</span><span class="sxs-lookup"><span data-stu-id="edbf6-168">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="edbf6-169">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="edbf6-169">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="edbf6-170">Padrão</span><span class="sxs-lookup"><span data-stu-id="edbf6-170">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="edbf6-171">**RemoteControlPolicy**</span><span class="sxs-lookup"><span data-stu-id="edbf6-171">**RemoteControlPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-172">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="edbf6-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-173">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="edbf6-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-174">A política que o servidor usa para recuperar as configurações de controle remoto.</span><span class="sxs-lookup"><span data-stu-id="edbf6-174">The policy the server uses to retrieve the remote control settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="edbf6-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)</span><span class="sxs-lookup"><span data-stu-id="edbf6-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-176">As configurações de controle remoto do usuário estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="edbf6-176">The user's remote control settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="edbf6-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)</span><span class="sxs-lookup"><span data-stu-id="edbf6-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="edbf6-178">As configurações de controle remoto do usuário são substituídas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="edbf6-178">The user's remote control settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="edbf6-179">**Status**</span><span class="sxs-lookup"><span data-stu-id="edbf6-179">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edbf6-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-182">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="edbf6-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-183">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="edbf6-183">Current status of the object.</span></span> <span data-ttu-id="edbf6-184">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="edbf6-184">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="edbf6-185">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="edbf6-185">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="edbf6-186">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="edbf6-186">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="edbf6-187">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="edbf6-187">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="edbf6-188">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="edbf6-188">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="edbf6-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="edbf6-190">("OK")</span><span class="sxs-lookup"><span data-stu-id="edbf6-190">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-191">("Erro")</span><span class="sxs-lookup"><span data-stu-id="edbf6-191">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-192">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="edbf6-192">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-193">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="edbf6-193">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-194">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="edbf6-194">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-195">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="edbf6-195">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-196">("Parando")</span><span class="sxs-lookup"><span data-stu-id="edbf6-196">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="edbf6-197">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="edbf6-197">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="edbf6-198">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="edbf6-198">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edbf6-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="edbf6-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="edbf6-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="edbf6-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="edbf6-201">O nome do terminal.</span><span class="sxs-lookup"><span data-stu-id="edbf6-201">The name of the terminal.</span></span>

<span data-ttu-id="edbf6-202">Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="edbf6-202">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="edbf6-203">Comentários</span><span class="sxs-lookup"><span data-stu-id="edbf6-203">Remarks</span></span>

<span data-ttu-id="edbf6-204">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="edbf6-204">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="edbf6-205">Para chamadas C/C++, isso seria um nível de autenticação de **privacidade do PCT no nível do RPC \_ C \_ Authn \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="edbf6-205">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="edbf6-206">Para chamadas de script e de Visual Basic, isso seria um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="edbf6-206">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="edbf6-207">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="edbf6-207">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="edbf6-208">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="edbf6-208">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="edbf6-209">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="edbf6-209">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="edbf6-210">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="edbf6-210">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="edbf6-211">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="edbf6-211">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="edbf6-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edbf6-212">Requirements</span></span>



| <span data-ttu-id="edbf6-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="edbf6-213">Requirement</span></span> | <span data-ttu-id="edbf6-214">Valor</span><span class="sxs-lookup"><span data-stu-id="edbf6-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edbf6-215">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edbf6-215">Minimum supported client</span></span><br/> | <span data-ttu-id="edbf6-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edbf6-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="edbf6-217">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edbf6-217">Minimum supported server</span></span><br/> | <span data-ttu-id="edbf6-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edbf6-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="edbf6-219">Namespace</span><span class="sxs-lookup"><span data-stu-id="edbf6-219">Namespace</span></span><br/>                | <span data-ttu-id="edbf6-220">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="edbf6-220">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="edbf6-221">MOF</span><span class="sxs-lookup"><span data-stu-id="edbf6-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="edbf6-222"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="edbf6-222"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="edbf6-223">DLL</span><span class="sxs-lookup"><span data-stu-id="edbf6-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edbf6-224"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edbf6-224"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbf6-225">Confira também</span><span class="sxs-lookup"><span data-stu-id="edbf6-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbf6-226">**Terminal do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="edbf6-226">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="edbf6-227">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="edbf6-227">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

