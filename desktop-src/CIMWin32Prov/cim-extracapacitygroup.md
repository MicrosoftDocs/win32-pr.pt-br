---
description: A \_ classe CIM ExtraCapacityGroup é derivada de um grupo de redundância que indica que os elementos agregados têm mais capacidade ou capacidade do que o necessário.
ms.assetid: fbbbd6ed-4a67-4917-8b0e-3cba4cac3b45
ms.tgt_platform: multiple
title: Classe CIM_ExtraCapacityGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExtraCapacityGroup
- CIM_ExtraCapacityGroup.Caption
- CIM_ExtraCapacityGroup.Description
- CIM_ExtraCapacityGroup.InstallDate
- CIM_ExtraCapacityGroup.Name
- CIM_ExtraCapacityGroup.Status
- CIM_ExtraCapacityGroup.CreationClassName
- CIM_ExtraCapacityGroup.RedundancyStatus
- CIM_ExtraCapacityGroup.MinNumberNeeded
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78f9aa79cfcc7b93d176859069d1b71f5adf450e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164069"
---
# <a name="cim_extracapacitygroup-class"></a><span data-ttu-id="eea06-103">\_Classe CIM ExtraCapacityGroup</span><span class="sxs-lookup"><span data-stu-id="eea06-103">CIM\_ExtraCapacityGroup class</span></span>

