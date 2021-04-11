---
title: Classe Win32_RDCentralPublishedFarm
description: A lista de farms da qual os desktops ou aplicativos foram publicados.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDCentralPublishedFarm Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDCentralPublishedFarm classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454978"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="1b27d-105">\_Classe Win32 RDCentralPublishedFarm</span><span class="sxs-lookup"><span data-stu-id="1b27d-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="1b27d-106">A lista de farms da qual os desktops ou aplicativos foram publicados.</span><span class="sxs-lookup"><span data-stu-id="1b27d-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="1b27d-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1b27d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b27d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b27d-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="1b27d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="1b27d-109">Members</span></span>

<span data-ttu-id="1b27d-110">A classe **Win32 \_ RDCentralPublishedFarm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1b27d-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="1b27d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b27d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1b27d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1b27d-112">Properties</span></span>

<span data-ttu-id="1b27d-113">A classe **Win32 \_ RDCentralPublishedFarm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1b27d-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b27d-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="1b27d-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b27d-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-117">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b27d-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-118">O nome do farm do qual os desktops ou aplicativos foram publicados.</span><span class="sxs-lookup"><span data-stu-id="1b27d-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1b27d-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b27d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="1b27d-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-123">Breve descrição (cadeia de caracteres de uma linha) do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b27d-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="1b27d-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b27d-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1b27d-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b27d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-128">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b27d-128">Description of the object.</span></span>

<span data-ttu-id="1b27d-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b27d-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-130">**Farmtype**</span><span class="sxs-lookup"><span data-stu-id="1b27d-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b27d-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b27d-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-133">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1b27d-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-134">O tipo de farm:</span><span class="sxs-lookup"><span data-stu-id="1b27d-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="1b27d-135">**RDSH** (0)</span><span class="sxs-lookup"><span data-stu-id="1b27d-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="1b27d-136">**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="1b27d-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="1b27d-137">**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="1b27d-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="1b27d-138">**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="1b27d-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b27d-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1b27d-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1b27d-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b27d-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-142">Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")</span><span class="sxs-lookup"><span data-stu-id="1b27d-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-143">A data em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1b27d-143">The date the object was installed.</span></span> <span data-ttu-id="1b27d-144">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="1b27d-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1b27d-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b27d-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-146">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="1b27d-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-147">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b27d-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b27d-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-149">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1b27d-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-150">**true** se um usuário precisar ser adicionado ao grupo de Administradores local na conexão; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1b27d-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="1b27d-151">Aplicável somente a tipos de farm ManualPersonalVm e AutoPersonalVM.</span><span class="sxs-lookup"><span data-stu-id="1b27d-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1b27d-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b27d-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-155">O nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b27d-155">The name of the object.</span></span>

<span data-ttu-id="1b27d-156">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b27d-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-157">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="1b27d-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-158">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1b27d-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-159">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b27d-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-160">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1b27d-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-161">**true** para reverter automaticamente a VM para um instantâneo após o logoff do usuário; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1b27d-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="1b27d-162">Aplicável somente a tipos de farm TempVm.</span><span class="sxs-lookup"><span data-stu-id="1b27d-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1b27d-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-165">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b27d-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-166">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1b27d-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-167">O nome do descritor de segurança que controla o acesso ao aplicativo, no formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="1b27d-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="1b27d-168">O uso de uma cadeia de caracteres vazia implica permitir todo o acesso.</span><span class="sxs-lookup"><span data-stu-id="1b27d-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="1b27d-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="1b27d-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b27d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="1b27d-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-173">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1b27d-173">Current status of the object.</span></span> <span data-ttu-id="1b27d-174">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1b27d-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1b27d-175">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1b27d-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1b27d-176">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="1b27d-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1b27d-177">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="1b27d-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1b27d-178">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="1b27d-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1b27d-179">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1b27d-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="1b27d-180">("OK")</span><span class="sxs-lookup"><span data-stu-id="1b27d-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-181">("Erro")</span><span class="sxs-lookup"><span data-stu-id="1b27d-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-182">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="1b27d-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-183">("Desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1b27d-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-184">("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1b27d-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-185">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1b27d-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-186">("Parando")</span><span class="sxs-lookup"><span data-stu-id="1b27d-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="1b27d-187">("Serviço")</span><span class="sxs-lookup"><span data-stu-id="1b27d-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1b27d-188">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="1b27d-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b27d-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1b27d-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-190">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1b27d-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1b27d-191">Qualificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1b27d-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1b27d-192">As configurações do farm de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="1b27d-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b27d-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b27d-193">Requirements</span></span>



| <span data-ttu-id="1b27d-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b27d-194">Requirement</span></span> | <span data-ttu-id="1b27d-195">Valor</span><span class="sxs-lookup"><span data-stu-id="1b27d-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b27d-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b27d-196">Minimum supported client</span></span><br/> | <span data-ttu-id="1b27d-197">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1b27d-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1b27d-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b27d-198">Minimum supported server</span></span><br/> | <span data-ttu-id="1b27d-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b27d-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="1b27d-200">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b27d-200">Namespace</span></span><br/>                | <span data-ttu-id="1b27d-201">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="1b27d-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1b27d-202">MOF</span><span class="sxs-lookup"><span data-stu-id="1b27d-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b27d-203"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b27d-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="1b27d-204">DLL</span><span class="sxs-lookup"><span data-stu-id="1b27d-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b27d-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b27d-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

