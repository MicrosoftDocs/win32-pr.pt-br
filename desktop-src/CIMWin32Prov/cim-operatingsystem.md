---
description: A \_ classe CIM OperatingSystem representa um sistema operacional de computador, que é composto por software e firmware que tornam o hardware de um sistema de computador utilizável.
ms.assetid: 014d2553-e1ac-4394-84ae-307af3658f6e
ms.tgt_platform: multiple
title: Classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem
- CIM_OperatingSystem.Caption
- CIM_OperatingSystem.CreationClassName
- CIM_OperatingSystem.CSCreationClassName
- CIM_OperatingSystem.CSName
- CIM_OperatingSystem.CurrentTimeZone
- CIM_OperatingSystem.Description
- CIM_OperatingSystem.Distributed
- CIM_OperatingSystem.FreePhysicalMemory
- CIM_OperatingSystem.FreeSpaceInPagingFiles
- CIM_OperatingSystem.FreeVirtualMemory
- CIM_OperatingSystem.InstallDate
- CIM_OperatingSystem.LastBootUpTime
- CIM_OperatingSystem.LocalDateTime
- CIM_OperatingSystem.MaxNumberOfProcesses
- CIM_OperatingSystem.MaxProcessMemorySize
- CIM_OperatingSystem.Name
- CIM_OperatingSystem.NumberOfLicensedUsers
- CIM_OperatingSystem.NumberOfProcesses
- CIM_OperatingSystem.NumberOfUsers
- CIM_OperatingSystem.OSType
- CIM_OperatingSystem.OtherTypeDescription
- CIM_OperatingSystem.SizeStoredInPagingFiles
- CIM_OperatingSystem.Status
- CIM_OperatingSystem.TotalSwapSpaceSize
- CIM_OperatingSystem.TotalVirtualMemorySize
- CIM_OperatingSystem.TotalVisibleMemorySize
- CIM_OperatingSystem.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b4af54a0f086bee4b743b083c27a67777786bc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500973"
---
# <a name="cim_operatingsystem-class"></a><span data-ttu-id="1e5cb-103">\_Classe de OPERATINGSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="1e5cb-103">CIM\_OperatingSystem class</span></span>

<span data-ttu-id="1e5cb-104">A classe **CIM \_ OperatingSystem** representa um sistema operacional de computador, que é composto por software e firmware que tornam o hardware de um sistema de computador utilizável.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-104">The **CIM\_OperatingSystem** class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e5cb-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1e5cb-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1e5cb-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1e5cb-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5cb-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e5cb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C565-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_OperatingSystem : CIM_LogicalElement
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  sint16   CurrentTimeZone;
  string   Description;
  boolean  Distributed;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint16   OSType;
  string   OtherTypeDescription;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1e5cb-110">Membros</span><span class="sxs-lookup"><span data-stu-id="1e5cb-110">Members</span></span>

<span data-ttu-id="1e5cb-111">A classe **CIM \_ OperatingSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1e5cb-111">The **CIM\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="1e5cb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e5cb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1e5cb-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e5cb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1e5cb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1e5cb-114">Methods</span></span>

