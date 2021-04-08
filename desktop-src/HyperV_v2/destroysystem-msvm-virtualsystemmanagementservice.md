---
description: Remove a máquina virtual definida anteriormente do escopo de gerenciamento do sistema host.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Método DestroySystem da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829367"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="4abd5-103">Método DestroySystem da \_ classe VirtualSystemManagementService Msvm</span><span class="sxs-lookup"><span data-stu-id="4abd5-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4abd5-104">Remove a máquina virtual definida anteriormente do escopo de gerenciamento do sistema host.</span><span class="sxs-lookup"><span data-stu-id="4abd5-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="4abd5-105">Todas as definições de recursos associadas também serão removidas.</span><span class="sxs-lookup"><span data-stu-id="4abd5-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="4abd5-106">A máquina virtual deve estar no estado desligado ou salvo antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="4abd5-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4abd5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4abd5-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4abd5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4abd5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abd5-109">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4abd5-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4abd5-110">Tipo: **\_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="4abd5-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="4abd5-111">Uma referência a uma instância do [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a instância de máquina virtual a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="4abd5-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="4abd5-112">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4abd5-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4abd5-113">Tipo: **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="4abd5-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="4abd5-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4abd5-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abd5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4abd5-115">Return value</span></span>

<span data-ttu-id="4abd5-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4abd5-116">Type: **uint32**</span></span>

<span data-ttu-id="4abd5-117">Se esse método for executado de forma síncrona, ele retornará 0 se tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="4abd5-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="4abd5-118">Se esse método for executado de forma assíncrona, ele retornará 4096 e o parâmetro de saída do *trabalho* poderá ser usado para acompanhar o progresso da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4abd5-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="4abd5-119">Qualquer outro valor de retorno indica um erro.</span><span class="sxs-lookup"><span data-stu-id="4abd5-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="4abd5-120">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="4abd5-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-121">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="4abd5-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-122">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="4abd5-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-123">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="4abd5-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-124">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="4abd5-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-125">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="4abd5-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4abd5-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-127">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="4abd5-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-128">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4abd5-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4abd5-129">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4abd5-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="4abd5-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4abd5-130">Remarks</span></span>

<span data-ttu-id="4abd5-131">O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="4abd5-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4abd5-132">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4abd5-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4abd5-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4abd5-133">Examples</span></span>

<span data-ttu-id="4abd5-134">O exemplo de C# a seguir usa o método **DestroySystem** para remover uma máquina virtual planejada.</span><span class="sxs-lookup"><span data-stu-id="4abd5-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="4abd5-135">Esse código é obtido do [exemplo de máquinas virtuais planejadas do Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="4abd5-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="4abd5-136">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="4abd5-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4abd5-137">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="4abd5-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="4abd5-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4abd5-138">Requirements</span></span>



| <span data-ttu-id="4abd5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4abd5-139">Requirement</span></span> | <span data-ttu-id="4abd5-140">Valor</span><span class="sxs-lookup"><span data-stu-id="4abd5-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abd5-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4abd5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4abd5-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4abd5-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4abd5-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4abd5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4abd5-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4abd5-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4abd5-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="4abd5-145">Namespace</span></span><br/>                | <span data-ttu-id="4abd5-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4abd5-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4abd5-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4abd5-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4abd5-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4abd5-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4abd5-149">DLL</span><span class="sxs-lookup"><span data-stu-id="4abd5-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4abd5-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4abd5-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4abd5-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="4abd5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abd5-152">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="4abd5-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

