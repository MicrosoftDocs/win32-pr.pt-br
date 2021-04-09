---
description: A \_ classe WMI do OrderGroup do Sqlorder do Win32 representa um grupo de serviços do sistema que definem dependências de execução.
ms.assetid: 0aa3151e-6622-46b4-9050-4e1c4c720902
ms.tgt_platform: multiple
title: Classe Win32_LoadOrderGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroup
- Win32_LoadOrderGroup.Caption
- Win32_LoadOrderGroup.Description
- Win32_LoadOrderGroup.InstallDate
- Win32_LoadOrderGroup.Status
- Win32_LoadOrderGroup.DriverEnabled
- Win32_LoadOrderGroup.GroupOrder
- Win32_LoadOrderGroup.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b81a6cb282018692fb72c8dbfe5ef0c5c74fe815
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089538"
---
# <a name="win32_loadordergroup-class"></a><span data-ttu-id="c3ab1-103">Classe do OrderGroup do Win32 \_</span><span class="sxs-lookup"><span data-stu-id="c3ab1-103">Win32\_LoadOrderGroup class</span></span>

<span data-ttu-id="c3ab1-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) do **OrderGroup do \_ sqlorder do Win32** representa um grupo de serviços do sistema que definem dependências de execução.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-104">The **Win32\_LoadOrderGroup** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a group of system services that define execution dependencies.</span></span> <span data-ttu-id="c3ab1-105">Os serviços devem ser iniciados na ordem especificada pelo grupo de ordem de carregamento, pois os serviços dependem uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-105">The services must be initiated in the order specified by the Load Order Group, as the services are dependent on each other.</span></span> <span data-ttu-id="c3ab1-106">Esses serviços dependentes exigem a presença dos serviços antecedentes para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-106">These dependent services require the presence of the antecedent services to function correctly.</span></span> <span data-ttu-id="c3ab1-107">Os dados nessa classe são derivados do provedor da chave do registro: **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **ServiceGroupOrder**.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-107">The data in this class is derived by the provider from the registry key: **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**ServiceGroupOrder**.</span></span>

<span data-ttu-id="c3ab1-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c3ab1-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ab1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3ab1-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D4-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  DriverEnabled;
  uint32   GroupOrder;
  string   Name;
};
```

## <a name="members"></a><span data-ttu-id="c3ab1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c3ab1-111">Members</span></span>

<span data-ttu-id="c3ab1-112">A classe do **\_ Sqlorder OrderGroup do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c3ab1-112">The **Win32\_LoadOrderGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="c3ab1-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c3ab1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3ab1-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c3ab1-114">Properties</span></span>

<span data-ttu-id="c3ab1-115">A classe do **\_ Sqlorder OrderGroup do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-115">The **Win32\_LoadOrderGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3ab1-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-120">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-120">A short textual description of the object.</span></span>

<span data-ttu-id="c3ab1-121">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3ab1-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-125">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-125">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-126">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-126">A textual description of the object.</span></span>

<span data-ttu-id="c3ab1-127">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3ab1-128">**DriverEnabled**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-128">**DriverEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-132">Indica se este grupo de ordem de carregamento pode incluir drivers juntamente com serviços do sistema.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-132">Indicates whether this load order group can include drivers along with system services.</span></span>

</dd> <dt>

<span data-ttu-id="c3ab1-133">**GroupOrder**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-133">**GroupOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-136">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-137">Sequência em que esse grupo de serviços é carregado no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-137">Sequence in which this group of services is loaded onto the operating system.</span></span>

<span data-ttu-id="c3ab1-138">Exemplo: 2</span><span class="sxs-lookup"><span data-stu-id="c3ab1-138">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="c3ab1-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-142">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-143">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-143">Indicates when the object was installed.</span></span> <span data-ttu-id="c3ab1-144">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-144">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c3ab1-145">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3ab1-146">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-149">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ GroupOrderList")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\GroupOrderList")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-150">Nome do grupo de ordem de carregamento.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-150">Name of the load order group.</span></span>

<span data-ttu-id="c3ab1-151">Exemplo: "disco primário"</span><span class="sxs-lookup"><span data-stu-id="c3ab1-151">Example: "Primary disk"</span></span>

</dd> <dt>

<span data-ttu-id="c3ab1-152">**Status**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-152">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3ab1-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c3ab1-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3ab1-155">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c3ab1-156">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-156">String that indicates the current status of the object.</span></span> <span data-ttu-id="c3ab1-157">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-157">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c3ab1-158">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="c3ab1-158">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c3ab1-159">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-159">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c3ab1-160">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="c3ab1-160">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c3ab1-161">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-161">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c3ab1-162">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-162">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c3ab1-163">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c3ab1-164">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3ab1-164">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c3ab1-165">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-165">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c3ab1-166">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-166">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c3ab1-167">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-167">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c3ab1-168">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-168">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c3ab1-169">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-169">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c3ab1-170">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-170">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c3ab1-171">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-171">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c3ab1-172">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-172">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c3ab1-173">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-173">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c3ab1-174">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-174">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c3ab1-175">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-175">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c3ab1-176">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="c3ab1-176">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="c3ab1-177"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c3ab1-177"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="c3ab1-178">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3ab1-178">Remarks</span></span>

<span data-ttu-id="c3ab1-179">A classe do **\_ OrderGroup do Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-179">The **Win32\_LoadOrderGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c3ab1-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3ab1-180">Requirements</span></span>



| <span data-ttu-id="c3ab1-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3ab1-181">Requirement</span></span> | <span data-ttu-id="c3ab1-182">Valor</span><span class="sxs-lookup"><span data-stu-id="c3ab1-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ab1-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3ab1-183">Minimum supported client</span></span><br/> | <span data-ttu-id="c3ab1-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c3ab1-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c3ab1-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3ab1-185">Minimum supported server</span></span><br/> | <span data-ttu-id="c3ab1-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c3ab1-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c3ab1-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3ab1-187">Namespace</span></span><br/>                | <span data-ttu-id="c3ab1-188">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c3ab1-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c3ab1-189">MOF</span><span class="sxs-lookup"><span data-stu-id="c3ab1-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3ab1-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab1-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3ab1-191">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ab1-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3ab1-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab1-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ab1-193">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3ab1-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ab1-194">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-194">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

<span data-ttu-id="c3ab1-195">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c3ab1-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