<span data-ttu-id="1e5cb-115">A classe **CIM \_ OperatingSystem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-115">The **CIM\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="1e5cb-116">Método</span><span class="sxs-lookup"><span data-stu-id="1e5cb-116">Method</span></span>                                                           | <span data-ttu-id="1e5cb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e5cb-117">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e5cb-118">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-118">**Reboot**</span></span>](reboot-method-in-class-cim-operatingsystem.md)     | <span data-ttu-id="1e5cb-119">Método de classe que desliga o sistema de computador e, em seguida, o reinicia.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-119">Class method that shuts down the computer system, then restarts it.</span></span> <span data-ttu-id="1e5cb-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-120">Not implemented by WMI.</span></span><br/>                                 |
| [<span data-ttu-id="1e5cb-121">**Desligar**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-121">**Shutdown**</span></span>](shutdown-method-in-class-cim-operatingsystem.md) | <span data-ttu-id="1e5cb-122">Método de classe que descarrega programas e DLLs para o ponto em que é seguro desligar o computador.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-122">Class method that unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span> <span data-ttu-id="1e5cb-123">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1e5cb-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1e5cb-124">Properties</span></span>

<span data-ttu-id="1e5cb-125">A classe **CIM \_ OperatingSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-125">The **CIM\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e5cb-126">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-129">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-130">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-130">Short textual description of the object.</span></span>

<span data-ttu-id="1e5cb-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-135">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-136">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="1e5cb-137">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-138">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-141">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-142">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-146">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-147">Nome do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-148">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-148">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-149">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-149">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-151">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutos")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-152">Número de minutos em que o sistema operacional é deslocado do horário de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-152">Number of minutes the operating system is offset from Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="1e5cb-153">O número é positivo, negativo ou zero.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-153">The number is positive, negative, or zero.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-157">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-157">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-158">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-158">Textual description of the object.</span></span>

<span data-ttu-id="1e5cb-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-160">**Fornecido**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-160">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-161">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-163">Se **for true**, o sistema operacional será distribuído entre vários nós de sistema de computador, que devem ser agrupados como um cluster.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-163">If **TRUE**, the operating system is distributed across several computer system nodes, which should be grouped as a cluster.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-164">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-164">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-165">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-167">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-167">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-168">Número de kilobytes de memória física atualmente não utilizados e disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-168">Number of kilobytes of physical memory currently unused and available.</span></span>

<span data-ttu-id="1e5cb-169">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-169">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-170">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-170">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-171">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-173">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Configurações de memória do sistema DMTF \| 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-174">Número de kilobytes que podem ser mapeados nos arquivos de paginação do sistema operacional sem fazer com que outras páginas sejam trocadas. Um valor de 0 indica que não há arquivos de paginação.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-174">Number of kilobytes that can be mapped into the operating system's paging files without causing other pages to be swapped out. A value of 0 indicates that there are no paging files.</span></span>

<span data-ttu-id="1e5cb-175">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-175">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-176">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-176">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-177">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-177">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-179">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-179">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-180">Número de kilobytes de memória virtual atualmente não utilizados e disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-180">Number of kilobytes of virtual memory currently unused and available.</span></span> <span data-ttu-id="1e5cb-181">Por exemplo, isso pode ser calculado adicionando a quantidade de RAM livre à quantidade de espaço de paginação livre (ou seja, adicionando as propriedades **FreePhysicalMemory** e **FreeSpaceInPagingFiles** ).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-181">For example, this can be calculated by adding the amount of free RAM to the amount of free paging space (that is, adding the **FreePhysicalMemory** and **FreeSpaceInPagingFiles** properties).</span></span>

<span data-ttu-id="1e5cb-182">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-183">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-183">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-184">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-184">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-186">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-187">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-187">Date and time the object was installed.</span></span> <span data-ttu-id="1e5cb-188">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-188">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1e5cb-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-190">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-190">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-191">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-191">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-193">Hora em que o sistema operacional foi inicializado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-193">Time when the operating system was last booted.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-194">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-194">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-195">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-195">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-197">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemDate "," MIF. \|Informações gerais do DMTF \| 1,6 ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-198">A noção do sistema operacional da data e hora local do dia.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-198">Operating system's notion of the local date and time of day.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-199">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-199">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-200">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-202">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-203">Número máximo de contextos de processo aos quais o sistema operacional pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-203">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="1e5cb-204">Se não houver um máximo fixo, o valor deverá ser 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-204">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="1e5cb-205">Em sistemas que têm um máximo fixo, esse objeto pode ajudar a diagnosticar falhas que ocorrem quando o máximo é atingido.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-205">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached.</span></span> <span data-ttu-id="1e5cb-206">Se for desconhecido, digite-1.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-206">If unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-207">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-207">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-208">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-208">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-210">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-211">Número máximo de kilobytes de memória que podem ser alocados a um processo.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-211">Maximum number of kilobytes of memory that can be allocated to a process.</span></span> <span data-ttu-id="1e5cb-212">Para sistemas operacionais sem memória virtual, esse valor é normalmente igual à quantidade total de memória física, menos memória usada pelo BIOS e pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-212">For operating systems with no virtual memory, this value is typically equal to the total amount of physical memory, minus memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="1e5cb-213">Para alguns sistemas operacionais, esse valor pode ser infinito; nesse caso, 0 deve ser inserido.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-213">For some operating systems, this value can be infinity, in which case 0 should be entered.</span></span> <span data-ttu-id="1e5cb-214">Em outros casos, esse valor pode ser uma constante, por exemplo, 2 GB ou 4 GB.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-214">In other cases, this value can be a constant, for example, 2 GB or 4 GB.</span></span>

