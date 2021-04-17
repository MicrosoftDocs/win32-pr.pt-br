---
description: A \_ classe CIM DS representa a funcionalidade fornecida por um dispositivo ou software, ou por uma rede, para carregar um sistema operacional em um sistema de computador unitário.
ms.assetid: d9c969bb-0f54-4e94-8e19-7ccd6f5adfb3
ms.tgt_platform: multiple
title: Classe CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService
- CIM_BootService.Caption
- CIM_BootService.Description
- CIM_BootService.InstallDate
- CIM_BootService.Status
- CIM_BootService.CreationClassName
- CIM_BootService.Name
- CIM_BootService.Started
- CIM_BootService.StartMode
- CIM_BootService.SystemCreationClassName
- CIM_BootService.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d32a8fdfe61e02e6ffe3a8dd2f115e57f338aec6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755675"
---
# <a name="cim_bootservice-class"></a><span data-ttu-id="0849f-103">\_Classe CIM DS</span><span class="sxs-lookup"><span data-stu-id="0849f-103">CIM\_BootService class</span></span>

<span data-ttu-id="0849f-104">A classe **CIM \_ DS** representa a funcionalidade fornecida por um dispositivo ou software, ou por uma rede, para carregar um sistema operacional em um sistema de computador unitário.</span><span class="sxs-lookup"><span data-stu-id="0849f-104">The **CIM\_BootService** class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0849f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="0849f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0849f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0849f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0849f-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0849f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0849f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="0849f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0849f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0849f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4FE-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_BootService : CIM_Service
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

## <a name="members"></a><span data-ttu-id="0849f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0849f-110">Members</span></span>

<span data-ttu-id="0849f-111">A classe **CIM \_ DS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0849f-111">The **CIM\_BootService** class has these types of members:</span></span>

-   [<span data-ttu-id="0849f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0849f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0849f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0849f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0849f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="0849f-114">Methods</span></span>

<span data-ttu-id="0849f-115">A classe **CIM \_ DS** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0849f-115">The **CIM\_BootService** class has these methods.</span></span>



| <span data-ttu-id="0849f-116">Método</span><span class="sxs-lookup"><span data-stu-id="0849f-116">Method</span></span>                                                               | <span data-ttu-id="0849f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0849f-117">Description</span></span>                                                               |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="0849f-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="0849f-118">**StartService**</span></span>](startservice-method-in-class-cim-bootservice.md) | <span data-ttu-id="0849f-119">Coloca o serviço no estado iniciado.</span><span class="sxs-lookup"><span data-stu-id="0849f-119">Puts the service in the started state.</span></span> <span data-ttu-id="0849f-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0849f-120">Not implemented by WMI.</span></span><br/> |
| [<span data-ttu-id="0849f-121">**StopService**</span><span class="sxs-lookup"><span data-stu-id="0849f-121">**StopService**</span></span>](stopservice-method-in-class-cim-bootservice.md)   | <span data-ttu-id="0849f-122">Coloca o serviço no estado parado.</span><span class="sxs-lookup"><span data-stu-id="0849f-122">Puts the service in the stopped state.</span></span> <span data-ttu-id="0849f-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="0849f-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0849f-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0849f-124">Properties</span></span>

<span data-ttu-id="0849f-125">A classe **CIM \_ DS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0849f-125">The **CIM\_BootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0849f-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="0849f-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0849f-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-130">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0849f-130">A short textual description of the object.</span></span>

<span data-ttu-id="0849f-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0849f-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-135">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nome da classe")</span><span class="sxs-lookup"><span data-stu-id="0849f-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-136">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="0849f-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0849f-137">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0849f-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0849f-138">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-138">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0849f-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-142">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="0849f-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-143">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0849f-143">A textual description of the object.</span></span>

<span data-ttu-id="0849f-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0849f-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-146">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0849f-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="0849f-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-149">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="0849f-149">Indicates when the object was installed.</span></span> <span data-ttu-id="0849f-150">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="0849f-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0849f-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0849f-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0849f-155">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0849f-156">A propriedade Name identifica exclusivamente o serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="0849f-156">The Name property uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="0849f-157">Essa funcionalidade é descrita mais detalhadamente na propriedade **Description** do objeto.</span><span class="sxs-lookup"><span data-stu-id="0849f-157">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="0849f-158">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-158">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-159">**Iniciado**</span><span class="sxs-lookup"><span data-stu-id="0849f-159">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-160">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0849f-160">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-162">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")</span><span class="sxs-lookup"><span data-stu-id="0849f-162">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-163">Se **for true**, o serviço foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="0849f-163">If **TRUE**, the service has started.</span></span>

<span data-ttu-id="0849f-164">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-165">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0849f-165">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-168">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de início")</span><span class="sxs-lookup"><span data-stu-id="0849f-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-169">Indica se o serviço é iniciado automaticamente (por exemplo, por um sistema operacional) ou iniciado somente mediante solicitação.</span><span class="sxs-lookup"><span data-stu-id="0849f-169">Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

