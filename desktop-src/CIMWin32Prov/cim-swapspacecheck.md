---
description: A \_ classe CIM SwapSpaceCheck especifica a quantidade de espaço de permuta que deve estar disponível no sistema.
ms.assetid: c5e5ec68-bc62-4bdf-93b7-ce868e738dee
ms.tgt_platform: multiple
title: Classe CIM_SwapSpaceCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwapSpaceCheck
- CIM_SwapSpaceCheck.CheckID
- CIM_SwapSpaceCheck.Caption
- CIM_SwapSpaceCheck.Description
- CIM_SwapSpaceCheck.CheckMode
- CIM_SwapSpaceCheck.Name
- CIM_SwapSpaceCheck.TargetOperatingSystem
- CIM_SwapSpaceCheck.Version
- CIM_SwapSpaceCheck.SoftwareElementID
- CIM_SwapSpaceCheck.SoftwareElementState
- CIM_SwapSpaceCheck.SwapSpaceSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 992d8a314797c7a977e9a672ecb9d3dcdb561292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500990"
---
# <a name="cim_swapspacecheck-class"></a><span data-ttu-id="04ba1-103">\_Classe CIM SwapSpaceCheck</span><span class="sxs-lookup"><span data-stu-id="04ba1-103">CIM\_SwapSpaceCheck class</span></span>

