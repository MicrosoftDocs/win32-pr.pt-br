---
description: A \_ classe CIM OSVersionCheck especifica as versões do sistema operacional que podem dar suporte a um elemento de software.
ms.assetid: 6796cfc4-3b6f-43a4-b5f0-854a95284238
ms.tgt_platform: multiple
title: Classe CIM_OSVersionCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck
- CIM_OSVersionCheck.CheckID
- CIM_OSVersionCheck.Caption
- CIM_OSVersionCheck.Description
- CIM_OSVersionCheck.CheckMode
- CIM_OSVersionCheck.Name
- CIM_OSVersionCheck.TargetOperatingSystem
- CIM_OSVersionCheck.Version
- CIM_OSVersionCheck.SoftwareElementID
- CIM_OSVersionCheck.SoftwareElementState
- CIM_OSVersionCheck.MaximumVersion
- CIM_OSVersionCheck.MinimumVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c341b9038b5b40b559b4a121adb88fbb2d7b5205
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010210"
---
# <a name="cim_osversioncheck-class"></a><span data-ttu-id="c8019-103">\_Classe CIM OSVersionCheck</span><span class="sxs-lookup"><span data-stu-id="c8019-103">CIM\_OSVersionCheck class</span></span>

<span data-ttu-id="c8019-104">A classe **CIM \_ OSVersionCheck** especifica as versões do sistema operacional que podem dar suporte a um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="c8019-104">The **CIM\_OSVersionCheck** class specifies the versions of the operating system that can support a software element.</span></span> <span data-ttu-id="c8019-105">A verificação pode ser executada para um determinado, mínimo, máximo ou um intervalo de versões do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c8019-105">The check can be run for a specific, minimum, maximum, or a range of operating system releases.</span></span> <span data-ttu-id="c8019-106">Para especificar uma versão específica do sistema operacional, as versões mínima e máxima devem ser iguais.</span><span class="sxs-lookup"><span data-stu-id="c8019-106">To specify a specific operating system version, the minimum and maximum versions must be equal.</span></span> <span data-ttu-id="c8019-107">Para especificar a versão mínima, a versão mínima deve ser especificada apenas.</span><span class="sxs-lookup"><span data-stu-id="c8019-107">To specify the minimum version, the minimum version only must be specified.</span></span> <span data-ttu-id="c8019-108">Para especificar uma versão máxima, a versão máxima precisa ser especificada apenas.</span><span class="sxs-lookup"><span data-stu-id="c8019-108">To specify a maximum version, the maximum version only needs to be specified.</span></span> <span data-ttu-id="c8019-109">Para especificar um intervalo, as versões mínima e máxima devem ser especificadas.</span><span class="sxs-lookup"><span data-stu-id="c8019-109">To specify a range, both minimum and maximum versions must be specified.</span></span>

<span data-ttu-id="c8019-110">O tipo de sistema operacional é especificado na propriedade **TargetOperatingSystem** do elemento de software proprietário.</span><span class="sxs-lookup"><span data-stu-id="c8019-110">The type of operating system is specified in the **TargetOperatingSystem** property of the owning software element.</span></span> <span data-ttu-id="c8019-111">Os detalhes das verificações são comparados aos detalhes correspondentes encontrados em um objeto de sistema [**\_ operacional CIM**](cim-operatingsystem.md) referenciado por uma associação de [**\_ InstalledOS CIM**](cim-installedos.md) para o objeto de [**\_ ComputerSystem do CIM**](cim-computersystem.md) que descreve o ambiente.</span><span class="sxs-lookup"><span data-stu-id="c8019-111">Details of the checks are compared with the corresponding details found in a [**CIM\_OperatingSystem**](cim-operatingsystem.md) object referenced by a [**CIM\_InstalledOS**](cim-installedos.md) association for the [**CIM\_ComputerSystem**](cim-computersystem.md) object that describes the environment.</span></span> <span data-ttu-id="c8019-112">Pelo menos uma classe **CIM \_ OperatingSystem** deve satisfazer os detalhes da condição para que a verificação seja satisfeita.</span><span class="sxs-lookup"><span data-stu-id="c8019-112">At least one **CIM\_OperatingSystem** class must satisfy the details of the condition for the check to be satisfied.</span></span> <span data-ttu-id="c8019-113">Em outras palavras, nem todos os sistemas operacionais no sistema de computador relevante precisam atender à condição.</span><span class="sxs-lookup"><span data-stu-id="c8019-113">In other words, not all of the operating systems on the relevant computer system need to satisfy the condition.</span></span> <span data-ttu-id="c8019-114">Além disso, a propriedade **OSType** da classe **CIM \_ OperatingSystem** deve corresponder ao tipo da propriedade **TargetOperatingSystem** .</span><span class="sxs-lookup"><span data-stu-id="c8019-114">Also, the **OSType** property of the **CIM\_OperatingSystem** class must match the type of the **TargetOperatingSystem** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8019-115">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c8019-115">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c8019-116">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c8019-116">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c8019-117">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c8019-117">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c8019-118">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c8019-118">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8019-119">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8019-119">Syntax</span></span>