<span data-ttu-id="0849f-170">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-170">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="0849f-171">**Automático** ("automático")</span><span class="sxs-lookup"><span data-stu-id="0849f-171">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="0849f-172">**Manual** ("manual")</span><span class="sxs-lookup"><span data-stu-id="0849f-172">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0849f-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="0849f-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-176">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="0849f-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-177">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="0849f-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="0849f-178">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="0849f-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="0849f-179">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="0849f-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="0849f-180">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="0849f-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="0849f-181">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="0849f-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0849f-182">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="0849f-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0849f-183">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="0849f-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0849f-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0849f-185">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0849f-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0849f-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="0849f-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0849f-187">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="0849f-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0849f-188">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="0849f-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0849f-189">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="0849f-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0849f-190">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="0849f-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0849f-191">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0849f-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0849f-192">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="0849f-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0849f-193">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="0849f-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0849f-194">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="0849f-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0849f-195">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="0849f-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0849f-196">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="0849f-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0849f-197">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="0849f-197">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0849f-198">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0849f-198">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-201">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema ")</span><span class="sxs-lookup"><span data-stu-id="0849f-201">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-202">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="0849f-202">Scoping system's creation class name.</span></span>

<span data-ttu-id="0849f-203">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-203">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="0849f-204">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0849f-204">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0849f-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0849f-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0849f-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0849f-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0849f-207">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema ")</span><span class="sxs-lookup"><span data-stu-id="0849f-207">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="0849f-208">Nome do sistema que hospeda o serviço.</span><span class="sxs-lookup"><span data-stu-id="0849f-208">Name of the system that hosts the service.</span></span>

<span data-ttu-id="0849f-209">Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-209">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0849f-210">Comentários</span><span class="sxs-lookup"><span data-stu-id="0849f-210">Remarks</span></span>

<span data-ttu-id="0849f-211">A classe **CIM \_ DS** é derivada do [**\_ serviço CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="0849f-211">The **CIM\_BootService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="0849f-212">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="0849f-212">WMI does not implement this class.</span></span>

<span data-ttu-id="0849f-213">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="0849f-213">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0849f-214">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="0849f-214">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0849f-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0849f-215">Requirements</span></span>



| <span data-ttu-id="0849f-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="0849f-216">Requirement</span></span> | <span data-ttu-id="0849f-217">Valor</span><span class="sxs-lookup"><span data-stu-id="0849f-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0849f-218">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0849f-218">Minimum supported client</span></span><br/> | <span data-ttu-id="0849f-219">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0849f-219">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0849f-220">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0849f-220">Minimum supported server</span></span><br/> | <span data-ttu-id="0849f-221">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0849f-221">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0849f-222">Namespace</span><span class="sxs-lookup"><span data-stu-id="0849f-222">Namespace</span></span><br/>                | <span data-ttu-id="0849f-223">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0849f-223">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0849f-224">MOF</span><span class="sxs-lookup"><span data-stu-id="0849f-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0849f-225"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0849f-225"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0849f-226">DLL</span><span class="sxs-lookup"><span data-stu-id="0849f-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0849f-227"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0849f-227"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0849f-228">Confira também</span><span class="sxs-lookup"><span data-stu-id="0849f-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0849f-229">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="0849f-229">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

