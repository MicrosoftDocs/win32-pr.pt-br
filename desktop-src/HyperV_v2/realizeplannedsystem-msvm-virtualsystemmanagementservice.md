---
description: Valida a configuração de uma máquina virtual planejada e a converte em uma máquina virtual realizada.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Método RealizePlannedSystem da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171300"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="30ba0-103">Método RealizePlannedSystem da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="30ba0-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="30ba0-104">Valida a configuração de uma máquina virtual planejada e a converte em uma máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="30ba0-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="30ba0-105">Todos os arquivos de tempo de execução ou de estado salvos associados à máquina virtual serão copiados do diretório de importação para a raiz de dados da máquina virtual, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="30ba0-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="30ba0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30ba0-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="30ba0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30ba0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30ba0-108">*PlannedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30ba0-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30ba0-109">Uma referência à instância [**de \_ PlannedComputerSystem Msvm**](msvm-plannedcomputersystem.md) que deve ser convertida em uma máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="30ba0-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="30ba0-110">*ResultingSystem* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="30ba0-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ba0-111">Se a operação for concluída de forma síncrona, uma referência a um objeto de [**\_ sistema**](msvm-computersystem.md) de computador CIM que representa a máquina virtual realizada resultante.</span><span class="sxs-lookup"><span data-stu-id="30ba0-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="30ba0-112">Tipo de dados atualizado do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="30ba0-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="30ba0-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="30ba0-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30ba0-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="30ba0-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30ba0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30ba0-115">Return value</span></span>

<span data-ttu-id="30ba0-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="30ba0-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="30ba0-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="30ba0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="30ba0-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="30ba0-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="30ba0-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="30ba0-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="30ba0-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="30ba0-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="30ba0-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="30ba0-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="30ba0-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="30ba0-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="30ba0-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="30ba0-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="30ba0-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="30ba0-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30ba0-130">Examples</span></span>

<span data-ttu-id="30ba0-131">O exemplo de C# a seguir usa o método **RealizePlannedSystem** para obter uma máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="30ba0-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="30ba0-132">Esse código é obtido do [exemplo de máquinas virtuais planejadas do Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="30ba0-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="30ba0-133">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="30ba0-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30ba0-134">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="30ba0-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="30ba0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30ba0-135">Requirements</span></span>



| <span data-ttu-id="30ba0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="30ba0-136">Requirement</span></span> | <span data-ttu-id="30ba0-137">Valor</span><span class="sxs-lookup"><span data-stu-id="30ba0-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30ba0-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30ba0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="30ba0-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="30ba0-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="30ba0-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30ba0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="30ba0-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="30ba0-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="30ba0-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="30ba0-142">Namespace</span></span><br/>                | <span data-ttu-id="30ba0-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="30ba0-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="30ba0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="30ba0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30ba0-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30ba0-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30ba0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="30ba0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30ba0-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30ba0-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30ba0-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="30ba0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30ba0-149">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="30ba0-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

