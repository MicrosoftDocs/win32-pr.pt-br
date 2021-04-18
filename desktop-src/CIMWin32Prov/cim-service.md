---
description: A \_ classe de serviço CIM representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software.
ms.assetid: b95e8ea7-4daf-4dcf-817c-b872560b62df
ms.tgt_platform: multiple
title: Classe CIM_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.Caption
- CIM_Service.Description
- CIM_Service.InstallDate
- CIM_Service.Status
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.Started
- CIM_Service.StartMode
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1656d9aa5e5ee8c58c5895a444afd7552227108c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755205"
---
# <a name="cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="ea47b-103">Classe CIM_Service (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ea47b-103">CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ea47b-104">A classe de **\_ serviço CIM** representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software.</span><span class="sxs-lookup"><span data-stu-id="ea47b-104">The **CIM\_Service** class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="ea47b-105">Um serviço é um objeto de finalidade geral para configurar e gerenciar a implementação da funcionalidade; Ela não é a funcionalidade propriamente dita.</span><span class="sxs-lookup"><span data-stu-id="ea47b-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ea47b-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="ea47b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ea47b-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ea47b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ea47b-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="ea47b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ea47b-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="ea47b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea47b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea47b-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C527-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services (CIM)"), AMENDMENT]
class CIM_Service : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="ea47b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="ea47b-111">Members</span></span>

<span data-ttu-id="ea47b-112">A classe de **\_ serviço CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ea47b-112">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="ea47b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea47b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea47b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea47b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea47b-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="ea47b-115">Methods</span></span>

<span data-ttu-id="ea47b-116">A classe de **\_ serviço CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ea47b-116">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="ea47b-117">Método</span><span class="sxs-lookup"><span data-stu-id="ea47b-117">Method</span></span>                                                           | <span data-ttu-id="ea47b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea47b-118">Description</span></span>                                                                                 |
|:-----------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea47b-119">**StartService**</span><span class="sxs-lookup"><span data-stu-id="ea47b-119">**StartService**</span></span>](startservice-method-in-class-cim-service.md) | <span data-ttu-id="ea47b-120">Tenta colocar o serviço em seu estado de inicialização.</span><span class="sxs-lookup"><span data-stu-id="ea47b-120">Attempts to put the service into its start-up state.</span></span> <span data-ttu-id="ea47b-121">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ea47b-121">Not implemented by WMI.</span></span><br/>     |
| [<span data-ttu-id="ea47b-122">**StopService**</span><span class="sxs-lookup"><span data-stu-id="ea47b-122">**StopService**</span></span>](stopservice-method-in-class-cim-service.md)   | <span data-ttu-id="ea47b-123">Método de classe que coloca o serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="ea47b-123">Class method that puts the service in the stopped state.</span></span> <span data-ttu-id="ea47b-124">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="ea47b-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ea47b-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ea47b-125">Properties</span></span>

<span data-ttu-id="ea47b-126">A classe de **\_ serviço CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ea47b-126">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ea47b-127">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="ea47b-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-130">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="ea47b-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-131">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ea47b-131">A short textual description of the object.</span></span>

<span data-ttu-id="ea47b-132">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ea47b-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea47b-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-136">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="ea47b-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-137">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="ea47b-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="ea47b-138">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="ea47b-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ea47b-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-142">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="ea47b-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-143">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ea47b-143">A textual description of the object.</span></span>

<span data-ttu-id="ea47b-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ea47b-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ea47b-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ea47b-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="ea47b-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-149">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="ea47b-149">Indicates when the object was installed.</span></span> <span data-ttu-id="ea47b-150">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="ea47b-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ea47b-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ea47b-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ea47b-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-155">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ea47b-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-156">A propriedade Name identifica exclusivamente o serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="ea47b-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="ea47b-157">Essa funcionalidade é descrita mais detalhadamente na propriedade Description do objeto.</span><span class="sxs-lookup"><span data-stu-id="ea47b-157">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-158">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="ea47b-158">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-159">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ea47b-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-161">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="ea47b-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-162">Se **for true**, o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ea47b-162">If **TRUE**, the service has started.</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-163">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="ea47b-163">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-166">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="ea47b-166">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-167">Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="ea47b-167">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="ea47b-168">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="ea47b-168">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="ea47b-169">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="ea47b-169">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ea47b-170">**Status**</span><span class="sxs-lookup"><span data-stu-id="ea47b-170">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-171">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-173">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="ea47b-173">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-174">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="ea47b-174">String that indicates the current status of the object.</span></span> <span data-ttu-id="ea47b-175">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="ea47b-175">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ea47b-176">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="ea47b-176">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ea47b-177">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="ea47b-177">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ea47b-178">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="ea47b-178">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ea47b-179">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="ea47b-179">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ea47b-180">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="ea47b-180">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ea47b-181">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ea47b-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ea47b-182">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ea47b-182">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ea47b-183">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="ea47b-183">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ea47b-184">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="ea47b-184">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ea47b-185">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="ea47b-185">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ea47b-186">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="ea47b-186">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ea47b-187">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="ea47b-187">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ea47b-188">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="ea47b-188">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ea47b-189">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="ea47b-189">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ea47b-190">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="ea47b-190">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ea47b-191">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="ea47b-191">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ea47b-192">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="ea47b-192">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ea47b-193">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="ea47b-193">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ea47b-194">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="ea47b-194">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ea47b-195">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ea47b-195">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-198">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="ea47b-198">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-199">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="ea47b-199">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="ea47b-200">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ea47b-200">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ea47b-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ea47b-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ea47b-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ea47b-203">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="ea47b-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="ea47b-204">Nome do sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="ea47b-204">Name of the system that hosts the service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea47b-205">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea47b-205">Remarks</span></span>

<span data-ttu-id="ea47b-206">A classe de **\_ serviço CIM** é derivada de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="ea47b-206">The **CIM\_Service** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="ea47b-207">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="ea47b-207">WMI does not implement this class.</span></span> <span data-ttu-id="ea47b-208">Para classes WMI derivadas do **\_ serviço CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ea47b-208">For WMI classes that are derived from **CIM\_Service**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ea47b-209">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="ea47b-209">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ea47b-210">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="ea47b-210">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea47b-211">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea47b-211">Requirements</span></span>



| <span data-ttu-id="ea47b-212">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea47b-212">Requirement</span></span> | <span data-ttu-id="ea47b-213">Valor</span><span class="sxs-lookup"><span data-stu-id="ea47b-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea47b-214">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea47b-214">Minimum supported client</span></span><br/> | <span data-ttu-id="ea47b-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea47b-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea47b-216">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea47b-216">Minimum supported server</span></span><br/> | <span data-ttu-id="ea47b-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea47b-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea47b-218">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea47b-218">Namespace</span></span><br/>                | <span data-ttu-id="ea47b-219">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ea47b-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ea47b-220">MOF</span><span class="sxs-lookup"><span data-stu-id="ea47b-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea47b-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ea47b-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea47b-222">DLL</span><span class="sxs-lookup"><span data-stu-id="ea47b-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea47b-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea47b-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea47b-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea47b-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea47b-225">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="ea47b-225">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

