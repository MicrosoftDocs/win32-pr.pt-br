---
description: A \_ classe CIM ProcessExecutable representa um vínculo entre um processo e um arquivo de dados e indica que o arquivo participa da execução do processo.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: Classe CIM_ProcessExecutable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010284"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="e86e2-103">\_Classe CIM ProcessExecutable</span><span class="sxs-lookup"><span data-stu-id="e86e2-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="e86e2-104">A classe **CIM \_ ProcessExecutable** representa um vínculo entre um processo e um arquivo de dados e indica que o arquivo participa da execução do processo.</span><span class="sxs-lookup"><span data-stu-id="e86e2-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e86e2-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e86e2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e86e2-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e86e2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e86e2-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e86e2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e86e2-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e86e2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86e2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e86e2-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="e86e2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e86e2-110">Members</span></span>

<span data-ttu-id="e86e2-111">A classe **CIM \_ ProcessExecutable** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e86e2-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="e86e2-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e86e2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e86e2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e86e2-113">Properties</span></span>

<span data-ttu-id="e86e2-114">A classe **CIM \_ ProcessExecutable** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e86e2-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e86e2-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="e86e2-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86e2-116">Tipo de dados **: \_ DataFile do CIM**</span><span class="sxs-lookup"><span data-stu-id="e86e2-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e86e2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e86e2-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e86e2-119">Um [**\_ DataFile do CIM**](cim-datafile.md) que descreve o arquivo de dados que participa da execução do processo.</span><span class="sxs-lookup"><span data-stu-id="e86e2-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="e86e2-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="e86e2-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86e2-121">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e86e2-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e86e2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-123">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e86e2-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e86e2-124">Endereço base do módulo no espaço de endereço do processo associado.</span><span class="sxs-lookup"><span data-stu-id="e86e2-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="e86e2-125">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e86e2-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="e86e2-126">**Depende**</span><span class="sxs-lookup"><span data-stu-id="e86e2-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86e2-127">Tipo de dados **: \_ processo CIM**</span><span class="sxs-lookup"><span data-stu-id="e86e2-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e86e2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-129">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (dependente), [**chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e86e2-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e86e2-130">Um [**\_ processo CIM**](cim-process.md) que descreve o processo.</span><span class="sxs-lookup"><span data-stu-id="e86e2-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="e86e2-131">**GlobalProcessCount**</span><span class="sxs-lookup"><span data-stu-id="e86e2-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86e2-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e86e2-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e86e2-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-134">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e86e2-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e86e2-135">Número atual de processos que têm o arquivo carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="e86e2-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="e86e2-136">**ModuleInstance**</span><span class="sxs-lookup"><span data-stu-id="e86e2-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86e2-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e86e2-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e86e2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-139">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e86e2-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e86e2-140">Identificador de instância do Win32.</span><span class="sxs-lookup"><span data-stu-id="e86e2-140">Win32 instance handle.</span></span> <span data-ttu-id="e86e2-141">Esta propriedade é obsoleta e não há nenhum valor de substituição.</span><span class="sxs-lookup"><span data-stu-id="e86e2-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="e86e2-142">**ProcessCount**</span><span class="sxs-lookup"><span data-stu-id="e86e2-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e86e2-143">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e86e2-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e86e2-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e86e2-145">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="e86e2-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="e86e2-146">Contagem de referência do arquivo no processo associado.</span><span class="sxs-lookup"><span data-stu-id="e86e2-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e86e2-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="e86e2-147">Remarks</span></span>

<span data-ttu-id="e86e2-148">A classe **CIM \_ ProcessExecutable** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e86e2-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e86e2-149">O WMI implementa a classe **CIM \_ ProcessExecutable** .</span><span class="sxs-lookup"><span data-stu-id="e86e2-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="e86e2-150">A classe **CIM \_ ProcessExecutable** é uma classe dinâmica.</span><span class="sxs-lookup"><span data-stu-id="e86e2-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="e86e2-151">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e86e2-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e86e2-152">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e86e2-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86e2-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e86e2-153">Requirements</span></span>



| <span data-ttu-id="e86e2-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="e86e2-154">Requirement</span></span> | <span data-ttu-id="e86e2-155">Valor</span><span class="sxs-lookup"><span data-stu-id="e86e2-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e86e2-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e86e2-156">Minimum supported client</span></span><br/> | <span data-ttu-id="e86e2-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e86e2-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e86e2-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e86e2-158">Minimum supported server</span></span><br/> | <span data-ttu-id="e86e2-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e86e2-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e86e2-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="e86e2-160">Namespace</span></span><br/>                | <span data-ttu-id="e86e2-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e86e2-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e86e2-162">MOF</span><span class="sxs-lookup"><span data-stu-id="e86e2-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e86e2-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e86e2-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e86e2-164">DLL</span><span class="sxs-lookup"><span data-stu-id="e86e2-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e86e2-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e86e2-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e86e2-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="e86e2-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86e2-167">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="e86e2-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

