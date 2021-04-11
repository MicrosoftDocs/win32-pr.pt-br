---
description: A \_ classe CIM DiskSpaceCheck verifica a quantidade de espaço em disco disponível do sistema e especifica-o na propriedade AvailableDiskSpace.
ms.assetid: 51440084-7713-4106-b05b-cd2827f4cb05
ms.tgt_platform: multiple
title: Classe CIM_DiskSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck
- CIM_DiskSpaceCheck.CheckID
- CIM_DiskSpaceCheck.Caption
- CIM_DiskSpaceCheck.Description
- CIM_DiskSpaceCheck.CheckMode
- CIM_DiskSpaceCheck.Name
- CIM_DiskSpaceCheck.TargetOperatingSystem
- CIM_DiskSpaceCheck.Version
- CIM_DiskSpaceCheck.SoftwareElementID
- CIM_DiskSpaceCheck.SoftwareElementState
- CIM_DiskSpaceCheck.AvailableDiskSpace
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ad7452698b4969e78ee14cf4144e1f5c7883892b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089291"
---
# <a name="cim_diskspacecheck-class"></a><span data-ttu-id="68282-103">\_Classe CIM DiskSpaceCheck</span><span class="sxs-lookup"><span data-stu-id="68282-103">CIM\_DiskSpaceCheck class</span></span>

<span data-ttu-id="68282-104">A classe **CIM \_ DiskSpaceCheck** verifica a quantidade de espaço em disco disponível do sistema e especifica-o na propriedade **AvailableDiskSpace** .</span><span class="sxs-lookup"><span data-stu-id="68282-104">The **CIM\_DiskSpaceCheck** class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="68282-105">Os detalhes são comparados com o valor na propriedade **AvailableSpace** do objeto de [**sistema de \_ arquivos CIM**](cim-filesystem.md) que está associado ao objeto [**CIM \_ ComputerSystem**](cim-computersystem.md) , que descreve o ambiente do sistema.</span><span class="sxs-lookup"><span data-stu-id="68282-105">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="68282-106">Quando o valor da propriedade **AvailableSpace** for maior ou igual ao valor especificado na propriedade **AvailableDiskSpace** , a condição será satisfeita.</span><span class="sxs-lookup"><span data-stu-id="68282-106">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68282-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="68282-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68282-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="68282-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68282-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="68282-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="68282-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="68282-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68282-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68282-111">Syntax</span></span>

``` syntax
[UUID("{D3B1178A-DB29-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DiskSpaceCheck : CIM_Check
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
  uint64  AvailableDiskSpace;
};
```

## <a name="members"></a><span data-ttu-id="68282-112">Membros</span><span class="sxs-lookup"><span data-stu-id="68282-112">Members</span></span>

<span data-ttu-id="68282-113">A classe **CIM \_ DiskSpaceCheck** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68282-113">The **CIM\_DiskSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="68282-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="68282-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="68282-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68282-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68282-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="68282-116">Methods</span></span>

<span data-ttu-id="68282-117">A classe **CIM \_ DiskSpaceCheck** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="68282-117">The **CIM\_DiskSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="68282-118">Método</span><span class="sxs-lookup"><span data-stu-id="68282-118">Method</span></span>                                                      | <span data-ttu-id="68282-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="68282-119">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="68282-120">**Chame**</span><span class="sxs-lookup"><span data-stu-id="68282-120">**Invoke**</span></span>](invoke-method-in-class-cim-diskspacecheck.md) | <span data-ttu-id="68282-121">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="68282-121">Takes a particular action.</span></span> <span data-ttu-id="68282-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="68282-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68282-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68282-123">Properties</span></span>

<span data-ttu-id="68282-124">A classe **CIM \_ DiskSpaceCheck** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="68282-124">The **CIM\_DiskSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68282-125">**AvailableDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="68282-125">**AvailableDiskSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="68282-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="68282-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-128">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema de arquivos CIM**](cim-filesystem.md).**AvailableSpace** "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="68282-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_FileSystem**](cim-filesystem.md).**AvailableSpace** "), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="68282-129">Espaço em disco disponível.</span><span class="sxs-lookup"><span data-stu-id="68282-129">Available disk space.</span></span>

<span data-ttu-id="68282-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="68282-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="68282-131">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="68282-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68282-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68282-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-134">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="68282-134">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="68282-135">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="68282-135">A short textual description of the subject.</span></span>

<span data-ttu-id="68282-136">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="68282-137">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="68282-137">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68282-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68282-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-140">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="68282-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68282-141">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="68282-141">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="68282-142">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="68282-143">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="68282-143">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-144">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="68282-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68282-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68282-146">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="68282-146">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="68282-147">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="68282-147">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="68282-148">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="68282-148">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="68282-149">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="68282-149">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="68282-150">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="68282-151">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68282-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68282-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68282-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68282-154">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="68282-154">A description of the objects.</span></span>