<span data-ttu-id="eea06-104">A classe **CIM \_ ExtraCapacityGroup** é derivada de um grupo de redundância que indica que os elementos agregados têm mais capacidade ou capacidade do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="eea06-104">The **CIM\_ExtraCapacityGroup** class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="eea06-105">Um exemplo desse tipo de redundância é a instalação de N + 1 fontes de alimentação ou ventiladores em um sistema.</span><span class="sxs-lookup"><span data-stu-id="eea06-105">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eea06-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="eea06-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eea06-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eea06-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eea06-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="eea06-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eea06-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="eea06-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea06-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eea06-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{570ED2E8-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ExtraCapacityGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint32   MinNumberNeeded;
};
```

## <a name="members"></a><span data-ttu-id="eea06-111">Membros</span><span class="sxs-lookup"><span data-stu-id="eea06-111">Members</span></span>

<span data-ttu-id="eea06-112">A classe **CIM \_ ExtraCapacityGroup** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="eea06-112">The **CIM\_ExtraCapacityGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="eea06-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eea06-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eea06-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eea06-114">Properties</span></span>

<span data-ttu-id="eea06-115">A classe **CIM \_ ExtraCapacityGroup** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="eea06-115">The **CIM\_ExtraCapacityGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eea06-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="eea06-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eea06-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea06-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="eea06-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="eea06-120">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="eea06-120">A short textual description of the object.</span></span>

<span data-ttu-id="eea06-121">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea06-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="eea06-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eea06-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea06-125">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="eea06-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="eea06-126">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="eea06-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="eea06-127">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="eea06-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="eea06-128">Essa propriedade é herdada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-128">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea06-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="eea06-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eea06-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea06-132">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="eea06-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="eea06-133">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="eea06-133">A textual description of the object.</span></span>

<span data-ttu-id="eea06-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea06-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="eea06-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-136">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="eea06-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea06-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="eea06-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="eea06-139">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="eea06-139">Indicates when the object was installed.</span></span> <span data-ttu-id="eea06-140">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="eea06-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="eea06-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea06-142">**MinNumberNeeded**</span><span class="sxs-lookup"><span data-stu-id="eea06-142">**MinNumberNeeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eea06-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eea06-145">Menor número de elementos que devem estar operacionais para ter redundância.</span><span class="sxs-lookup"><span data-stu-id="eea06-145">Smallest number of elements that must be operational to have redundancy.</span></span> <span data-ttu-id="eea06-146">Por exemplo, em uma relação N + 1 de redundância, essa propriedade deve ser definida igual a N.</span><span class="sxs-lookup"><span data-stu-id="eea06-146">For example, in an N+1 redundancy relationship, this property should be set equal to N.</span></span>

</dd> <dt>

<span data-ttu-id="eea06-147">**Nome**</span><span class="sxs-lookup"><span data-stu-id="eea06-147">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eea06-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea06-150">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="eea06-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="eea06-151">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="eea06-151">Label by which the object is known.</span></span> <span data-ttu-id="eea06-152">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="eea06-152">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="eea06-153">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea06-154">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="eea06-154">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-155">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="eea06-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eea06-157">Informações sobre o estado do grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="eea06-157">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="eea06-158">Essa propriedade é herdada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-158">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eea06-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="eea06-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="eea06-160">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="eea06-160">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="eea06-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="eea06-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="eea06-162">Outros.</span><span class="sxs-lookup"><span data-stu-id="eea06-162">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="eea06-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="eea06-163"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="eea06-164">Toda a redundância configurada está disponível.</span><span class="sxs-lookup"><span data-stu-id="eea06-164">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="eea06-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundância degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="eea06-165"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="eea06-166">A quantidade reduzida de redundância está disponível devido a algumas falhas.</span><span class="sxs-lookup"><span data-stu-id="eea06-166">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="eea06-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundância perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="eea06-167"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="eea06-168">A redundância não está disponível devido a um número suficiente de falhas.</span><span class="sxs-lookup"><span data-stu-id="eea06-168">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="eea06-169">A próxima falha causará falha geral.</span><span class="sxs-lookup"><span data-stu-id="eea06-169">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="eea06-170">**Status**</span><span class="sxs-lookup"><span data-stu-id="eea06-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eea06-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="eea06-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="eea06-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eea06-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eea06-173">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="eea06-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="eea06-174">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="eea06-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="eea06-175">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="eea06-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="eea06-176">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="eea06-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="eea06-177">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="eea06-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="eea06-178">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="eea06-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="eea06-179">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="eea06-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="eea06-180">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="eea06-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="eea06-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="eea06-182">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="eea06-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="eea06-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="eea06-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="eea06-184">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="eea06-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="eea06-185">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="eea06-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="eea06-186">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="eea06-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="eea06-187">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="eea06-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="eea06-188">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="eea06-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="eea06-189">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="eea06-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="eea06-190">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="eea06-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="eea06-191">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="eea06-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="eea06-192">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="eea06-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="eea06-193">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="eea06-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="eea06-194">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="eea06-194">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="eea06-195"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eea06-195"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="eea06-196">Comentários</span><span class="sxs-lookup"><span data-stu-id="eea06-196">Remarks</span></span>

<span data-ttu-id="eea06-197">A classe **CIM \_ ExtraCapacityGroup** é derivada de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="eea06-197">The **CIM\_ExtraCapacityGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="eea06-198">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="eea06-198">WMI does not implement this class.</span></span>

<span data-ttu-id="eea06-199">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="eea06-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eea06-200">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="eea06-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea06-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea06-201">Requirements</span></span>



| <span data-ttu-id="eea06-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea06-202">Requirement</span></span> | <span data-ttu-id="eea06-203">Valor</span><span class="sxs-lookup"><span data-stu-id="eea06-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea06-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eea06-204">Minimum supported client</span></span><br/> | <span data-ttu-id="eea06-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eea06-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eea06-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eea06-206">Minimum supported server</span></span><br/> | <span data-ttu-id="eea06-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eea06-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eea06-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="eea06-208">Namespace</span></span><br/>                | <span data-ttu-id="eea06-209">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eea06-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eea06-210">MOF</span><span class="sxs-lookup"><span data-stu-id="eea06-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eea06-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eea06-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eea06-212">DLL</span><span class="sxs-lookup"><span data-stu-id="eea06-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eea06-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eea06-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea06-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="eea06-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea06-215">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="eea06-215">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

