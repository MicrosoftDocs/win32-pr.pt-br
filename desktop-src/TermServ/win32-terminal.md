---
title: Classe Win32_Terminal
description: Representa um terminal.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_Terminal Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_Terminal classe, descrita
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ae74003f798049fbdb34c955db3f64112bfcd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085297"
---
# <a name="win32_terminal-class"></a><span data-ttu-id="beadc-105">\_Classe de terminal Win32</span><span class="sxs-lookup"><span data-stu-id="beadc-105">Win32\_Terminal class</span></span>

<span data-ttu-id="beadc-106">A classe WMI de **\_ terminal do Win32** representa um terminal.</span><span class="sxs-lookup"><span data-stu-id="beadc-106">The **Win32\_Terminal** WMI class represents a terminal.</span></span>

<span data-ttu-id="beadc-107">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.</span><span class="sxs-lookup"><span data-stu-id="beadc-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="beadc-108">Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.</span><span class="sxs-lookup"><span data-stu-id="beadc-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="beadc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="beadc-109">Syntax</span></span>

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="beadc-110">Membros</span><span class="sxs-lookup"><span data-stu-id="beadc-110">Members</span></span>

<span data-ttu-id="beadc-111">A **classe \_ terminal do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="beadc-111">The **Win32\_Terminal** class has these types of members:</span></span>

-   [<span data-ttu-id="beadc-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="beadc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="beadc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="beadc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="beadc-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="beadc-114">Methods</span></span>

<span data-ttu-id="beadc-115">A **classe \_ terminal do Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="beadc-115">The **Win32\_Terminal** class has these methods.</span></span>



| <span data-ttu-id="beadc-116">Método</span><span class="sxs-lookup"><span data-stu-id="beadc-116">Method</span></span>                                  | <span data-ttu-id="beadc-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="beadc-117">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beadc-118">**Criada**</span><span class="sxs-lookup"><span data-stu-id="beadc-118">**Create**</span></span>](create-win32-terminal.md) | <span data-ttu-id="beadc-119">Cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e métodos das classes [**\_ TerminalSetting do Win32**](win32-terminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="beadc-119">Creates a terminal with default settings which can be customized by using the properties and methods of the [**Win32\_TerminalSetting**](win32-terminalsetting.md) classes.</span></span><br/> |
| [<span data-ttu-id="beadc-120">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="beadc-120">**Delete**</span></span>](delete-win32-terminal.md) | <span data-ttu-id="beadc-121">Exclui o terminal especificado.</span><span class="sxs-lookup"><span data-stu-id="beadc-121">Deletes the specified terminal.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="beadc-122">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="beadc-122">**Enable**</span></span>](win32-terminal-enable.md) | <span data-ttu-id="beadc-123">Desabilita ou habilita o terminal.</span><span class="sxs-lookup"><span data-stu-id="beadc-123">Disables or enables the terminal.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="beadc-124">**Renomear**</span><span class="sxs-lookup"><span data-stu-id="beadc-124">**Rename**</span></span>](win32-terminal-rename.md) | <span data-ttu-id="beadc-125">Renomeia o terminal.</span><span class="sxs-lookup"><span data-stu-id="beadc-125">Renames the terminal.</span></span><br/>                                                                                                                                                        |



 

### <a name="properties"></a><span data-ttu-id="beadc-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="beadc-126">Properties</span></span>

<span data-ttu-id="beadc-127">A **classe \_ terminal do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="beadc-127">The **Win32\_Terminal** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="beadc-128">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="beadc-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="beadc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="beadc-131">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="beadc-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="beadc-132">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="beadc-132">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="beadc-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="beadc-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="beadc-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="beadc-134">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="beadc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="beadc-137">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="beadc-137">Description of the object.</span></span>

<span data-ttu-id="beadc-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="beadc-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="beadc-139">**fEnableTerminal**</span><span class="sxs-lookup"><span data-stu-id="beadc-139">**fEnableTerminal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="beadc-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="beadc-142">Especifica se o terminal especificado está desabilitado ou habilitado.</span><span class="sxs-lookup"><span data-stu-id="beadc-142">Specifies whether the specified terminal is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="beadc-143"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="beadc-143"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="beadc-144">O terminal está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="beadc-144">The terminal is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="beadc-145"><span id="TRUE"></span><span id="true"></span>**Verdadeiro** (1)</span><span class="sxs-lookup"><span data-stu-id="beadc-145"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="beadc-146">O terminal está habilitado.</span><span class="sxs-lookup"><span data-stu-id="beadc-146">The terminal is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="beadc-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="beadc-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-148">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="beadc-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="beadc-150">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="beadc-150">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="beadc-151">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="beadc-151">The date the object was installed.</span></span> <span data-ttu-id="beadc-152">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="beadc-152">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="beadc-153">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="beadc-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="beadc-154">**LoggedOnUsers**</span><span class="sxs-lookup"><span data-stu-id="beadc-154">**LoggedOnUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-155">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="beadc-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="beadc-157">Número de sessões conectadas para o terminal.</span><span class="sxs-lookup"><span data-stu-id="beadc-157">Number of logged-on sessions for the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="beadc-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="beadc-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="beadc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="beadc-161">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="beadc-161">The name of the object.</span></span>

