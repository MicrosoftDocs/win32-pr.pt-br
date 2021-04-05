---
description: Representa uma configuração de ambiente do sistema ou ambiente em um sistema de computador Windows.
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Classe Win32_Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826687"
---
# <a name="win32_environment-class"></a><span data-ttu-id="d7f49-103">\_Classe de ambiente Win32</span><span class="sxs-lookup"><span data-stu-id="d7f49-103">Win32\_Environment class</span></span>

<span data-ttu-id="d7f49-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) do **\_ ambiente Win32** representa uma configuração de ambiente ou ambiente do sistema em um sistema de computador Windows.</span><span class="sxs-lookup"><span data-stu-id="d7f49-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="d7f49-105">Consultar essa classe retorna variáveis de ambiente encontradas em:</span><span class="sxs-lookup"><span data-stu-id="d7f49-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="d7f49-106">**HKEY \_ \_** Ambiente de \\  \\  \\ **controle** \\  \\  CurrentControlSet do sistema de máquina local</span><span class="sxs-lookup"><span data-stu-id="d7f49-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="d7f49-107">e</span><span class="sxs-lookup"><span data-stu-id="d7f49-107">and</span></span>

<span data-ttu-id="d7f49-108">**HKEY \_** \\ Ambiente de **< usuário >** dos usuários \\ </span><span class="sxs-lookup"><span data-stu-id="d7f49-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="d7f49-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d7f49-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d7f49-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="d7f49-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f49-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f49-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="d7f49-112">Membros</span><span class="sxs-lookup"><span data-stu-id="d7f49-112">Members</span></span>

<span data-ttu-id="d7f49-113">A classe de **\_ ambiente Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7f49-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="d7f49-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7f49-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7f49-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7f49-115">Properties</span></span>

<span data-ttu-id="d7f49-116">A classe de **\_ ambiente Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7f49-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d7f49-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="d7f49-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7f49-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7f49-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d7f49-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d7f49-121">A short textual description of the object.</span></span>

<span data-ttu-id="d7f49-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d7f49-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7f49-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7f49-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7f49-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7f49-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-126">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="d7f49-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-127">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d7f49-127">A textual description of the object.</span></span>

<span data-ttu-id="d7f49-128">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d7f49-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7f49-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d7f49-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-130">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d7f49-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7f49-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-132">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="d7f49-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-133">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="d7f49-133">Indicates when the object was installed.</span></span> <span data-ttu-id="d7f49-134">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="d7f49-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d7f49-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d7f49-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7f49-136">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d7f49-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7f49-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d7f49-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-139">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="d7f49-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-140">Cadeia de caracteres que especifica o nome de uma variável de ambiente baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="d7f49-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="d7f49-141">Ao especificar o nome de uma variável que ainda não existe, um aplicativo cria uma nova variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="d7f49-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="d7f49-142">Exemplo: "caminho"</span><span class="sxs-lookup"><span data-stu-id="d7f49-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="d7f49-143">**Status**</span><span class="sxs-lookup"><span data-stu-id="d7f49-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7f49-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7f49-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-146">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="d7f49-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-147">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="d7f49-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="d7f49-148">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="d7f49-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d7f49-149">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="d7f49-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d7f49-150">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="d7f49-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d7f49-151">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="d7f49-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d7f49-152">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="d7f49-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d7f49-153">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="d7f49-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d7f49-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d7f49-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d7f49-155">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d7f49-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d7f49-156">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d7f49-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d7f49-157">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="d7f49-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d7f49-158">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="d7f49-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d7f49-159">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="d7f49-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d7f49-160">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="d7f49-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d7f49-161">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="d7f49-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d7f49-162">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="d7f49-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d7f49-163">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="d7f49-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d7f49-164">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="d7f49-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d7f49-165">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="d7f49-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d7f49-166">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="d7f49-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d7f49-167">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="d7f49-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d7f49-168">**SystemVariable**</span><span class="sxs-lookup"><span data-stu-id="d7f49-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-169">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="d7f49-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7f49-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-171">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| ambiente do Gerenciador de sessão de controle de CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="d7f49-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-172">Indica se a variável é uma variável do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7f49-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="d7f49-173">Uma variável de sistema é definida pelo sistema operacional e é independente das configurações de ambiente do usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f49-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="d7f49-174">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d7f49-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7f49-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7f49-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-177">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("ambiente do Gerenciador de sessão de controle do Win32Registry do \| sistema \\ \\ \\ \\ \\ \\ \\ \\ )</span><span class="sxs-lookup"><span data-stu-id="d7f49-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-178">Nome do proprietário da configuração de ambiente.</span><span class="sxs-lookup"><span data-stu-id="d7f49-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="d7f49-179">Ele é definido como <SYSTEM> para as configurações específicas do sistema baseado no Windows (em oposição a um usuário específico) e <DEFAULT> para as configurações de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="d7f49-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="d7f49-180">Exemplo: "JSmith"</span><span class="sxs-lookup"><span data-stu-id="d7f49-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="d7f49-181">**VariableValue**</span><span class="sxs-lookup"><span data-stu-id="d7f49-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7f49-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d7f49-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-183">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d7f49-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d7f49-184">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| ambiente do Gerenciador de sessão de controle de CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \\ \\ ")</span><span class="sxs-lookup"><span data-stu-id="d7f49-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="d7f49-185">Variável de espaço reservado de uma variável de ambiente baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="d7f49-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="d7f49-186">Informações como o diretório do sistema de arquivos podem mudar de computador para computador.</span><span class="sxs-lookup"><span data-stu-id="d7f49-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="d7f49-187">O sistema operacional substitui espaços reservados para eles.</span><span class="sxs-lookup"><span data-stu-id="d7f49-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="d7f49-188">Exemplo: "% SystemRoot%"</span><span class="sxs-lookup"><span data-stu-id="d7f49-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7f49-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7f49-189">Remarks</span></span>

