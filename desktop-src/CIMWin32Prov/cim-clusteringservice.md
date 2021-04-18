---
description: A \_ classe CIM ClusteringService representa a funcionalidade fornecida por um cluster. Por exemplo, a funcionalidade de failover pode ser modelada como um serviço de um cluster de failover.
ms.assetid: 550e3be3-c1e2-4714-b702-49cb1213c65b
ms.tgt_platform: multiple
title: Classe CIM_ClusteringService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusteringService
- CIM_ClusteringService.Caption
- CIM_ClusteringService.Description
- CIM_ClusteringService.InstallDate
- CIM_ClusteringService.Status
- CIM_ClusteringService.CreationClassName
- CIM_ClusteringService.Name
- CIM_ClusteringService.Started
- CIM_ClusteringService.StartMode
- CIM_ClusteringService.SystemCreationClassName
- CIM_ClusteringService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 40dc0ebd8daebb79c323d54591fc16126e0ef97a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748270"
---
# <a name="cim_clusteringservice-class"></a><span data-ttu-id="bd3fa-104">\_Classe CIM ClusteringService</span><span class="sxs-lookup"><span data-stu-id="bd3fa-104">CIM\_ClusteringService class</span></span>

<span data-ttu-id="bd3fa-105">A classe **CIM \_ ClusteringService** representa a funcionalidade fornecida por um cluster.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-105">The **CIM\_ClusteringService** class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="bd3fa-106">Por exemplo, a funcionalidade de failover pode ser modelada como um serviço de um cluster de failover.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-106">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd3fa-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bd3fa-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bd3fa-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bd3fa-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd3fa-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd3fa-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{debac832-6b54-4add-8a62-8d3861b97b1d}"), AMENDMENT]
class CIM_ClusteringService : CIM_Service
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="bd3fa-112">Membros</span><span class="sxs-lookup"><span data-stu-id="bd3fa-112">Members</span></span>

<span data-ttu-id="bd3fa-113">A classe **CIM \_ ClusteringService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bd3fa-113">The **CIM\_ClusteringService** class has these types of members:</span></span>