<span data-ttu-id="68282-155">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-155">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="68282-156">**Nome**</span><span class="sxs-lookup"><span data-stu-id="68282-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68282-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68282-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-159">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="68282-159">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68282-160">Nome usado para identificar o elemento de software</span><span class="sxs-lookup"><span data-stu-id="68282-160">Name used to identify the software element</span></span>

<span data-ttu-id="68282-161">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-161">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="68282-162">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="68282-162">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68282-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68282-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-165">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="68282-165">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="68282-166">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="68282-166">This is an identifier for this software element.</span></span>

<span data-ttu-id="68282-167">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-167">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="68282-168">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="68282-168">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-169">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68282-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68282-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-171">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68282-171">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68282-172">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="68282-172">The software element state of a software element.</span></span>

<span data-ttu-id="68282-173">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-173">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="68282-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="68282-174"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="68282-175">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="68282-175">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="68282-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="68282-176"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="68282-177">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="68282-177">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="68282-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="68282-178"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68282-179">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="68282-179">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="68282-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="68282-180"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="68282-181">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="68282-181">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68282-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="68282-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-183">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68282-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68282-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-185">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="68282-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="68282-186">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="68282-186">Target operating system of the software element.</span></span>

<span data-ttu-id="68282-187">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-187">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68282-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="68282-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68282-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="68282-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="68282-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="68282-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68282-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="68282-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="68282-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="68282-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="68282-193">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="68282-193">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="68282-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="68282-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="68282-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="68282-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="68282-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="68282-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="68282-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="68282-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="68282-198">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="68282-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="68282-199"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="68282-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="68282-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="68282-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="68282-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="68282-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="68282-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="68282-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="68282-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="68282-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="68282-204"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="68282-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="68282-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="68282-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="68282-206">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="68282-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="68282-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="68282-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="68282-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="68282-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="68282-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="68282-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="68282-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="68282-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="68282-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="68282-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="68282-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="68282-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="68282-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="68282-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="68282-214"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="68282-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="68282-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="68282-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="68282-216"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="68282-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="68282-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="68282-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="68282-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="68282-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="68282-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="68282-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="68282-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="68282-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="68282-221"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="68282-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="68282-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="68282-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="68282-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="68282-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="68282-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="68282-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="68282-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="68282-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="68282-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="68282-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="68282-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="68282-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="68282-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="68282-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="68282-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="68282-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="68282-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="68282-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="68282-231"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="68282-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="68282-232">Uma série</span><span class="sxs-lookup"><span data-stu-id="68282-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="68282-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="68282-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="68282-234">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="68282-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="68282-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="68282-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="68282-236">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="68282-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="68282-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="68282-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="68282-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="68282-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="68282-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="68282-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="68282-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="68282-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="68282-241"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="68282-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="68282-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="68282-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="68282-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="68282-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="68282-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="68282-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="68282-245">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="68282-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="68282-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="68282-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="68282-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="68282-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="68282-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="68282-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="68282-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="68282-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="68282-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="68282-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="68282-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="68282-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="68282-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="68282-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="68282-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="68282-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="68282-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="68282-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="68282-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="68282-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="68282-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="68282-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="68282-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="68282-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="68282-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="68282-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="68282-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="68282-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="68282-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="68282-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="68282-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="68282-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="68282-262">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="68282-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="68282-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="68282-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="68282-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="68282-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="68282-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="68282-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="68282-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="68282-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="68282-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="68282-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68282-268">**Versão**</span><span class="sxs-lookup"><span data-stu-id="68282-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68282-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68282-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68282-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68282-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68282-271">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="68282-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="68282-272">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="68282-272">Version of the operation.</span></span>

<span data-ttu-id="68282-273">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="68282-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="68282-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="68282-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="68282-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="68282-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="68282-276">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="68282-276">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68282-277">Comentários</span><span class="sxs-lookup"><span data-stu-id="68282-277">Remarks</span></span>

<span data-ttu-id="68282-278">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="68282-278">WMI does not implement this class.</span></span>

<span data-ttu-id="68282-279">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="68282-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68282-280">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="68282-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68282-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68282-281">Requirements</span></span>



| <span data-ttu-id="68282-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="68282-282">Requirement</span></span> | <span data-ttu-id="68282-283">Valor</span><span class="sxs-lookup"><span data-stu-id="68282-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68282-284">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68282-284">Minimum supported client</span></span><br/> | <span data-ttu-id="68282-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68282-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68282-286">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68282-286">Minimum supported server</span></span><br/> | <span data-ttu-id="68282-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68282-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68282-288">Namespace</span><span class="sxs-lookup"><span data-stu-id="68282-288">Namespace</span></span><br/>                | <span data-ttu-id="68282-289">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68282-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68282-290">MOF</span><span class="sxs-lookup"><span data-stu-id="68282-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68282-291"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68282-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68282-292">DLL</span><span class="sxs-lookup"><span data-stu-id="68282-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68282-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68282-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68282-294">Confira também</span><span class="sxs-lookup"><span data-stu-id="68282-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68282-295">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="68282-295">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

