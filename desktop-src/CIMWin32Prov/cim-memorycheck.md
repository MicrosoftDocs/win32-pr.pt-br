---
description: A \_ classe CIM MemoryCheck especifica uma condição para a quantidade mínima de memória que deve estar disponível em um sistema.
ms.assetid: a7d22f31-a285-41c4-b069-47c54865ddf5
ms.tgt_platform: multiple
title: Classe CIM_MemoryCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCheck
- CIM_MemoryCheck.CheckID
- CIM_MemoryCheck.Caption
- CIM_MemoryCheck.Description
- CIM_MemoryCheck.CheckMode
- CIM_MemoryCheck.Name
- CIM_MemoryCheck.TargetOperatingSystem
- CIM_MemoryCheck.Version
- CIM_MemoryCheck.SoftwareElementID
- CIM_MemoryCheck.SoftwareElementState
- CIM_MemoryCheck.MemorySize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4265b108bd57bcb91aa903fd163ff14bd91311ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750958"
---
# <a name="cim_memorycheck-class"></a><span data-ttu-id="9f155-103">\_Classe CIM MemoryCheck</span><span class="sxs-lookup"><span data-stu-id="9f155-103">CIM\_MemoryCheck class</span></span>

<span data-ttu-id="9f155-104">A classe **CIM \_ MemoryCheck** especifica uma condição para a quantidade mínima de memória que deve estar disponível em um sistema.</span><span class="sxs-lookup"><span data-stu-id="9f155-104">The **CIM\_MemoryCheck** class specifies a condition for the minimum amount of memory that must be available on a system.</span></span> <span data-ttu-id="9f155-105">O valor é especificado na propriedade **MemorySize** .</span><span class="sxs-lookup"><span data-stu-id="9f155-105">The amount is specified in the **MemorySize** property.</span></span> <span data-ttu-id="9f155-106">Os detalhes das verificações são comparados com o valor da propriedade **FreePhysicalMemory** do objeto [**CIM \_ OperatingSystem**](cim-operatingsystem.md) referenciado por uma associação [**\_ InstalledOS**](cim-installedos.md) do CIM para o objeto de [**\_ ComputerSystem do CIM**](cim-computersystem.md) que descreve o ambiente.</span><span class="sxs-lookup"><span data-stu-id="9f155-106">Details of the checks are compared with the value of the **FreePhysicalMemory** property of the [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="9f155-107">Quando o valor da propriedade **FreePhysicalMemory** for maior ou igual ao valor especificado em **MemorySize**, a condição será satisfeita.</span><span class="sxs-lookup"><span data-stu-id="9f155-107">When the value of the **FreePhysicalMemory** property is greater than or equal to the value specified in **MemorySize**, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f155-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9f155-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f155-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f155-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9f155-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9f155-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9f155-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9f155-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f155-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f155-112">Syntax</span></span>

``` syntax
[UUID("{DC0E96FE-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_MemoryCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  uint64  MemorySize;
};
```

## <a name="members"></a><span data-ttu-id="9f155-113">Membros</span><span class="sxs-lookup"><span data-stu-id="9f155-113">Members</span></span>

<span data-ttu-id="9f155-114">A classe **CIM \_ MemoryCheck** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9f155-114">The **CIM\_MemoryCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="9f155-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f155-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f155-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f155-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f155-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="9f155-117">Methods</span></span>

<span data-ttu-id="9f155-118">A classe **CIM \_ MemoryCheck** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9f155-118">The **CIM\_MemoryCheck** class has these methods.</span></span>



| <span data-ttu-id="9f155-119">Método</span><span class="sxs-lookup"><span data-stu-id="9f155-119">Method</span></span>                                                   | <span data-ttu-id="9f155-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f155-120">Description</span></span>                                                   |
|:---------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="9f155-121">**Chame**</span><span class="sxs-lookup"><span data-stu-id="9f155-121">**Invoke**</span></span>](invoke-method-in-class-cim-memorycheck.md) | <span data-ttu-id="9f155-122">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="9f155-122">Takes a particular action.</span></span> <span data-ttu-id="9f155-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="9f155-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f155-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f155-124">Properties</span></span>

<span data-ttu-id="9f155-125">A classe **CIM \_ MemoryCheck** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f155-125">The **CIM\_MemoryCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f155-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9f155-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f155-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9f155-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9f155-130">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="9f155-130">A short textual description of the subject.</span></span>

<span data-ttu-id="9f155-131">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="9f155-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f155-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-135">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9f155-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9f155-136">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="9f155-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="9f155-137">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="9f155-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9f155-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f155-141">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="9f155-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="9f155-142">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="9f155-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="9f155-143">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="9f155-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="9f155-144">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="9f155-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="9f155-145">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9f155-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f155-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f155-149">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="9f155-149">A description of the objects.</span></span>

<span data-ttu-id="9f155-150">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-151">**Tamanho da memória**</span><span class="sxs-lookup"><span data-stu-id="9f155-151">**MemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-152">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9f155-152">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-154">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="9f155-154">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**FreePhysicalMemory**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9f155-155">Quantidade de memória que precisa existir em um sistema de computador para que um elemento de software seja executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="9f155-155">Amount of memory that needs to exist on a computer system for a software element to execute properly.</span></span>