``` syntax
[UUID("{FEE8368A-DB2A-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_OSVersionCheck : CIM_Check
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
  string  MaximumVersion;
  string  MinimumVersion;
};
```

## <a name="members"></a><span data-ttu-id="c8019-120">Membros</span><span class="sxs-lookup"><span data-stu-id="c8019-120">Members</span></span>

<span data-ttu-id="c8019-121">A classe **CIM \_ OSVersionCheck** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c8019-121">The **CIM\_OSVersionCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="c8019-122">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8019-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="c8019-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c8019-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c8019-124">Métodos</span><span class="sxs-lookup"><span data-stu-id="c8019-124">Methods</span></span>

<span data-ttu-id="c8019-125">A classe **CIM \_ OSVersionCheck** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c8019-125">The **CIM\_OSVersionCheck** class has these methods.</span></span>



| <span data-ttu-id="c8019-126">Método</span><span class="sxs-lookup"><span data-stu-id="c8019-126">Method</span></span>                                                      | <span data-ttu-id="c8019-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8019-127">Description</span></span>                                                   |
|:------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="c8019-128">**Chame**</span><span class="sxs-lookup"><span data-stu-id="c8019-128">**Invoke**</span></span>](invoke-method-in-class-cim-osversioncheck.md) | <span data-ttu-id="c8019-129">Executa uma ação específica.</span><span class="sxs-lookup"><span data-stu-id="c8019-129">Takes a particular action.</span></span> <span data-ttu-id="c8019-130">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="c8019-130">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c8019-131">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c8019-131">Properties</span></span>

<span data-ttu-id="c8019-132">A classe **CIM \_ OSVersionCheck** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c8019-132">The **CIM\_OSVersionCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8019-133">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="c8019-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-136">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c8019-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c8019-137">Uma breve descrição textual do assunto.</span><span class="sxs-lookup"><span data-stu-id="c8019-137">A short textual description of the subject.</span></span>

<span data-ttu-id="c8019-138">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-138">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8019-139">**CheckID**</span><span class="sxs-lookup"><span data-stu-id="c8019-139">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-142">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c8019-142">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c8019-143">Identificador usado em conjunto com outras chaves para identificar exclusivamente a verificação.</span><span class="sxs-lookup"><span data-stu-id="c8019-143">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="c8019-144">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-144">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8019-145">**CheckMode**</span><span class="sxs-lookup"><span data-stu-id="c8019-145">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-146">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="c8019-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8019-148">Se for **true**, espera-se que a condição exista no ambiente.</span><span class="sxs-lookup"><span data-stu-id="c8019-148">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="c8019-149">Por exemplo, espera-se que um arquivo esteja em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="c8019-149">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="c8019-150">Se for **false**, a condição não deverá existir.</span><span class="sxs-lookup"><span data-stu-id="c8019-150">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="c8019-151">Por exemplo, um arquivo não está em um sistema, portanto, o método [**Invoke**](invoke-method-in-class-cim-check.md) deve retornar **false**.</span><span class="sxs-lookup"><span data-stu-id="c8019-151">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="c8019-152">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-152">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8019-153">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c8019-153">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8019-156">Uma descrição dos objetos.</span><span class="sxs-lookup"><span data-stu-id="c8019-156">A description of the objects.</span></span>