<span data-ttu-id="1e5cb-215">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-215">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-216">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-217">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-219">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-219">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-220">Chave de uma instância do sistema operacional em um sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-220">Key of an operating system instance within a computer system.</span></span>

<span data-ttu-id="1e5cb-221">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-222">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-222">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-223">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-224">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-225">Número de licenças de usuário para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-225">Number of user licenses for the operating system.</span></span> <span data-ttu-id="1e5cb-226">Se for ilimitado, insira 0, se for desconhecido, digite-1.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-226">If unlimited, enter 0, if unknown, enter -1.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-227">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-227">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-228">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-228">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-230">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-230">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-231">Número de contextos de processo atualmente carregados ou em execução no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-231">Number of process contexts currently loaded or running on the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-232">**NumberOfUsers**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-232">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-233">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-235">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-236">Número de sessões de usuário para as quais o sistema operacional está armazenando informações de estado no momento.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-236">Number of user sessions for which the operating system is currently storing state information.</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-237">**OSType**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-237">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-238">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-239">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-239">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-240">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**sistema \_ operacional CIM**.**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-240">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-241">Tipo do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-241">Type of operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1e5cb-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1e5cb-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="1e5cb-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-244"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-245">Mac OS</span><span class="sxs-lookup"><span data-stu-id="1e5cb-245">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="1e5cb-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-246"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-247">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="1e5cb-247">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="1e5cb-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-248"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="1e5cb-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-249"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="1e5cb-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-250"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="1e5cb-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-251"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-252">Abrir VMS</span><span class="sxs-lookup"><span data-stu-id="1e5cb-252">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="1e5cb-253"><span id="HPUX"></span><span id="hpux"></span>HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="1e5cb-253"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-254">HP-UX</span><span class="sxs-lookup"><span data-stu-id="1e5cb-254">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="1e5cb-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-255"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="1e5cb-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-256"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="1e5cb-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-257"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="1e5cb-258"><span id="OS_2"></span><span id="os_2"></span>**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-258"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="1e5cb-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-259"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-260">VM (máquina virtual) da Microsoft para Java</span><span class="sxs-lookup"><span data-stu-id="1e5cb-260">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="1e5cb-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-261"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="1e5cb-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-262"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-263">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="1e5cb-263">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="1e5cb-264"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-264"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-265">Windows 95</span><span class="sxs-lookup"><span data-stu-id="1e5cb-265">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="1e5cb-266"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-266"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-267">Windows 98</span><span class="sxs-lookup"><span data-stu-id="1e5cb-267">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="1e5cb-268"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-268"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-269">Windows NT</span><span class="sxs-lookup"><span data-stu-id="1e5cb-269">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="1e5cb-270"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-270"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-271">Windows CE</span><span class="sxs-lookup"><span data-stu-id="1e5cb-271">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="1e5cb-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-272"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-273">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="1e5cb-273">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="1e5cb-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-274"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="1e5cb-275"><span id="OSF"></span><span id="osf"></span>**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-275"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="1e5cb-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-276"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="1e5cb-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-277"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="1e5cb-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-278"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="1e5cb-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-279"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="1e5cb-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-280"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="1e5cb-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-281"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="1e5cb-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-282"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="1e5cb-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-283"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="1e5cb-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-284"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="1e5cb-285"><span id="ASERIES"></span><span id="aseries"></span>**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-285"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-286">Uma série</span><span class="sxs-lookup"><span data-stu-id="1e5cb-286">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="1e5cb-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-287"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-288">NSK tandem</span><span class="sxs-lookup"><span data-stu-id="1e5cb-288">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="1e5cb-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-289"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-290">NT em tandem</span><span class="sxs-lookup"><span data-stu-id="1e5cb-290">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="1e5cb-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-291"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-292">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="1e5cb-292">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="1e5cb-293"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-293"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="1e5cb-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-294"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="1e5cb-295"><span id="XENIX"></span><span id="xenix"></span>**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-295"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="1e5cb-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-296"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="1e5cb-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-297"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="1e5cb-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-298"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-299">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="1e5cb-299">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="1e5cb-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-300"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="1e5cb-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-301"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="1e5cb-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-302"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="1e5cb-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-303"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-304">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="1e5cb-304">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="1e5cb-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-305"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="1e5cb-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-306"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="1e5cb-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-307"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="1e5cb-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-308"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="1e5cb-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-309"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="1e5cb-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-310"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="1e5cb-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-311"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="1e5cb-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-312"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="1e5cb-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-313"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="1e5cb-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-314"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="1e5cb-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-315"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="1e5cb-316">Sistema operacional Palm</span><span class="sxs-lookup"><span data-stu-id="1e5cb-316">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="1e5cb-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-317"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="1e5cb-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-318"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="1e5cb-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-319"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="1e5cb-320"><span id="OS_390"></span><span id="os_390"></span>**Os/390** (60)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-320"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="1e5cb-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-321"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="1e5cb-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="1e5cb-322"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1e5cb-323">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-323">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-326">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**sistema \_ operacional CIM**.**OSType**")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-326">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_OperatingSystem**.**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-327">Descreve o tipo de fabricante e sistema operacional quando a propriedade **OSType** é definida como 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="1e5cb-327">Describes the manufacturer and operating system type when the **OSType** property is set to 1 ("Other").</span></span> <span data-ttu-id="1e5cb-328">O formato da cadeia de caracteres inserida em **OtherTypeDescription** deve ser semelhante às cadeias de caracteres de **valores** definidas para **OSType**.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-328">The format of the string inserted in **OtherTypeDescription** should be similar to the **Values** strings defined for **OSType**.</span></span> <span data-ttu-id="1e5cb-329">Essa propriedade deve ser definida como NULL quando **OSType** é um valor diferente de 1 (um).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-329">This property should be set to null when **OSType** is a value other than 1 (one).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-330">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-330">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-331">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-332">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-333">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Configurações de memória do sistema DMTF \| 1,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" quilobytes ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-334">Número de kilobytes que podem ser armazenados nos arquivos de paginação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-334">Number of kilobytes that can be stored in the operating system's paging files.</span></span> <span data-ttu-id="1e5cb-335">Esse número não representa o tamanho físico real do arquivo de paginação no disco.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-335">This number does not represent the actual physical size of the paging file on disk.</span></span> <span data-ttu-id="1e5cb-336">Um valor de 0 (zero) indica que não há arquivos de paginação.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-336">A value of 0 (zero)indicates that there are no paging files.</span></span>

