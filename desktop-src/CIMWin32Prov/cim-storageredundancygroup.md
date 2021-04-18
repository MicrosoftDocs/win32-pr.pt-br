---
description: A \_ classe CIM StorageRedundancyGroup representa informações de redundância relacionadas ao armazenamento em massa.
ms.assetid: 6bc81680-672a-4872-8951-11d7f10acbc7
ms.tgt_platform: multiple
title: Classe CIM_StorageRedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageRedundancyGroup
- CIM_StorageRedundancyGroup.Caption
- CIM_StorageRedundancyGroup.Description
- CIM_StorageRedundancyGroup.InstallDate
- CIM_StorageRedundancyGroup.Name
- CIM_StorageRedundancyGroup.Status
- CIM_StorageRedundancyGroup.CreationClassName
- CIM_StorageRedundancyGroup.RedundancyStatus
- CIM_StorageRedundancyGroup.TypeOfAlgorithm
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bef8cb8029c62957446ee5d7aefcf67fe5d7acb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771704"
---
# <a name="cim_storageredundancygroup-class"></a><span data-ttu-id="b8366-103">\_Classe CIM StorageRedundancyGroup</span><span class="sxs-lookup"><span data-stu-id="b8366-103">CIM\_StorageRedundancyGroup class</span></span>

