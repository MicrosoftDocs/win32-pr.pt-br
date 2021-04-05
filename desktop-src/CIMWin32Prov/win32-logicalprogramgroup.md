---
description: O Win32 \_ LogicalProgramGroup&\# 8194; A classe WMI representa um grupo de programas em um sistema de computador que executa o Windows. Por exemplo, acessórios ou inicialização.
ms.assetid: e05b512d-92ab-4864-b8df-f4a8b66761c9
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroup
- Win32_LogicalProgramGroup.Caption
- Win32_LogicalProgramGroup.Description
- Win32_LogicalProgramGroup.InstallDate
- Win32_LogicalProgramGroup.Status
- Win32_LogicalProgramGroup.GroupName
- Win32_LogicalProgramGroup.Name
- Win32_LogicalProgramGroup.UserName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db7c7484489ecbc87e908dc6eb1c3de156cda665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826580"
---
# <a name="win32_logicalprogramgroup-class"></a><span data-ttu-id="247ad-104">\_Classe Win32 LogicalProgramGroup</span><span class="sxs-lookup"><span data-stu-id="247ad-104">Win32\_LogicalProgramGroup class</span></span>

<span data-ttu-id="247ad-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroup do Win32** representa um grupo de programas em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="247ad-105">The **Win32\_LogicalProgramGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a program group in a computer system running Windows.</span></span> <span data-ttu-id="247ad-106">Por exemplo, acessórios ou inicialização.</span><span class="sxs-lookup"><span data-stu-id="247ad-106">For example, Accessories or Startup.</span></span>

<span data-ttu-id="247ad-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="247ad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="247ad-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="247ad-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="247ad-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="247ad-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{D52706F2-8045-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroup : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   GroupName;
  string   Name;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="247ad-110">Membros</span><span class="sxs-lookup"><span data-stu-id="247ad-110">Members</span></span>

<span data-ttu-id="247ad-111">A classe **Win32 \_ LogicalProgramGroup** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="247ad-111">The **Win32\_LogicalProgramGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="247ad-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="247ad-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="247ad-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="247ad-113">Properties</span></span>

<span data-ttu-id="247ad-114">A classe **Win32 \_ LogicalProgramGroup** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="247ad-114">The **Win32\_LogicalProgramGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="247ad-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="247ad-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="247ad-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="247ad-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="247ad-119">A short textual description of the object.</span></span>

<span data-ttu-id="247ad-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="247ad-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="247ad-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="247ad-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="247ad-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-124">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="247ad-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="247ad-125">A textual description of the object.</span></span>

<span data-ttu-id="247ad-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="247ad-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="247ad-127">**GroupName**</span><span class="sxs-lookup"><span data-stu-id="247ad-127">**GroupName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="247ad-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="247ad-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-131">Nome do grupo de programas do Windows.</span><span class="sxs-lookup"><span data-stu-id="247ad-131">Name of the Windows program group.</span></span> <span data-ttu-id="247ad-132">Os grupos de programas são implementados como pastas de arquivos no Win32.</span><span class="sxs-lookup"><span data-stu-id="247ad-132">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="247ad-133">Exemplo: "ferramentas do sistema de acessórios \\ "</span><span class="sxs-lookup"><span data-stu-id="247ad-133">Example: "Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="247ad-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="247ad-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-135">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="247ad-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="247ad-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-138">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="247ad-138">Indicates when the object was installed.</span></span> <span data-ttu-id="247ad-139">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="247ad-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="247ad-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="247ad-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="247ad-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="247ad-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="247ad-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-144">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue classe Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="247ad-144">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-145">Nome atribuído pelo usuário seguido pelo nome do grupo.</span><span class="sxs-lookup"><span data-stu-id="247ad-145">User-assigned name followed by the group name.</span></span> <span data-ttu-id="247ad-146">Os grupos de programas são implementados como pastas de arquivos no Win32.</span><span class="sxs-lookup"><span data-stu-id="247ad-146">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="247ad-147">Exemplo: "todos os usuários: \\ Ferramentas do sistema de acessórios"</span><span class="sxs-lookup"><span data-stu-id="247ad-147">Example: "All Users:Accessories\\System Tools"</span></span>

</dd> <dt>

<span data-ttu-id="247ad-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="247ad-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="247ad-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="247ad-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-152">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="247ad-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="247ad-153">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="247ad-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="247ad-154">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="247ad-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="247ad-155">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="247ad-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="247ad-156">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="247ad-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="247ad-157">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="247ad-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="247ad-158">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="247ad-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="247ad-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="247ad-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="247ad-160">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="247ad-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="247ad-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="247ad-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="247ad-162">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="247ad-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="247ad-163">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="247ad-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="247ad-164">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="247ad-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="247ad-165">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="247ad-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="247ad-166">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="247ad-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="247ad-167">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="247ad-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="247ad-168">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="247ad-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="247ad-169">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="247ad-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="247ad-170">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="247ad-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="247ad-171">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="247ad-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="247ad-172">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="247ad-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="247ad-173">**UserName**</span><span class="sxs-lookup"><span data-stu-id="247ad-173">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="247ad-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="247ad-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="247ad-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="247ad-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="247ad-176">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="247ad-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="247ad-177">Usuários que podem acessar o grupo de programas do Windows.</span><span class="sxs-lookup"><span data-stu-id="247ad-177">Users who can access the Windows program group.</span></span> <span data-ttu-id="247ad-178">Os grupos de programas são implementados como pastas de arquivos no Win32.</span><span class="sxs-lookup"><span data-stu-id="247ad-178">Program groups are implemented as file folders in Win32.</span></span>

<span data-ttu-id="247ad-179">Exemplo: "todos os usuários"</span><span class="sxs-lookup"><span data-stu-id="247ad-179">Example: "All Users"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="247ad-180">Comentários</span><span class="sxs-lookup"><span data-stu-id="247ad-180">Remarks</span></span>

<span data-ttu-id="247ad-181">A classe **Win32 \_ LogicalProgramGroup** é derivada de [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="247ad-181">The **Win32\_LogicalProgramGroup** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="247ad-182">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="247ad-182">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="247ad-183">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="247ad-183">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="247ad-184">Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="247ad-184">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="247ad-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="247ad-185">Requirements</span></span>



| <span data-ttu-id="247ad-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="247ad-186">Requirement</span></span> | <span data-ttu-id="247ad-187">Valor</span><span class="sxs-lookup"><span data-stu-id="247ad-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="247ad-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="247ad-188">Minimum supported client</span></span><br/> | <span data-ttu-id="247ad-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="247ad-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="247ad-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="247ad-190">Minimum supported server</span></span><br/> | <span data-ttu-id="247ad-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="247ad-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="247ad-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="247ad-192">Namespace</span></span><br/>                | <span data-ttu-id="247ad-193">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="247ad-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="247ad-194">MOF</span><span class="sxs-lookup"><span data-stu-id="247ad-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="247ad-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="247ad-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="247ad-196">DLL</span><span class="sxs-lookup"><span data-stu-id="247ad-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="247ad-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="247ad-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="247ad-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="247ad-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="247ad-199">**\_ProgramGroupOrItem Win32**</span><span class="sxs-lookup"><span data-stu-id="247ad-199">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="247ad-200">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="247ad-200">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