<span data-ttu-id="beadc-162">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="beadc-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="beadc-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="beadc-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="beadc-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="beadc-166">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="beadc-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="beadc-167">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="beadc-167">Current status of the object.</span></span> <span data-ttu-id="beadc-168">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="beadc-168">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="beadc-169">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="beadc-169">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="beadc-170">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="beadc-170">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="beadc-171">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="beadc-171">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="beadc-172">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="beadc-172">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="beadc-173">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="beadc-173">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="beadc-174">("OK")</span><span class="sxs-lookup"><span data-stu-id="beadc-174">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-175">("Erro")</span><span class="sxs-lookup"><span data-stu-id="beadc-175">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-176">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="beadc-176">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-177">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="beadc-177">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-178">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="beadc-178">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-179">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="beadc-179">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-180">("Parando")</span><span class="sxs-lookup"><span data-stu-id="beadc-180">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="beadc-181">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="beadc-181">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="beadc-182">**Terminalname**</span><span class="sxs-lookup"><span data-stu-id="beadc-182">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="beadc-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="beadc-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="beadc-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="beadc-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="beadc-185">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="beadc-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="beadc-186">O nome exclusivo que identifica a instância do terminal.</span><span class="sxs-lookup"><span data-stu-id="beadc-186">The unique name that identifies the instance of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="beadc-187">Comentários</span><span class="sxs-lookup"><span data-stu-id="beadc-187">Remarks</span></span>

<span data-ttu-id="beadc-188">**Win32 \_ O terminal** é associado [**ao Win32 \_ TerminalSetting**](win32-terminalsetting.md) como a propriedade **Element** da Associação [**Win32 \_ TerminalTerminalSetting**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="beadc-188">**Win32\_Terminal** is associated with [**Win32\_TerminalSetting**](win32-terminalsetting.md) as the **Element** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="beadc-189">As classes a seguir são subclasses da classe de **\_ terminal do Win32** : [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md), [**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md), [**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), Win32 TSClientSetting, [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)e [**Win32 \_ TSAccount**](win32-tsaccount.md). [**\_**](win32-tsclientsetting.md)</span><span class="sxs-lookup"><span data-stu-id="beadc-189">The following classes are subclasses of the **Win32\_Terminal** class: [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32\_TSLogonSetting**](win32-tslogonsetting.md), [**Win32\_TSSessionSetting**](win32-tssessionsetting.md), [**Win32\_TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32\_TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32\_TSClientSetting**](win32-tsclientsetting.md), [**Win32\_TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32\_TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32\_TSPermissionsSetting**](win32-tspermissionssetting.md), and [**Win32\_TSAccount**](win32-tsaccount.md).</span></span>

<span data-ttu-id="beadc-190">Observe que o WinStations associado à sessão de console não pode acessar os métodos e as propriedades dessa classe.</span><span class="sxs-lookup"><span data-stu-id="beadc-190">Note that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="beadc-191">Se for feita uma tentativa de fazer isso especificando "console" como o valor da propriedade **terminalname** , os métodos desse objeto retornam **WBEM \_ E \_ sem \_ suporte**.</span><span class="sxs-lookup"><span data-stu-id="beadc-191">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="beadc-192">Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="beadc-192">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="beadc-193">Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote.</span><span class="sxs-lookup"><span data-stu-id="beadc-193">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="beadc-194">Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**.</span><span class="sxs-lookup"><span data-stu-id="beadc-194">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="beadc-195">Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6.</span><span class="sxs-lookup"><span data-stu-id="beadc-195">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="beadc-196">O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.</span><span class="sxs-lookup"><span data-stu-id="beadc-196">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="beadc-197">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="beadc-197">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="beadc-198">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="beadc-198">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="beadc-199">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="beadc-199">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="beadc-200">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="beadc-200">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="beadc-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beadc-201">Requirements</span></span>



| <span data-ttu-id="beadc-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="beadc-202">Requirement</span></span> | <span data-ttu-id="beadc-203">Valor</span><span class="sxs-lookup"><span data-stu-id="beadc-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beadc-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beadc-204">Minimum supported client</span></span><br/> | <span data-ttu-id="beadc-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="beadc-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="beadc-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beadc-206">Minimum supported server</span></span><br/> | <span data-ttu-id="beadc-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="beadc-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="beadc-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="beadc-208">Namespace</span></span><br/>                | <span data-ttu-id="beadc-209">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="beadc-209">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="beadc-210">MOF</span><span class="sxs-lookup"><span data-stu-id="beadc-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beadc-211"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="beadc-211"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="beadc-212">DLL</span><span class="sxs-lookup"><span data-stu-id="beadc-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beadc-213"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beadc-213"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beadc-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="beadc-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beadc-215">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="beadc-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="beadc-216">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="beadc-216">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="beadc-217">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="beadc-217">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> </dl>

 