<span data-ttu-id="c8019-157">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-157">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8019-158">**MaximumVersion**</span><span class="sxs-lookup"><span data-stu-id="c8019-158">**MaximumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-161">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="c8019-161">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="c8019-162">Versão máxima do sistema operacional necessário.</span><span class="sxs-lookup"><span data-stu-id="c8019-162">Maximum version of the required operating system.</span></span>

<span data-ttu-id="c8019-163">O valor é codificado em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="c8019-163">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="c8019-164"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="c8019-164"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="c8019-165"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="c8019-165"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="c8019-166">**MinimumVersion**</span><span class="sxs-lookup"><span data-stu-id="c8019-166">**MinimumVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-169">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**Version**")</span><span class="sxs-lookup"><span data-stu-id="c8019-169">Qualifiers: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**Version**")</span></span>
</dt> </dl>

<span data-ttu-id="c8019-170">Versão mínima do sistema operacional necessário.</span><span class="sxs-lookup"><span data-stu-id="c8019-170">Minimum version of the required operating system.</span></span>

<span data-ttu-id="c8019-171">O valor é codificado em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="c8019-171">The value is encoded in one of the following forms:</span></span>

-   <span data-ttu-id="c8019-172"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="c8019-172"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="c8019-173"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="c8019-173"><major>.<minor><letter><revision></span></span>

</dd> <dt>

<span data-ttu-id="c8019-174">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c8019-174">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-177">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c8019-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c8019-178">Nome usado para identificar o elemento de software</span><span class="sxs-lookup"><span data-stu-id="c8019-178">Name used to identify the software element</span></span>

<span data-ttu-id="c8019-179">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-179">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8019-180">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="c8019-180">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-183">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c8019-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c8019-184">Este é um identificador para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="c8019-184">This is an identifier for this software element.</span></span>

<span data-ttu-id="c8019-185">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-185">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="c8019-186">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="c8019-186">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8019-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-189">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c8019-189">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c8019-190">O estado do elemento de software de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="c8019-190">The software element state of a software element.</span></span>

<span data-ttu-id="c8019-191">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-191">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="c8019-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="c8019-192"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-193">Descreve os detalhes necessários para a distribuição bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado instalável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="c8019-193">Describes the details necessary for successful distribution and the details (conditions and actions) required to create a software element in the installable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="c8019-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="c8019-194"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-195">Descreve os detalhes necessários para a instalação bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado executável (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="c8019-195">Describes the details necessary for successful installation and the details (conditions and actions) required to create a software element in the executable state (that is, the next state).</span></span>

</dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="c8019-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="c8019-196"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-197">Descreve os detalhes necessários para a execução bem-sucedida e os detalhes (condições e ações) necessários para criar um elemento de software no estado em execução (ou seja, o próximo estado).</span><span class="sxs-lookup"><span data-stu-id="c8019-197">Describes the details necessary for successful execution and the details (conditions and actions) required to create a software element in the running state (that is, the next state).</span></span>

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="c8019-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="c8019-198"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-199">Descreve os detalhes necessários para monitorar e operar em um elemento inicial.</span><span class="sxs-lookup"><span data-stu-id="c8019-199">Describes the details necessary to monitor and operate on a start element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c8019-200">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="c8019-200">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-201">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c8019-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-203">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Informações do componente de software DMTF \| 2,5 ")</span><span class="sxs-lookup"><span data-stu-id="c8019-203">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="c8019-204">Sistema operacional de destino do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="c8019-204">Target operating system of the software element.</span></span>

