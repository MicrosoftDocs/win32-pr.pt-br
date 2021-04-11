---
description: Cria um instantâneo de uma máquina virtual.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Método createsnapshot da classe Msvm_VirtualSystemSnapshotService (DBDAOINT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296922"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="460f4-103">Método createsnapshot da classe Msvm \_ VirtualSystemSnapshotService</span><span class="sxs-lookup"><span data-stu-id="460f4-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="460f4-104">Cria um instantâneo de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="460f4-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="460f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="460f4-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="460f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="460f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="460f4-107">*AffectedSystem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="460f4-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460f4-108">Uma referência a uma classe de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual da qual criar um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="460f4-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="460f4-109">*SnapshotSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="460f4-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460f4-110">Uma cadeia de caracteres que contém uma instância inserida de uma classe de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que contém as configurações de parâmetro para o instantâneo.</span><span class="sxs-lookup"><span data-stu-id="460f4-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="460f4-111">Esse parâmetro é opcional e pode ser uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="460f4-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="460f4-112">*Instantâneotype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="460f4-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="460f4-113">Especifica o tipo de instantâneo solicitado.</span><span class="sxs-lookup"><span data-stu-id="460f4-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="460f4-114">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="460f4-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="460f4-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantâneo completo** (2)</span><span class="sxs-lookup"><span data-stu-id="460f4-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="460f4-116">Instantâneo completo da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="460f4-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="460f4-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Instantâneo do disco** (3)</span><span class="sxs-lookup"><span data-stu-id="460f4-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="460f4-118">Instantâneo de discos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="460f4-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="460f4-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="460f4-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="460f4-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="460f4-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="460f4-121">*ResultingSnapshot* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="460f4-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="460f4-122">Uma referência a um objeto [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa o instantâneo da máquina virtual resultante.</span><span class="sxs-lookup"><span data-stu-id="460f4-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="460f4-123">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="460f4-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="460f4-124">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="460f4-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="460f4-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="460f4-125">Return value</span></span>

<span data-ttu-id="460f4-126">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="460f4-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="460f4-127">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="460f4-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-128">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="460f4-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-129">**Falha** (2)</span><span class="sxs-lookup"><span data-stu-id="460f4-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-130">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="460f4-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-131">**Parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="460f4-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-132">**Estado inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="460f4-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-133">**Tipo inválido** (6)</span><span class="sxs-lookup"><span data-stu-id="460f4-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="460f4-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-135">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="460f4-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-136">**Método reservado** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="460f4-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="460f4-137">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="460f4-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="460f4-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="460f4-138">Examples</span></span>

<span data-ttu-id="460f4-139">O código de exemplo C# a seguir cria uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="460f4-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="460f4-140">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="460f4-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="460f4-141">Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="460f4-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="460f4-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="460f4-142">Requirements</span></span>



| <span data-ttu-id="460f4-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="460f4-143">Requirement</span></span> | <span data-ttu-id="460f4-144">Valor</span><span class="sxs-lookup"><span data-stu-id="460f4-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="460f4-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="460f4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="460f4-146">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="460f4-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="460f4-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="460f4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="460f4-148">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="460f4-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="460f4-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="460f4-149">Namespace</span></span><br/>                | <span data-ttu-id="460f4-150">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="460f4-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="460f4-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="460f4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="460f4-152"><dt>DBDAOINT. h</dt></span><span class="sxs-lookup"><span data-stu-id="460f4-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="460f4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="460f4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="460f4-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="460f4-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="460f4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="460f4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="460f4-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="460f4-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="460f4-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="460f4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="460f4-158">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="460f4-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="460f4-159">**CreateVirtualSystemSnapshot (v1)**</span><span class="sxs-lookup"><span data-stu-id="460f4-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