<span data-ttu-id="1e5cb-337">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-337">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-338">**Status**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-338">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-339">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-340">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-341">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-341">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-342">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-342">Current status of the object.</span></span>

<span data-ttu-id="1e5cb-343">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1e5cb-344">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1e5cb-344">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1e5cb-345">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-345">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1e5cb-346">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-346">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1e5cb-347">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-347">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1e5cb-348">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-348">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1e5cb-349">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-349">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1e5cb-350">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-350">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1e5cb-351">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-351">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1e5cb-352">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-352">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1e5cb-353">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-353">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1e5cb-354">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-354">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1e5cb-355">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-355">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1e5cb-356">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-356">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1e5cb-357">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-357">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-358">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-359">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-360">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-361">Espaço total de permuta, em quilobytes.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-361">Total swap space, in kilobytes.</span></span> <span data-ttu-id="1e5cb-362">Esse valor pode ser nulo (não especificado) se o espaço de permuta não for diferenciado dos arquivos de paginação.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-362">This value can be null (unspecified) if swap space is not distinguished from page files.</span></span> <span data-ttu-id="1e5cb-363">No entanto, alguns sistemas operacionais distinguem esses conceitos.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-363">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="1e5cb-364">Por exemplo, processos inteiros podem ser "trocados" no UNIX quando a lista de páginas livre cai e permanece abaixo de uma quantidade especificada.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-364">For example, entire processes can be "swapped out" in UNIX when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="1e5cb-365">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-365">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-366">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-366">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-367">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-369">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-369">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-370">Número de kilobytes de memória virtual.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-370">Number of kilobytes of virtual memory.</span></span> <span data-ttu-id="1e5cb-371">Por exemplo, calcule isso adicionando a quantidade de RAM total à quantidade de espaço de paginação (ou seja, adicione a quantidade de memória ou agregada pelo sistema de computador à propriedade **SizeStoredInPagingFiles** .</span><span class="sxs-lookup"><span data-stu-id="1e5cb-371">For example, calculate this by adding the amount of total RAM to the amount of paging space (that is, add the amount of memory in or aggregated by the computer system to the **SizeStoredInPagingFiles** property.</span></span>

<span data-ttu-id="1e5cb-372">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-373">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-373">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-374">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-374">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-376">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-376">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-377">Quantidade total de memória física, em quilobytes, disponível para o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-377">Total amount of physical memory, in kilobytes, available to the operating system.</span></span> <span data-ttu-id="1e5cb-378">Esse valor não indica necessariamente a quantidade real de memória física, mas o que é relatado para o sistema operacional como disponível para ele.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-378">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="1e5cb-379">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-379">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="1e5cb-380">**Versão**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e5cb-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1e5cb-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e5cb-383">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operacional DMTF \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="1e5cb-383">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="1e5cb-384">Versão da operação.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-384">Version of the operation.</span></span>

<span data-ttu-id="1e5cb-385">A versão da operação deve estar em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="1e5cb-385">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="1e5cb-386"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="1e5cb-386"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="1e5cb-387"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="1e5cb-387"><major>.<minor><letter><revision></span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e5cb-388">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e5cb-388">Remarks</span></span>

<span data-ttu-id="1e5cb-389">A classe **CIM \_ OperatingSystem** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-389">The **CIM\_OperatingSystem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="1e5cb-390">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-390">WMI does not implement this class.</span></span> <span data-ttu-id="1e5cb-391">Para classes WMI que são derivadas do **sistema \_ operacional CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1e5cb-391">For WMI classes that are derived from **CIM\_OperatingSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="1e5cb-392">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-392">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1e5cb-393">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="1e5cb-393">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5cb-394">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e5cb-394">Requirements</span></span>



| <span data-ttu-id="1e5cb-395">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e5cb-395">Requirement</span></span> | <span data-ttu-id="1e5cb-396">Valor</span><span class="sxs-lookup"><span data-stu-id="1e5cb-396">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5cb-397">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e5cb-397">Minimum supported client</span></span><br/> | <span data-ttu-id="1e5cb-398">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e5cb-398">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e5cb-399">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e5cb-399">Minimum supported server</span></span><br/> | <span data-ttu-id="1e5cb-400">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e5cb-400">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e5cb-401">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e5cb-401">Namespace</span></span><br/>                | <span data-ttu-id="1e5cb-402">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1e5cb-402">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e5cb-403">MOF</span><span class="sxs-lookup"><span data-stu-id="1e5cb-403">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e5cb-404"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e5cb-404"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e5cb-405">DLL</span><span class="sxs-lookup"><span data-stu-id="1e5cb-405">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e5cb-406"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e5cb-406"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5cb-407">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e5cb-407">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5cb-408">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="1e5cb-408">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