<span data-ttu-id="c8019-205">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-205">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c8019-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="c8019-206"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c8019-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="c8019-207"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="c8019-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="c8019-208"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-209">Mac OS</span><span class="sxs-lookup"><span data-stu-id="c8019-209">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="c8019-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="c8019-210"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-211">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="c8019-211">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="c8019-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="c8019-212"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="c8019-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="c8019-213"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="c8019-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="c8019-214"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="c8019-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="c8019-215"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-216">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="c8019-216">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="c8019-217"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="c8019-217"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-218">HP-UX</span><span class="sxs-lookup"><span data-stu-id="c8019-218">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="c8019-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="c8019-219"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="c8019-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="c8019-220"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="c8019-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="c8019-221"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="c8019-222"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="c8019-222"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="c8019-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="c8019-223"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-224">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="c8019-224">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="c8019-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="c8019-225"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="c8019-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="c8019-226"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-227">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="c8019-227">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="c8019-228"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="c8019-228"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-229">Windows 95</span><span class="sxs-lookup"><span data-stu-id="c8019-229">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="c8019-230"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="c8019-230"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-231">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c8019-231">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="c8019-232"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="c8019-232"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-233">Windows NT</span><span class="sxs-lookup"><span data-stu-id="c8019-233">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="c8019-234"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="c8019-234"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-235">Windows CE</span><span class="sxs-lookup"><span data-stu-id="c8019-235">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="c8019-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="c8019-236"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-237">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="c8019-237">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="c8019-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="c8019-238"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="c8019-239"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="c8019-239"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="c8019-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="c8019-240"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="c8019-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="c8019-241"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="c8019-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="c8019-242"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="c8019-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="c8019-243"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="c8019-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="c8019-244"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="c8019-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="c8019-245"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="c8019-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="c8019-246"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="c8019-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="c8019-247"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="c8019-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="c8019-248"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="c8019-249"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="c8019-249"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-250">Uma série</span><span class="sxs-lookup"><span data-stu-id="c8019-250">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="c8019-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="c8019-251"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-252">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="c8019-252">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="c8019-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="c8019-253"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-254">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="c8019-254">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="c8019-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="c8019-255"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-256">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="c8019-256">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="c8019-257"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="c8019-257"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="c8019-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="c8019-258"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="c8019-259"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="c8019-259"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="c8019-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="c8019-260"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="c8019-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="c8019-261"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="c8019-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="c8019-262"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-263">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="c8019-263">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="c8019-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="c8019-264"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="c8019-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="c8019-265"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="c8019-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="c8019-266"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="c8019-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="c8019-267"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-268">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="c8019-268">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="c8019-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="c8019-269"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="c8019-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="c8019-270"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="c8019-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="c8019-271"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="c8019-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="c8019-272"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="c8019-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="c8019-273"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="c8019-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="c8019-274"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="c8019-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="c8019-275"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="c8019-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="c8019-276"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="c8019-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="c8019-277"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="c8019-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="c8019-278"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="c8019-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="c8019-279"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="c8019-280">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="c8019-280">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="c8019-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="c8019-281"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="c8019-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="c8019-282"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="c8019-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="c8019-283"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="c8019-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="c8019-284"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="c8019-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="c8019-285"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c8019-286">**Versão**</span><span class="sxs-lookup"><span data-stu-id="c8019-286">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8019-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c8019-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8019-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c8019-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8019-289">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Componente DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="c8019-289">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="c8019-290">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="c8019-290">Version of the operation.</span></span>

<span data-ttu-id="c8019-291">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="c8019-291">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="c8019-292"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="c8019-292"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="c8019-293"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="c8019-293"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="c8019-294">Essa propriedade é herdada [**da \_ verificação CIM**](cim-check.md).</span><span class="sxs-lookup"><span data-stu-id="c8019-294">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8019-295">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8019-295">Remarks</span></span>

<span data-ttu-id="c8019-296">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c8019-296">WMI does not implement this class.</span></span>

<span data-ttu-id="c8019-297">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c8019-297">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c8019-298">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c8019-298">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8019-299">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8019-299">Requirements</span></span>



| <span data-ttu-id="c8019-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8019-300">Requirement</span></span> | <span data-ttu-id="c8019-301">Valor</span><span class="sxs-lookup"><span data-stu-id="c8019-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8019-302">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8019-302">Minimum supported client</span></span><br/> | <span data-ttu-id="c8019-303">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8019-303">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c8019-304">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c8019-304">Minimum supported server</span></span><br/> | <span data-ttu-id="c8019-305">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8019-305">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8019-306">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8019-306">Namespace</span></span><br/>                | <span data-ttu-id="c8019-307">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c8019-307">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c8019-308">MOF</span><span class="sxs-lookup"><span data-stu-id="c8019-308">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8019-309"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8019-309"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8019-310">DLL</span><span class="sxs-lookup"><span data-stu-id="c8019-310">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8019-311"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8019-311"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8019-312">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8019-312">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8019-313">**Verificação de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="c8019-313">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

