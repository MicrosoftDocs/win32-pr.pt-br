---
description: O Win32 \_ LogicalProgramGroupItem&\# 8194; A classe WMI representa um elemento contido por um \_ LogicalProgramGroup Win32 que não é também outra \_ instância do Win32 LogicalProgramGroup.
ms.assetid: 70b127bf-4e94-4c1a-98ff-909bdfe0f009
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItem
- Win32_LogicalProgramGroupItem.Caption
- Win32_LogicalProgramGroupItem.Description
- Win32_LogicalProgramGroupItem.InstallDate
- Win32_LogicalProgramGroupItem.Status
- Win32_LogicalProgramGroupItem.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1afd78ba17e444520d8dec81eac05fffa103aede
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501106"
---
# <a name="win32_logicalprogramgroupitem-class"></a><span data-ttu-id="cbc62-103">\_Classe Win32 LogicalProgramGroupItem</span><span class="sxs-lookup"><span data-stu-id="cbc62-103">Win32\_LogicalProgramGroupItem class</span></span>

<span data-ttu-id="cbc62-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroupItem do Win32** representa um elemento contido por [**um \_ LogicalProgramGroup Win32**](win32-logicalprogramgroup.md) que não é também outra instância **Win32 \_ LogicalProgramGroup** .</span><span class="sxs-lookup"><span data-stu-id="cbc62-104">The **Win32\_LogicalProgramGroupItem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an element contained by a [**Win32\_LogicalProgramGroup**](win32-logicalprogramgroup.md) that is not also another **Win32\_LogicalProgramGroup** instance.</span></span>

<span data-ttu-id="cbc62-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cbc62-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cbc62-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="cbc62-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc62-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbc62-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{86E30E82-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItem : Win32_ProgramGroupOrItem
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="cbc62-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cbc62-108">Members</span></span>

<span data-ttu-id="cbc62-109">A classe **Win32 \_ LogicalProgramGroupItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cbc62-109">The **Win32\_LogicalProgramGroupItem** class has these types of members:</span></span>

-   [<span data-ttu-id="cbc62-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cbc62-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cbc62-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cbc62-111">Properties</span></span>

<span data-ttu-id="cbc62-112">A classe **Win32 \_ LogicalProgramGroupItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cbc62-112">The **Win32\_LogicalProgramGroupItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cbc62-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cbc62-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbc62-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbc62-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbc62-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cbc62-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cbc62-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cbc62-117">A short textual description of the object.</span></span>

<span data-ttu-id="cbc62-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbc62-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbc62-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbc62-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbc62-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbc62-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbc62-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-122">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="cbc62-122">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cbc62-123">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cbc62-123">A textual description of the object.</span></span>

<span data-ttu-id="cbc62-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbc62-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbc62-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cbc62-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbc62-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cbc62-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbc62-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="cbc62-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cbc62-129">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="cbc62-129">Indicates when the object was installed.</span></span> <span data-ttu-id="cbc62-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="cbc62-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="cbc62-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbc62-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbc62-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cbc62-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbc62-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbc62-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbc62-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-135">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| CWbemProviderGlue Class Methods \| [**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span><span class="sxs-lookup"><span data-stu-id="cbc62-135">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|CWbemProviderGlue Class Methods\|[**GetAllInstances**](/windows/desktop/api/wbemglue/nf-wbemglue-cwbemproviderglue-getallinstances)")</span></span>
</dt> </dl>

<span data-ttu-id="cbc62-136">Instância em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="cbc62-136">Instance within a computer system.</span></span> <span data-ttu-id="cbc62-137">Os grupos de programas são implementados como pastas de arquivos no Win32.</span><span class="sxs-lookup"><span data-stu-id="cbc62-137">Program groups are implemented as file folders in Win32.</span></span> <span data-ttu-id="cbc62-138">Devem ser fornecidos nomes de caminho completos.</span><span class="sxs-lookup"><span data-stu-id="cbc62-138">Full path names should be provided.</span></span>

<span data-ttu-id="cbc62-139">Exemplo: "C: \\ usuários \\ *alguém* \\ AppData \\ roaming \\ do \\ menu Iniciar do Microsoft Windows \\ \\ programas \\ acessórios do bloco de \\ notas. lnk"</span><span class="sxs-lookup"><span data-stu-id="cbc62-139">Example: "C:\\Users\\*someone*\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Accessories\\NotePad.Lnk"</span></span>

</dd> <dt>

<span data-ttu-id="cbc62-140">**Status**</span><span class="sxs-lookup"><span data-stu-id="cbc62-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cbc62-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cbc62-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cbc62-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cbc62-143">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="cbc62-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cbc62-144">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cbc62-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="cbc62-145">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="cbc62-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="cbc62-146">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="cbc62-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="cbc62-147">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="cbc62-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="cbc62-148">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="cbc62-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cbc62-149">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="cbc62-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cbc62-150">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="cbc62-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cbc62-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cbc62-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cbc62-152">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cbc62-152">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cbc62-153">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cbc62-153">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cbc62-154">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="cbc62-154">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cbc62-155">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="cbc62-155">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cbc62-156">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="cbc62-156">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cbc62-157">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="cbc62-157">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cbc62-158">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="cbc62-158">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cbc62-159">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="cbc62-159">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cbc62-160">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="cbc62-160">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cbc62-161">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="cbc62-161">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cbc62-162">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="cbc62-162">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cbc62-163">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="cbc62-163">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cbc62-164">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="cbc62-164">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="cbc62-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="cbc62-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="cbc62-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbc62-166">Remarks</span></span>

<span data-ttu-id="cbc62-167">A classe **Win32 \_ LogicalProgramGroupItem** é derivada de [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md).</span><span class="sxs-lookup"><span data-stu-id="cbc62-167">The **Win32\_LogicalProgramGroupItem** class is derived from [**Win32\_ProgramGroupOrItem**](win32-programgrouporitem.md).</span></span>

<span data-ttu-id="cbc62-168">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="cbc62-168">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="cbc62-169">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="cbc62-169">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="cbc62-170">Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="cbc62-170">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc62-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc62-171">Requirements</span></span>



| <span data-ttu-id="cbc62-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc62-172">Requirement</span></span> | <span data-ttu-id="cbc62-173">Valor</span><span class="sxs-lookup"><span data-stu-id="cbc62-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc62-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbc62-174">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc62-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cbc62-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cbc62-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cbc62-176">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc62-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cbc62-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cbc62-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="cbc62-178">Namespace</span></span><br/>                | <span data-ttu-id="cbc62-179">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cbc62-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cbc62-180">MOF</span><span class="sxs-lookup"><span data-stu-id="cbc62-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbc62-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbc62-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbc62-182">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc62-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc62-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbc62-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc62-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbc62-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc62-185">**\_ProgramGroupOrItem Win32**</span><span class="sxs-lookup"><span data-stu-id="cbc62-185">**Win32\_ProgramGroupOrItem**</span></span>](win32-programgrouporitem.md)
</dt> <dt>

<span data-ttu-id="cbc62-186">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cbc62-186">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

