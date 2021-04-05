---
description: Valida o sistema planejado especificado.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Método ValidatePlannedSystem da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663004"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f02d4-103">Método ValidatePlannedSystem da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="f02d4-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f02d4-104">Valida o sistema planejado especificado.</span><span class="sxs-lookup"><span data-stu-id="f02d4-104">Validates the specified planned system.</span></span> <span data-ttu-id="f02d4-105">Isso envolve verificações de configuração de máquina virtual, dispositivos, configuração de instantâneo, dispositivos de instantâneo, arquivos de estado salvos e arquivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f02d4-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="f02d4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f02d4-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f02d4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f02d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f02d4-108">*PlannedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f02d4-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f02d4-109">Uma referência a um objeto [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa o sistema planejado a ser validado.</span><span class="sxs-lookup"><span data-stu-id="f02d4-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="f02d4-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f02d4-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f02d4-111">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f02d4-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f02d4-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f02d4-112">Return value</span></span>

<span data-ttu-id="f02d4-113">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f02d4-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f02d4-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f02d4-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f02d4-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f02d4-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f02d4-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f02d4-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f02d4-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f02d4-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f02d4-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f02d4-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f02d4-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f02d4-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f02d4-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f02d4-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f02d4-127">**Arquivo em uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="f02d4-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="f02d4-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f02d4-128">Examples</span></span>

<span data-ttu-id="f02d4-129">O exemplo de C# a seguir usa o método **ValidatePlannedSystem** para validar uma máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="f02d4-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="f02d4-130">Esse código é obtido do [exemplo de máquinas virtuais planejadas do Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="f02d4-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="f02d4-131">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f02d4-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f02d4-132">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="f02d4-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="f02d4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02d4-133">Requirements</span></span>



| <span data-ttu-id="f02d4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f02d4-134">Requirement</span></span> | <span data-ttu-id="f02d4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f02d4-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02d4-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f02d4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f02d4-137">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f02d4-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f02d4-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f02d4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f02d4-139">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f02d4-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f02d4-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f02d4-140">Namespace</span></span><br/>                | <span data-ttu-id="f02d4-141">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f02d4-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f02d4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f02d4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f02d4-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f02d4-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f02d4-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f02d4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f02d4-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f02d4-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f02d4-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f02d4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02d4-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f02d4-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