<span data-ttu-id="d7f49-190">A classe de **\_ ambiente do Win32** é derivada do [**CIM \_ SystemResource**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="d7f49-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="d7f49-191">Você pode usar essa classe para localizar os caminhos de pastas especiais, como a pasta do sistema ou os arquivos de programas em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d7f49-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="d7f49-192">Alguns exemplos são: WINDIR, SystemRoot, ProgramFiles e UserProfile.</span><span class="sxs-lookup"><span data-stu-id="d7f49-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="d7f49-193">**Win32 \_** Basicamente, o ambiente retorna o que pode ser encontrado em:</span><span class="sxs-lookup"><span data-stu-id="d7f49-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="d7f49-194">**HKEY \_ \_** Ambiente de \\  \\  \\ **controle** \\  \\  CurrentControlSet do sistema de máquina local</span><span class="sxs-lookup"><span data-stu-id="d7f49-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="d7f49-195">e</span><span class="sxs-lookup"><span data-stu-id="d7f49-195">and</span></span>

<span data-ttu-id="d7f49-196">**HKEY \_** \\ Ambiente de **< usuário >** dos usuários \\ </span><span class="sxs-lookup"><span data-stu-id="d7f49-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="d7f49-197">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="d7f49-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="d7f49-198">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="d7f49-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="d7f49-199">Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d7f49-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="d7f49-200">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7f49-200">Examples</span></span>

<span data-ttu-id="d7f49-201">A [lista de variáveis de ambiente em um computador](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl exemplo usa WMI para retornar informações sobre todas as variáveis de ambiente em um computador.</span><span class="sxs-lookup"><span data-stu-id="d7f49-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="d7f49-202">O exemplo de código VBScript a seguir enumera as variáveis de ambiente no computador local.</span><span class="sxs-lookup"><span data-stu-id="d7f49-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="d7f49-203">O exemplo de código VBScript a seguir altera uma variável de ambiente chamada tipo de BUILD \_ para uma entrada de valor pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d7f49-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="d7f49-204">O script supõe que a variável de tipo de compilação \_ já existe.</span><span class="sxs-lookup"><span data-stu-id="d7f49-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="d7f49-205">Se ele não existir, o script será encerrado.</span><span class="sxs-lookup"><span data-stu-id="d7f49-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="d7f49-206">O valor de entrada está marcado: deve ser "Build1", "Build2" ou "Build3", e nenhum outro valor é aceito.</span><span class="sxs-lookup"><span data-stu-id="d7f49-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="d7f49-207">A função [UCase](https://msdn.microsoft.com/library/aa902519.aspx) do VBScript torna a entrada não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d7f49-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="d7f49-208">Se o que é digitado não for um dos três valores aceitáveis, o script será encerrado.</span><span class="sxs-lookup"><span data-stu-id="d7f49-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="d7f49-209">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f49-209">Requirements</span></span>



| <span data-ttu-id="d7f49-210">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f49-210">Requirement</span></span> | <span data-ttu-id="d7f49-211">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f49-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f49-212">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f49-212">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f49-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7f49-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7f49-214">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7f49-214">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f49-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7f49-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7f49-216">Namespace</span><span class="sxs-lookup"><span data-stu-id="d7f49-216">Namespace</span></span><br/>                | <span data-ttu-id="d7f49-217">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d7f49-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d7f49-218">MOF</span><span class="sxs-lookup"><span data-stu-id="d7f49-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7f49-219"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7f49-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7f49-220">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f49-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f49-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7f49-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f49-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7f49-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f49-223">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="d7f49-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="d7f49-224">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7f49-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