-   [<span data-ttu-id="bd3fa-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd3fa-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="bd3fa-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bd3fa-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bd3fa-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd3fa-116">Methods</span></span>

<span data-ttu-id="bd3fa-117">A classe **CIM \_ ClusteringService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-117">The **CIM\_ClusteringService** class has these methods.</span></span>



| <span data-ttu-id="bd3fa-118">Método</span><span class="sxs-lookup"><span data-stu-id="bd3fa-118">Method</span></span>                                                                     | <span data-ttu-id="bd3fa-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd3fa-119">Description</span></span>                                                                                                |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd3fa-120">**AddNode**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-120">**AddNode**</span></span>](addnode-method-in-class-cim-clusteringservice.md)           | <span data-ttu-id="bd3fa-121">Método de classe que coloca um novo sistema de computador em um cluster.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-121">Class method that brings a new computer system into a cluster.</span></span> <span data-ttu-id="bd3fa-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-122">Not implemented by WMI.</span></span><br/>          |
| [<span data-ttu-id="bd3fa-123">**EvictNode**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-123">**EvictNode**</span></span>](evictnode-method-in-class-cim-clusteringservice.md)       | <span data-ttu-id="bd3fa-124">Método de classe que remove um sistema de computador de um cluster.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-124">Class method that removes a computer system from a cluster.</span></span> <span data-ttu-id="bd3fa-125">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-125">Not implemented by WMI.</span></span><br/>             |
| [<span data-ttu-id="bd3fa-126">**StartService**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-126">**StartService**</span></span>](startservice-method-in-class-cim-clusteringservice.md) | <span data-ttu-id="bd3fa-127">Método de classe que tenta posicionar o serviço em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-127">Class method that attempts to place the service into its startup state.</span></span> <span data-ttu-id="bd3fa-128">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-128">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="bd3fa-129">**StopService**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-129">**StopService**</span></span>](stopservice-method-in-class-cim-clusteringservice.md)   | <span data-ttu-id="bd3fa-130">Método de classe que coloca o serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-130">Class method that places the service in the stopped state.</span></span> <span data-ttu-id="bd3fa-131">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-131">Not implemented by WMI.</span></span><br/>              |



 

### <a name="properties"></a><span data-ttu-id="bd3fa-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bd3fa-132">Properties</span></span>

<span data-ttu-id="bd3fa-133">A classe **CIM \_ ClusteringService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-133">The **CIM\_ClusteringService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd3fa-134">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-134">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-137">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-137">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-138">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-138">A short textual description of the object.</span></span>

<span data-ttu-id="bd3fa-139">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-140">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-140">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-143">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-144">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-144">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bd3fa-145">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-145">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bd3fa-146">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-146">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-147">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-150">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-150">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-151">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-151">A textual description of the object.</span></span>

<span data-ttu-id="bd3fa-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-154">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-156">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-156">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-157">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-157">Indicates when the object was installed.</span></span> <span data-ttu-id="bd3fa-158">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-158">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bd3fa-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-163">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bd3fa-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-164">A propriedade Name identifica exclusivamente o serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-164">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="bd3fa-165">Essa funcionalidade é descrita mais detalhadamente na propriedade Description do objeto.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-165">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="bd3fa-166">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-166">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-167">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-167">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-168">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-170">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-170">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-171">Se **for true**, o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-171">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="bd3fa-172">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-172">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-173">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-173">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-176">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-176">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-177">Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-177">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="bd3fa-178">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-178">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="bd3fa-179">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-179">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="bd3fa-180">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-180">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd3fa-181">**Status**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-184">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-184">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-185">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-185">String that indicates the current status of the object.</span></span> <span data-ttu-id="bd3fa-186">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-186">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="bd3fa-187">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="bd3fa-187">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="bd3fa-188">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-188">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="bd3fa-189">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="bd3fa-189">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bd3fa-190">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-190">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bd3fa-191">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-191">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bd3fa-192">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-192">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bd3fa-193">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bd3fa-193">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bd3fa-194">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-194">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bd3fa-195">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-195">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bd3fa-196">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-196">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd3fa-197">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-197">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bd3fa-198">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-198">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bd3fa-199">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-199">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bd3fa-200">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-200">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bd3fa-201">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-201">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bd3fa-202">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-202">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bd3fa-203">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-203">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bd3fa-204">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-204">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bd3fa-205">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-205">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd3fa-206">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-206">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-207">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-209">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-209">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-210">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-210">Scoping system's creation class name.</span></span>

<span data-ttu-id="bd3fa-211">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-211">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd3fa-212">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-212">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd3fa-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bd3fa-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd3fa-215">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="bd3fa-215">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd3fa-216">Nome do sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-216">Name of the system that hosts the service.</span></span>

<span data-ttu-id="bd3fa-217">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-217">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd3fa-218">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd3fa-218">Remarks</span></span>

<span data-ttu-id="bd3fa-219">A classe **CIM \_ ClusteringService** é derivada do [**\_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd3fa-219">The **CIM\_ClusteringService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="bd3fa-220">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-220">WMI does not implement this class.</span></span>

<span data-ttu-id="bd3fa-221">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-221">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bd3fa-222">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bd3fa-222">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd3fa-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd3fa-223">Requirements</span></span>



| <span data-ttu-id="bd3fa-224">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd3fa-224">Requirement</span></span> | <span data-ttu-id="bd3fa-225">Valor</span><span class="sxs-lookup"><span data-stu-id="bd3fa-225">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd3fa-226">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd3fa-226">Minimum supported client</span></span><br/> | <span data-ttu-id="bd3fa-227">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd3fa-227">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd3fa-228">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd3fa-228">Minimum supported server</span></span><br/> | <span data-ttu-id="bd3fa-229">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd3fa-229">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd3fa-230">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd3fa-230">Namespace</span></span><br/>                | <span data-ttu-id="bd3fa-231">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bd3fa-231">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd3fa-232">MOF</span><span class="sxs-lookup"><span data-stu-id="bd3fa-232">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd3fa-233"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd3fa-233"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd3fa-234">DLL</span><span class="sxs-lookup"><span data-stu-id="bd3fa-234">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd3fa-235"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd3fa-235"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd3fa-236">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd3fa-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd3fa-237">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="bd3fa-237">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