<span data-ttu-id="b8366-104">A classe **CIM \_ StorageRedundancyGroup** representa informações de redundância relacionadas ao armazenamento em massa.</span><span class="sxs-lookup"><span data-stu-id="b8366-104">The **CIM\_StorageRedundancyGroup** class represents mass storage-related redundancy information.</span></span> <span data-ttu-id="b8366-105">Os grupos de redundância de armazenamento são usados para proteger os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8366-105">Storage redundancy groups are used to protect user data.</span></span> <span data-ttu-id="b8366-106">Eles são compostos de uma ou mais extensões físicas ou de uma ou mais extensões físicas de agregação.</span><span class="sxs-lookup"><span data-stu-id="b8366-106">They are made up of one or more physical extents, or one or more aggregate physical extents.</span></span> <span data-ttu-id="b8366-107">Os grupos de redundância de armazenamento podem se sobrepor; no entanto, as extensões subjacentes dentro da sobreposição não devem conter nenhum dado de verificação.</span><span class="sxs-lookup"><span data-stu-id="b8366-107">Storage redundancy groups may overlap; however, the underlying extents within the overlap should not contain any check data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b8366-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b8366-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b8366-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b8366-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b8366-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b8366-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b8366-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b8366-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8366-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8366-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{6D477DBC-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_StorageRedundancyGroup : CIM_RedundancyGroup
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
  uint16   TypeOfAlgorithm;
};
```

## <a name="members"></a><span data-ttu-id="b8366-113">Membros</span><span class="sxs-lookup"><span data-stu-id="b8366-113">Members</span></span>

<span data-ttu-id="b8366-114">A classe **CIM \_ StorageRedundancyGroup** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b8366-114">The **CIM\_StorageRedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="b8366-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b8366-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b8366-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b8366-116">Properties</span></span>

<span data-ttu-id="b8366-117">A classe **CIM \_ StorageRedundancyGroup** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b8366-117">The **CIM\_StorageRedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8366-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b8366-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8366-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b8366-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b8366-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8366-122">A short textual description of the object.</span></span>

<span data-ttu-id="b8366-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8366-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b8366-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8366-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-127">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b8366-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b8366-128">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b8366-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b8366-129">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b8366-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b8366-130">Essa propriedade é herdada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8366-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b8366-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8366-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-134">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b8366-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b8366-135">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8366-135">A textual description of the object.</span></span>

<span data-ttu-id="b8366-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8366-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b8366-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b8366-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b8366-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b8366-141">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b8366-141">Indicates when the object was installed.</span></span> <span data-ttu-id="b8366-142">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="b8366-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b8366-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8366-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b8366-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8366-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-147">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b8366-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b8366-148">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b8366-148">Label by which the object is known.</span></span> <span data-ttu-id="b8366-149">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b8366-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b8366-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8366-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="b8366-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-152">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8366-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8366-154">Informações sobre o estado do grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="b8366-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="b8366-155">Essa propriedade é herdada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8366-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b8366-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b8366-157">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b8366-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8366-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b8366-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b8366-159">Outros.</span><span class="sxs-lookup"><span data-stu-id="b8366-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="b8366-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="b8366-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b8366-161">Toda a redundância configurada está disponível.</span><span class="sxs-lookup"><span data-stu-id="b8366-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="b8366-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundância degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="b8366-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b8366-163">A quantidade reduzida de redundância está disponível devido a algumas falhas.</span><span class="sxs-lookup"><span data-stu-id="b8366-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="b8366-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundância perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="b8366-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b8366-165">A redundância não está disponível devido a um número suficiente de falhas.</span><span class="sxs-lookup"><span data-stu-id="b8366-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="b8366-166">A próxima falha causará falha geral.</span><span class="sxs-lookup"><span data-stu-id="b8366-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b8366-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="b8366-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b8366-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-170">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b8366-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b8366-171">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b8366-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="b8366-172">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="b8366-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b8366-173">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="b8366-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b8366-174">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="b8366-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b8366-175">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b8366-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b8366-176">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b8366-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b8366-177">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b8366-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b8366-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b8366-179">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b8366-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b8366-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b8366-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b8366-181">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b8366-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b8366-182">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b8366-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8366-183">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b8366-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b8366-184">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b8366-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b8366-185">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b8366-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b8366-186">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b8366-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b8366-187">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b8366-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b8366-188">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b8366-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b8366-189">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b8366-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b8366-190">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b8366-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b8366-191">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b8366-191">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b8366-192">**TypeOfAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="b8366-192">**TypeOfAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8366-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b8366-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b8366-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b8366-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8366-195">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Grupo de REDUNDÂNCIA DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="b8366-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Redundancy Group\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="b8366-196">Algoritmo usado para a redundância e reconstrução de dados.</span><span class="sxs-lookup"><span data-stu-id="b8366-196">Algorithm used for data redundancy and reconstruction.</span></span> <span data-ttu-id="b8366-197">O valor 0 não é válido no esquema CIM, pois ele representa que não existe nenhuma redundância no DMI.</span><span class="sxs-lookup"><span data-stu-id="b8366-197">The value 0 is not valid in the CIM schema since it represents that no redundancy exists in DMI.</span></span> <span data-ttu-id="b8366-198">Nesse caso, o objeto não deve ser instanciado.</span><span class="sxs-lookup"><span data-stu-id="b8366-198">In which case, the object should not be instantiated.</span></span>

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="b8366-199">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="b8366-199">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b8366-200">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="b8366-200">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b8366-201">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="b8366-201">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="b8366-202">**Cópia** (3)</span><span class="sxs-lookup"><span data-stu-id="b8366-202">**Copy** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="XOR"></span><span id="xor"></span>

<span data-ttu-id="b8366-203">**XOR** (4)</span><span class="sxs-lookup"><span data-stu-id="b8366-203">**XOR** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="P_Q"></span><span id="p_q"></span>

<span data-ttu-id="b8366-204">**P + Q** (5)</span><span class="sxs-lookup"><span data-stu-id="b8366-204">**P+Q** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S"></span><span id="s"></span>

<span data-ttu-id="b8366-205">**S** (6)</span><span class="sxs-lookup"><span data-stu-id="b8366-205">**S** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="P_S"></span><span id="p_s"></span>

<span data-ttu-id="b8366-206">**P + S** (7)</span><span class="sxs-lookup"><span data-stu-id="b8366-206">**P+S** (7)</span></span>


<span data-ttu-id="b8366-207"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b8366-207"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b8366-208">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8366-208">Remarks</span></span>

<span data-ttu-id="b8366-209">A classe **CIM \_ StorageRedundancyGroup** é derivada de [**\_ RedundancyGroup CIM**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="b8366-209">The **CIM\_StorageRedundancyGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="b8366-210">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b8366-210">WMI does not implement this class.</span></span>

<span data-ttu-id="b8366-211">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b8366-211">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b8366-212">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b8366-212">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8366-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8366-213">Requirements</span></span>



| <span data-ttu-id="b8366-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8366-214">Requirement</span></span> | <span data-ttu-id="b8366-215">Valor</span><span class="sxs-lookup"><span data-stu-id="b8366-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8366-216">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8366-216">Minimum supported client</span></span><br/> | <span data-ttu-id="b8366-217">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b8366-217">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b8366-218">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8366-218">Minimum supported server</span></span><br/> | <span data-ttu-id="b8366-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b8366-219">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b8366-220">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8366-220">Namespace</span></span><br/>                | <span data-ttu-id="b8366-221">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b8366-221">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b8366-222">MOF</span><span class="sxs-lookup"><span data-stu-id="b8366-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8366-223"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8366-223"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8366-224">DLL</span><span class="sxs-lookup"><span data-stu-id="b8366-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8366-225"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8366-225"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8366-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8366-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8366-227">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="b8366-227">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