<span data-ttu-id="9f155-156">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9f155-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-157">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9f155-157">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f155-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-160">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9f155-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9f155-161">Nome usado para identificar o elemento de software</span><span class="sxs-lookup"><span data-stu-id="9f155-161">Name used to identify the software element</span></span>

<span data-ttu-id="9f155-162">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-163">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="9f155-163">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f155-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-166">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="9f155-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="9f155-167">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9f155-167">This is an identifier for this software element.</span></span>

<span data-ttu-id="9f155-168">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f155-169">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="9f155-169">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-170">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f155-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-172">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f155-172">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f155-173">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9f155-173">The software element state of a software element.</span></span>

<span data-ttu-id="9f155-174">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-174">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="9f155-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="9f155-175"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-176">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9f155-176">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="9f155-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="9f155-177"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-178">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9f155-178">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="9f155-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="9f155-179"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-180">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="9f155-180">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="9f155-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="9f155-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-182">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="9f155-182">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f155-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="9f155-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f155-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-186">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="9f155-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="9f155-187">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="9f155-187">Target operating system of the software element.</span></span>

<span data-ttu-id="9f155-188">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f155-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="9f155-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f155-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="9f155-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="9f155-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="9f155-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="9f155-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="9f155-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="9f155-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="9f155-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="9f155-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="9f155-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="9f155-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="9f155-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="9f155-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="9f155-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="9f155-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="9f155-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-199">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="9f155-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="9f155-200"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="9f155-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="9f155-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="9f155-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="9f155-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="9f155-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="9f155-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="9f155-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="9f155-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="9f155-205"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="9f155-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="9f155-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="9f155-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-207">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="9f155-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="9f155-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="9f155-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="9f155-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="9f155-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="9f155-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="9f155-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="9f155-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="9f155-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="9f155-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="9f155-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9f155-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="9f155-215"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="9f155-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="9f155-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="9f155-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="9f155-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="9f155-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="9f155-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="9f155-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="9f155-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="9f155-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="9f155-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="9f155-222"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="9f155-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="9f155-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="9f155-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="9f155-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="9f155-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="9f155-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="9f155-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="9f155-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="9f155-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="9f155-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="9f155-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="9f155-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="9f155-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="9f155-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="9f155-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="9f155-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="9f155-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="9f155-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="9f155-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="9f155-232"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="9f155-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-233">Uma série</span><span class="sxs-lookup"><span data-stu-id="9f155-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="9f155-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="9f155-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-235">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="9f155-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="9f155-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="9f155-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-237">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="9f155-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="9f155-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="9f155-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="9f155-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="9f155-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="9f155-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="9f155-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="9f155-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="9f155-242"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="9f155-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="9f155-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="9f155-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="9f155-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="9f155-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="9f155-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="9f155-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-246">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="9f155-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="9f155-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="9f155-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="9f155-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="9f155-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="9f155-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="9f155-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="9f155-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="9f155-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="9f155-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="9f155-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="9f155-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="9f155-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="9f155-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="9f155-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="9f155-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="9f155-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="9f155-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="9f155-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="9f155-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="9f155-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="9f155-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="9f155-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="9f155-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="9f155-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="9f155-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="9f155-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="9f155-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="9f155-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="9f155-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="9f155-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="9f155-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="9f155-263">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="9f155-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="9f155-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="9f155-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="9f155-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="9f155-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="9f155-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="9f155-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="9f155-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="9f155-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="9f155-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="9f155-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f155-269">**Versão**</span><span class="sxs-lookup"><span data-stu-id="9f155-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f155-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9f155-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f155-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f155-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f155-272">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="9f155-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="9f155-273">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="9f155-273">Version of the operation.</span></span>

<span data-ttu-id="9f155-274">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="9f155-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="9f155-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="9f155-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="9f155-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="9f155-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="9f155-277">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f155-278">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f155-278">Remarks</span></span>

<span data-ttu-id="9f155-279">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9f155-279">WMI does not implement this class.</span></span>

<span data-ttu-id="9f155-280">A classe **CIM \_ MemoryCheck** é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="9f155-280">The **CIM\_MemoryCheck** class is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<span data-ttu-id="9f155-281">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f155-281">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f155-282">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9f155-282">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f155-283">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f155-283">Requirements</span></span>



| <span data-ttu-id="9f155-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f155-284">Requirement</span></span> | <span data-ttu-id="9f155-285">Valor</span><span class="sxs-lookup"><span data-stu-id="9f155-285">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f155-286">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f155-286">Minimum supported client</span></span><br/> | <span data-ttu-id="9f155-287">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f155-287">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f155-288">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f155-288">Minimum supported server</span></span><br/> | <span data-ttu-id="9f155-289">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f155-289">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f155-290">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f155-290">Namespace</span></span><br/>                | <span data-ttu-id="9f155-291">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9f155-291">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f155-292">MOF</span><span class="sxs-lookup"><span data-stu-id="9f155-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f155-293"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f155-293"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f155-294">DLL</span><span class="sxs-lookup"><span data-stu-id="9f155-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f155-295"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f155-295"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f155-296">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f155-296">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f155-297">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9f155-297">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