<span data-ttu-id="04ba1-104">A classe **CIM \_ SwapSpaceCheck** especifica a quantidade de espaço de permuta que deve estar disponível no sistema.</span><span class="sxs-lookup"><span data-stu-id="04ba1-104">The **CIM\_SwapSpaceCheck** class specifies the amount of swap space that must be available on the system.</span></span> <span data-ttu-id="04ba1-105">O valor é especificado na propriedade **SwapSpaceSize** .</span><span class="sxs-lookup"><span data-stu-id="04ba1-105">The amount is specified in the **SwapSpaceSize** property.</span></span> <span data-ttu-id="04ba1-106">Os detalhes dessa verificação são comparados com os detalhes correspondentes encontrados em um objeto de sistema [**\_ operacional CIM**](cim-operatingsystem.md) referenciado pela Associação [**\_ InstalledOS**](cim-installedos.md) do CIM para o objeto de [**\_ ComputerSystem do CIM**](cim-computersystem.md) que descreve o ambiente.</span><span class="sxs-lookup"><span data-stu-id="04ba1-106">Details of this check are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by the [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="04ba1-107">Quando o valor da propriedade **TotalSwapSpaceSize** for maior ou igual ao valor especificado na propriedade **SwapSpaceSize** , a condição será satisfeita.</span><span class="sxs-lookup"><span data-stu-id="04ba1-107">When the value of the **TotalSwapSpaceSize** property is greater than or equal to the value specified in the **SwapSpaceSize** property, the condition is satisfied.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ba1-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="04ba1-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="04ba1-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="04ba1-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="04ba1-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="04ba1-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="04ba1-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="04ba1-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ba1-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04ba1-112">Syntax</span></span>

``` syntax
[UUID("{A5AE701E-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SwapSpaceCheck : CIM_Check
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
  uint64  SwapSpaceSize;
};
```

## <a name="members"></a><span data-ttu-id="04ba1-113">Membros</span><span class="sxs-lookup"><span data-stu-id="04ba1-113">Members</span></span>

<span data-ttu-id="04ba1-114">A classe **CIM \_ SwapSpaceCheck** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="04ba1-114">The **CIM\_SwapSpaceCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="04ba1-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="04ba1-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="04ba1-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="04ba1-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="04ba1-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="04ba1-117">Methods</span></span>

<span data-ttu-id="04ba1-118">A classe **CIM \_ SwapSpaceCheck** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="04ba1-118">The **CIM\_SwapSpaceCheck** class has these methods.</span></span>



| <span data-ttu-id="04ba1-119">Método</span><span class="sxs-lookup"><span data-stu-id="04ba1-119">Method</span></span>                                                      | <span data-ttu-id="04ba1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="04ba1-120">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="04ba1-121">**Chame**</span><span class="sxs-lookup"><span data-stu-id="04ba1-121">**Invoke**</span></span>](invoke-method-in-class-cim-swapspacecheck.md) | <span data-ttu-id="04ba1-122">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="04ba1-122">Takes a particular action.</span></span> <span data-ttu-id="04ba1-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="04ba1-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="04ba1-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="04ba1-124">Properties</span></span>

<span data-ttu-id="04ba1-125">A classe **CIM \_ SwapSpaceCheck** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="04ba1-125">The **CIM\_SwapSpaceCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04ba1-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="04ba1-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04ba1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="04ba1-129">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-130">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="04ba1-130">A short textual description of the subject.</span></span>

<span data-ttu-id="04ba1-131">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-131">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-132">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="04ba1-132">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04ba1-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-135">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="04ba1-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-136">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="04ba1-136">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="04ba1-137">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-137">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-138">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="04ba1-138">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-139">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="04ba1-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-141">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="04ba1-141">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="04ba1-142">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="04ba1-142">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="04ba1-143">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="04ba1-143">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="04ba1-144">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="04ba1-144">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="04ba1-145">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-145">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="04ba1-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04ba1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-149">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="04ba1-149">A description of the objects.</span></span>

<span data-ttu-id="04ba1-150">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-151">**Nome**</span><span class="sxs-lookup"><span data-stu-id="04ba1-151">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04ba1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-154">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="04ba1-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-155">Nome usado para identificar o elemento de software</span><span class="sxs-lookup"><span data-stu-id="04ba1-155">Name used to identify the software element</span></span>

<span data-ttu-id="04ba1-156">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-156">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-157">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="04ba1-157">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04ba1-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-160">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="04ba1-160">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-161">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="04ba1-161">This is an identifier for this software element.</span></span>

<span data-ttu-id="04ba1-162">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-162">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-163">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="04ba1-163">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04ba1-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-166">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="04ba1-166">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-167">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="04ba1-167">The software element state of a software element.</span></span>

<span data-ttu-id="04ba1-168">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-168">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="04ba1-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="04ba1-169"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-170">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="04ba1-170">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="04ba1-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="04ba1-171"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-172">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="04ba1-172">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="04ba1-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="04ba1-173"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-174">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="04ba1-174">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="04ba1-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="04ba1-175"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-176">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="04ba1-176">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="04ba1-177">**SwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="04ba1-177">**SwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-178">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="04ba1-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-180">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="04ba1-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**TotalSwapSpaceSize**"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-181">Tamanho mínimo de espaço de permuta, em kilobytes, que deve estar disponível no sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="04ba1-181">Minimum swap-space size, in kilobytes, that must be available on the target system.</span></span>

<span data-ttu-id="04ba1-182">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="04ba1-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="04ba1-183">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="04ba1-183">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04ba1-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-186">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="04ba1-186">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-187">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="04ba1-187">Target operating system of the software element.</span></span>

<span data-ttu-id="04ba1-188">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-188">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04ba1-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="04ba1-189"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04ba1-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="04ba1-190"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="04ba1-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="04ba1-191"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-192">Mac OS</span><span class="sxs-lookup"><span data-stu-id="04ba1-192">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="04ba1-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="04ba1-193"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-194">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="04ba1-194">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="04ba1-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="04ba1-195"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="04ba1-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="04ba1-196"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="04ba1-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="04ba1-197"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="04ba1-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="04ba1-198"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-199">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="04ba1-199">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="04ba1-200"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="04ba1-200"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-201">HP-UX</span><span class="sxs-lookup"><span data-stu-id="04ba1-201">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="04ba1-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="04ba1-202"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="04ba1-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="04ba1-203"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="04ba1-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="04ba1-204"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="04ba1-205"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="04ba1-205"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="04ba1-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="04ba1-206"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-207">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="04ba1-207">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="04ba1-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="04ba1-208"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="04ba1-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="04ba1-209"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-210">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="04ba1-210">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="04ba1-211"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="04ba1-211"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-212">Windows 95</span><span class="sxs-lookup"><span data-stu-id="04ba1-212">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="04ba1-213"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="04ba1-213"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-214">Windows 98</span><span class="sxs-lookup"><span data-stu-id="04ba1-214">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="04ba1-215"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="04ba1-215"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-216">Windows NT</span><span class="sxs-lookup"><span data-stu-id="04ba1-216">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="04ba1-217"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="04ba1-217"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-218">Windows CE</span><span class="sxs-lookup"><span data-stu-id="04ba1-218">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="04ba1-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="04ba1-219"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-220">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="04ba1-220">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="04ba1-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="04ba1-221"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="04ba1-222"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="04ba1-222"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="04ba1-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="04ba1-223"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="04ba1-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="04ba1-224"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="04ba1-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="04ba1-225"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="04ba1-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="04ba1-226"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="04ba1-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="04ba1-227"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="04ba1-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="04ba1-228"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="04ba1-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="04ba1-229"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="04ba1-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="04ba1-230"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="04ba1-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="04ba1-231"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="04ba1-232"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="04ba1-232"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-233">Uma série</span><span class="sxs-lookup"><span data-stu-id="04ba1-233">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="04ba1-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="04ba1-234"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-235">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="04ba1-235">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="04ba1-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="04ba1-236"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-237">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="04ba1-237">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="04ba1-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="04ba1-238"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-239">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="04ba1-239">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="04ba1-240"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="04ba1-240"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="04ba1-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="04ba1-241"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="04ba1-242"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="04ba1-242"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="04ba1-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="04ba1-243"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="04ba1-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="04ba1-244"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="04ba1-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="04ba1-245"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-246">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="04ba1-246">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="04ba1-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="04ba1-247"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="04ba1-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="04ba1-248"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="04ba1-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="04ba1-249"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="04ba1-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="04ba1-250"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-251">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="04ba1-251">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="04ba1-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="04ba1-252"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="04ba1-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="04ba1-253"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="04ba1-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="04ba1-254"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="04ba1-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="04ba1-255"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="04ba1-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="04ba1-256"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="04ba1-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="04ba1-257"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="04ba1-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="04ba1-258"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="04ba1-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="04ba1-259"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="04ba1-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="04ba1-260"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="04ba1-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="04ba1-261"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="04ba1-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="04ba1-262"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="04ba1-263">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="04ba1-263">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="04ba1-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="04ba1-264"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="04ba1-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="04ba1-265"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="04ba1-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="04ba1-266"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="04ba1-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="04ba1-267"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="04ba1-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="04ba1-268"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="04ba1-269">**Versão**</span><span class="sxs-lookup"><span data-stu-id="04ba1-269">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ba1-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="04ba1-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="04ba1-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ba1-272">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="04ba1-272">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="04ba1-273">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="04ba1-273">Version of the operation.</span></span>

<span data-ttu-id="04ba1-274">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="04ba1-274">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="04ba1-275"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="04ba1-275"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="04ba1-276"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="04ba1-276"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="04ba1-277">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="04ba1-277">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04ba1-278">Comentários</span><span class="sxs-lookup"><span data-stu-id="04ba1-278">Remarks</span></span>

<span data-ttu-id="04ba1-279">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="04ba1-279">WMI does not implement this class.</span></span>

<span data-ttu-id="04ba1-280">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="04ba1-280">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="04ba1-281">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="04ba1-281">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ba1-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ba1-282">Requirements</span></span>



| <span data-ttu-id="04ba1-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ba1-283">Requirement</span></span> | <span data-ttu-id="04ba1-284">Valor</span><span class="sxs-lookup"><span data-stu-id="04ba1-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04ba1-285">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04ba1-285">Minimum supported client</span></span><br/> | <span data-ttu-id="04ba1-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04ba1-286">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04ba1-287">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04ba1-287">Minimum supported server</span></span><br/> | <span data-ttu-id="04ba1-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04ba1-288">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04ba1-289">Namespace</span><span class="sxs-lookup"><span data-stu-id="04ba1-289">Namespace</span></span><br/>                | <span data-ttu-id="04ba1-290">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="04ba1-290">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04ba1-291">MOF</span><span class="sxs-lookup"><span data-stu-id="04ba1-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04ba1-292"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04ba1-292"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04ba1-293">DLL</span><span class="sxs-lookup"><span data-stu-id="04ba1-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ba1-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ba1-294"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ba1-295">Confira também</span><span class="sxs-lookup"><span data-stu-id="04ba1-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ba1-296">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="04ba1-296">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

