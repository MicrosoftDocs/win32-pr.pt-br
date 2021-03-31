---
description: Faz referência às informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computador VM) ou um host (quando executado em um sistema de computador host).
ms.assetid: A3DB75BF-91C8-444E-B273-25DF8A5BFA7B
title: Classe Msvm_CompatibilityVector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CompatibilityVector
- Msvm_CompatibilityVector.VectorId
- Msvm_CompatibilityVector.CompareOperation
- Msvm_CompatibilityVector.CompatibilityInfo
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66eba92daf420fb4bd332d3f7d537b7936618ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829036"
---
# <a name="msvm_compatibilityvector-class"></a><span data-ttu-id="67350-103">\_Classe Msvm CompatibilityVector</span><span class="sxs-lookup"><span data-stu-id="67350-103">Msvm\_CompatibilityVector class</span></span>

<span data-ttu-id="67350-104">Faz referência às informações de compatibilidade para uma VM (máquina virtual) (quando executado em um sistema de computador VM) ou um host (quando executado em um sistema de computador host).</span><span class="sxs-lookup"><span data-stu-id="67350-104">References the compatibility info for a virtual machine (VM) (when run on a VM computer system) or a host (when run on a host computer system).</span></span>

<span data-ttu-id="67350-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="67350-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="67350-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67350-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CompatibilityVector
{
  uint32 VectorId;
  uint32 CompareOperation;
  uint64 CompatibilityInfo;
};
```

## <a name="members"></a><span data-ttu-id="67350-107">Membros</span><span class="sxs-lookup"><span data-stu-id="67350-107">Members</span></span>

<span data-ttu-id="67350-108">A classe **Msvm \_ CompatibilityVector** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="67350-108">The **Msvm\_CompatibilityVector** class has these types of members:</span></span>

-   [<span data-ttu-id="67350-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67350-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67350-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67350-110">Properties</span></span>

<span data-ttu-id="67350-111">A classe **Msvm \_ CompatibilityVector** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="67350-111">The **Msvm\_CompatibilityVector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67350-112">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="67350-112">**CompareOperation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67350-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67350-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67350-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67350-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67350-115">Identifica a operação de comparação que retornará true se e somente se dois vetores forem compatíveis.</span><span class="sxs-lookup"><span data-stu-id="67350-115">Identifies the comparison operation that will return true if and only if two vectors are compatible.</span></span> <span data-ttu-id="67350-116">Os dados da VM estão no lado esquerdo da comparação, e os dados do host estão no lado direito.</span><span class="sxs-lookup"><span data-stu-id="67350-116">The VM's data is on the left hand side of the comparison, and the host's data is on the right hand side.</span></span>

<dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>

<span data-ttu-id="67350-117">**Igual** (0)</span><span class="sxs-lookup"><span data-stu-id="67350-117">**Equal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Superset"></span><span id="superset"></span><span id="SUPERSET"></span>

<span data-ttu-id="67350-118">**Superconjunto** (1)</span><span class="sxs-lookup"><span data-stu-id="67350-118">**Superset** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Subset"></span><span id="subset"></span><span id="SUBSET"></span>

<span data-ttu-id="67350-119">**Subconjunto** (2)</span><span class="sxs-lookup"><span data-stu-id="67350-119">**Subset** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disjoint"></span><span id="disjoint"></span><span id="DISJOINT"></span>

<span data-ttu-id="67350-120">Não **contíguo** (3)</span><span class="sxs-lookup"><span data-stu-id="67350-120">**Disjoint** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThan"></span><span id="greaterthan"></span><span id="GREATERTHAN"></span>

<span data-ttu-id="67350-121">**GreaterThan** (4)</span><span class="sxs-lookup"><span data-stu-id="67350-121">**GreaterThan** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="GreaterThanOrEqual"></span><span id="greaterthanorequal"></span><span id="GREATERTHANOREQUAL"></span>

<span data-ttu-id="67350-122">**GreaterThanOrEqual** (5)</span><span class="sxs-lookup"><span data-stu-id="67350-122">**GreaterThanOrEqual** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThan"></span><span id="lessthan"></span><span id="LESSTHAN"></span>

<span data-ttu-id="67350-123">**LessThan** (6)</span><span class="sxs-lookup"><span data-stu-id="67350-123">**LessThan** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="LessThanOrEqual"></span><span id="lessthanorequal"></span><span id="LESSTHANOREQUAL"></span>

<span data-ttu-id="67350-124">**LessThanOrEqual** (7)</span><span class="sxs-lookup"><span data-stu-id="67350-124">**LessThanOrEqual** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiple"></span><span id="multiple"></span><span id="MULTIPLE"></span>

<span data-ttu-id="67350-125">**Múltiplo** (8)</span><span class="sxs-lookup"><span data-stu-id="67350-125">**Multiple** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Divisible"></span><span id="divisible"></span><span id="DIVISIBLE"></span>

<span data-ttu-id="67350-126">**Divisível** (9)</span><span class="sxs-lookup"><span data-stu-id="67350-126">**Divisible** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67350-127">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="67350-127">**CompatibilityInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67350-128">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="67350-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="67350-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67350-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67350-130">Os dados de atributo de compatibilidade reais que são usados para comparação.</span><span class="sxs-lookup"><span data-stu-id="67350-130">The actual compatibility attribute data that is used for comparison.</span></span>

</dd> <dt>

<span data-ttu-id="67350-131">**Vetorid**</span><span class="sxs-lookup"><span data-stu-id="67350-131">**VectorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67350-132">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67350-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67350-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67350-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67350-134">Identifica um vetor de compatibilidade que representa um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="67350-134">Identifies a compatibility vector that represents a specific attribute.</span></span> <span data-ttu-id="67350-135">Essa propriedade é usada para corresponder os vetores correspondentes entre um host e uma VM.</span><span class="sxs-lookup"><span data-stu-id="67350-135">This property is used to match corresponding vectors between a host and a VM.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67350-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="67350-136">Remarks</span></span>

<span data-ttu-id="67350-137">O método [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) da classe [**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) retorna uma matriz de instâncias de **Msvm \_ CompatibilityVector** para o host (se executado no host) ou uma VM (se executado na VM).</span><span class="sxs-lookup"><span data-stu-id="67350-137">The [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class returns an array of **Msvm\_CompatibilityVector** instances for the host (if run on the host) or a VM (if run on the VM).</span></span> <span data-ttu-id="67350-138">Cada entrada **Msvm \_ CompatibilityVector** na lista descreve um vetor de atributo de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="67350-138">Each **Msvm\_CompatibilityVector** entry in the list describes a compatibility attribute vector.</span></span> <span data-ttu-id="67350-139">Para que uma VM seja compatível com um host, todos os seus atributos de compatibilidade devem ser compatíveis com os atributos do host.</span><span class="sxs-lookup"><span data-stu-id="67350-139">For a VM to be compatible with a host, all of its compatibility attributes must be compatible with the host s attributes.</span></span>

<span data-ttu-id="67350-140">Cada **entrada \_ CompatibilityVector Msvm** tem estas propriedades:</span><span class="sxs-lookup"><span data-stu-id="67350-140">Each **Msvm\_CompatibilityVector** entry has these properties:</span></span>

<dl> <dt>

<span data-ttu-id="67350-141">**Vetorid**</span><span class="sxs-lookup"><span data-stu-id="67350-141">**VectorId**</span></span>
</dt> <dd>

<span data-ttu-id="67350-142">Identifica exclusivamente o vetor de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="67350-142">Uniquely identifies the compatibility vector.</span></span> <span data-ttu-id="67350-143">Isso é usado para corresponder os vetores para comparar entre um host e uma VM.</span><span class="sxs-lookup"><span data-stu-id="67350-143">This is used to match the vectors to compare between a host and a VM.</span></span>

</dd> <dt>

<span data-ttu-id="67350-144">**CompareOperation**</span><span class="sxs-lookup"><span data-stu-id="67350-144">**CompareOperation**</span></span>
</dt> <dd>

<span data-ttu-id="67350-145">Identifica a operação de comparação que determina se os vetores são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="67350-145">Identifies the comparison operation that determines whether the vectors are compatible.</span></span>

</dd> <dt>

<span data-ttu-id="67350-146">**CompatibilityInfo**</span><span class="sxs-lookup"><span data-stu-id="67350-146">**CompatibilityInfo**</span></span>
</dt> <dd>

<span data-ttu-id="67350-147">Contém o atributo de compatibilidade real; Isso é efetivamente a carga de atributo (por exemplo, máscara de recurso de processador, tamanho de liberação de linha de cache, etc.)</span><span class="sxs-lookup"><span data-stu-id="67350-147">Contains the actual compatibility attribute; This is effectively the attribute payload (e.g. processor feature mask, cache line flush size, etc.)</span></span>

</dd> </dl>

<span data-ttu-id="67350-148">O conjunto de operações definido para **CompareOperation** envolve a comparação de inteiros básico e a lógica bit-a-bit.</span><span class="sxs-lookup"><span data-stu-id="67350-148">The set of operations defined for **CompareOperation** just involve basic integer comparison and bitwise logic.</span></span> <span data-ttu-id="67350-149">Isso permite que o conteúdo real de **CompatibilityInfo** permaneça opaco.</span><span class="sxs-lookup"><span data-stu-id="67350-149">This enables the actual contents of **CompatibilityInfo** to remain opaque.</span></span> <span data-ttu-id="67350-150">O conjunto de operações inclui:</span><span class="sxs-lookup"><span data-stu-id="67350-150">The set of operations include:</span></span>



| <span data-ttu-id="67350-151">CompareOperation</span><span class="sxs-lookup"><span data-stu-id="67350-151">CompareOperation</span></span> | <span data-ttu-id="67350-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="67350-152">Description</span></span>                                      | <span data-ttu-id="67350-153">Comparação de pseudocódigo</span><span class="sxs-lookup"><span data-stu-id="67350-153">Pseudocode Comparison</span></span>                |
|------------------|--------------------------------------------------|--------------------------------------|
| <span data-ttu-id="67350-154">VmCcEqual</span><span class="sxs-lookup"><span data-stu-id="67350-154">VmCcEqual</span></span>        | <span data-ttu-id="67350-155">VmAttr deve ser igual a HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-155">VmAttr must equal HostAttr</span></span>                       | <span data-ttu-id="67350-156">If (VmAttr = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-156">If (VmAttr == HostAttr)</span></span>              |
| <span data-ttu-id="67350-157">VmCcSuperSet</span><span class="sxs-lookup"><span data-stu-id="67350-157">VmCcSuperSet</span></span>     | <span data-ttu-id="67350-158">VmAttr deve ser um superconjunto de HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-158">VmAttr must be a superset of HostAttr</span></span>            | <span data-ttu-id="67350-159">If (VmAttr & HostAttr) = = HostAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-159">If ((VmAttr & HostAttr) == HostAttr)</span></span> |
| <span data-ttu-id="67350-160">VmCcSubSet</span><span class="sxs-lookup"><span data-stu-id="67350-160">VmCcSubSet</span></span>       | <span data-ttu-id="67350-161">VmAttr deve ser um subconjunto de HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-161">VmAttr must be a subset of HostAttr</span></span>              | <span data-ttu-id="67350-162">If (VmAttr & HostAttr) = = VmAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-162">If ((VmAttr & HostAttr) == VmAttr)</span></span>   |
| <span data-ttu-id="67350-163">VmCcDisjointSet</span><span class="sxs-lookup"><span data-stu-id="67350-163">VmCcDisjointSet</span></span>  | <span data-ttu-id="67350-164">VmAttr deve ser um conjunto não contíguo de HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-164">VmAttr must be a disjoint set from HostAttr</span></span>      | <span data-ttu-id="67350-165">If ((VmAttr & HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="67350-165">If ((VmAttr & HostAttr) == 0)</span></span>        |
| <span data-ttu-id="67350-166">VmCcGreater</span><span class="sxs-lookup"><span data-stu-id="67350-166">VmCcGreater</span></span>      | <span data-ttu-id="67350-167">VmAttr deve ser maior que HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-167">VmAttr must be greater than HostAttr</span></span>             | <span data-ttu-id="67350-168">If (VmAttr > HostAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-168">If (VmAttr > HostAttr)</span></span>            |
| <span data-ttu-id="67350-169">VmCcGreaterEqual</span><span class="sxs-lookup"><span data-stu-id="67350-169">VmCcGreaterEqual</span></span> | <span data-ttu-id="67350-170">VmAttr deve ser maior ou igual a HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-170">VmAttr must be greater than or equal to HostAttr</span></span> | <span data-ttu-id="67350-171">If (VmAttr >= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-171">If (VmAttr >= HostAttr)</span></span>           |
| <span data-ttu-id="67350-172">VmCcLess</span><span class="sxs-lookup"><span data-stu-id="67350-172">VmCcLess</span></span>         | <span data-ttu-id="67350-173">VmAttr deve ser menor que HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-173">VmAttr must be less than HostAttr</span></span>                | <span data-ttu-id="67350-174">If (VmAttr < HostAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-174">If (VmAttr < HostAttr)</span></span>            |
| <span data-ttu-id="67350-175">VmCcLessEqual</span><span class="sxs-lookup"><span data-stu-id="67350-175">VmCcLessEqual</span></span>    | <span data-ttu-id="67350-176">VmAttr deve ser menor ou igual a HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-176">VmAttr must be less than or equal to HostAttr</span></span>    | <span data-ttu-id="67350-177">If (VmAttr <= HostAttr)</span><span class="sxs-lookup"><span data-stu-id="67350-177">If (VmAttr <= HostAttr)</span></span>           |
| <span data-ttu-id="67350-178">VmCcMultiple</span><span class="sxs-lookup"><span data-stu-id="67350-178">VmCcMultiple</span></span>     | <span data-ttu-id="67350-179">VmAttr deve ser um múltiplo de HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-179">VmAttr must be a multiple of HostAttr</span></span>            | <span data-ttu-id="67350-180">If ((VmAttr% HostAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="67350-180">If ((VmAttr % HostAttr) == 0)</span></span>        |
| <span data-ttu-id="67350-181">VmCcDivisor</span><span class="sxs-lookup"><span data-stu-id="67350-181">VmCcDivisor</span></span>      | <span data-ttu-id="67350-182">VmAttr deve ser um divisor de HostAttr</span><span class="sxs-lookup"><span data-stu-id="67350-182">VmAttr must be a divisor of HostAttr</span></span>             | <span data-ttu-id="67350-183">If ((HostAttr% VmAttr) = = 0)</span><span class="sxs-lookup"><span data-stu-id="67350-183">If ((HostAttr % VmAttr) == 0)</span></span>        |



 

<span data-ttu-id="67350-184">O SCVMM precisa executar estas etapas para determinar se uma VM é compatível com um host.</span><span class="sxs-lookup"><span data-stu-id="67350-184">SCVMM needs to do these steps to determine whether a VM is compatible with a host.</span></span>

<span data-ttu-id="67350-185">**Para determinar se uma VM é compatível com um host**</span><span class="sxs-lookup"><span data-stu-id="67350-185">**To determine whether a VM is compatible with a host**</span></span>

1.  <span data-ttu-id="67350-186">Iterar em todos os elementos **Msvm \_ CompatibilityVector** para a VM.</span><span class="sxs-lookup"><span data-stu-id="67350-186">Iterate through all of the **Msvm\_CompatibilityVector** elements for the VM.</span></span>
2.  <span data-ttu-id="67350-187">Para cada elemento **Msvm \_ CompatibilityVector** , use a operação de compatibilidade especificada em **CompareOperation** para comparar o vetor de compatibilidade de hardware de VM s com o vetor de compatibilidade correspondente para o host.</span><span class="sxs-lookup"><span data-stu-id="67350-187">For each **Msvm\_CompatibilityVector** element, use the compatibility operation specified in **CompareOperation** to compare the VM s hardware compatibility vector with the corresponding compatibility vector for the host.</span></span>
3.  <span data-ttu-id="67350-188">Se todos os elementos **Msvm \_ COMPATIBILITYVECTOR** da VM forem considerados compatíveis, a VM será compatível com o host (da perspectiva do recurso do processador).</span><span class="sxs-lookup"><span data-stu-id="67350-188">If the all of the **Msvm\_CompatibilityVector** elements from the VM are deemed compatible, the VM is compatible with the host (from a processor feature perspective).</span></span>

## <a name="requirements"></a><span data-ttu-id="67350-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67350-189">Requirements</span></span>



| <span data-ttu-id="67350-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="67350-190">Requirement</span></span> | <span data-ttu-id="67350-191">Valor</span><span class="sxs-lookup"><span data-stu-id="67350-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67350-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67350-192">Minimum supported client</span></span><br/> | <span data-ttu-id="67350-193">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="67350-193">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="67350-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67350-194">Minimum supported server</span></span><br/> | <span data-ttu-id="67350-195">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="67350-195">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="67350-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="67350-196">Namespace</span></span><br/>                | <span data-ttu-id="67350-197">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="67350-197">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67350-198">MOF</span><span class="sxs-lookup"><span data-stu-id="67350-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67350-199"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67350-199"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67350-200">DLL</span><span class="sxs-lookup"><span data-stu-id="67350-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67350-201"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67350-201"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67350-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="67350-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67350-203">**GetSystemCompatibilityVectors**</span><span class="sxs-lookup"><span data-stu-id="67350-203">**GetSystemCompatibilityVectors**</span></span>](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[<span data-ttu-id="67350-204">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="67350-204">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




