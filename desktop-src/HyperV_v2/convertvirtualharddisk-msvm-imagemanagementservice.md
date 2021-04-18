---
description: Converte um disco rígido virtual existente em um tipo ou formato diferente.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Método ConvertVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810358"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="f8601-103">Método ConvertVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="f8601-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="f8601-104">Converte um disco rígido virtual existente em um tipo ou formato diferente.</span><span class="sxs-lookup"><span data-stu-id="f8601-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="f8601-105">Esse método cria um novo disco rígido virtual e não converte o disco rígido virtual de origem em vigor.</span><span class="sxs-lookup"><span data-stu-id="f8601-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="f8601-106">Consulte comentários para restrições de uso para este método.</span><span class="sxs-lookup"><span data-stu-id="f8601-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8601-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8601-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f8601-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8601-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8601-109">*SourcePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8601-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8601-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f8601-110">Type: **string**</span></span>

<span data-ttu-id="f8601-111">O caminho totalmente qualificado do arquivo de disco rígido virtual de origem a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="f8601-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="f8601-112">Este arquivo não será modificado como resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="f8601-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="f8601-113">*VirtualDiskSettingData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f8601-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8601-114">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f8601-114">Type: **string**</span></span>

<span data-ttu-id="f8601-115">Uma representação de cadeia de caracteres da classe [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) que especifica os atributos do novo disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="f8601-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="f8601-116">As propriedades **Path**, **Type**, **Format**, **ParentPath**, **BlockSize** e **LogicalSectorSize** devem ser definidas.</span><span class="sxs-lookup"><span data-stu-id="f8601-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="f8601-117">A propriedade **ParentPath** pode ser **nula** se não for necessária.</span><span class="sxs-lookup"><span data-stu-id="f8601-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="f8601-118">Defina as propriedades **BlockSize** e **LogicalSectorSize** como 0 para usar os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="f8601-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="f8601-119">Para especificar o formato (VHD ou VHDX) do novo disco rígido virtual, defina a extensão do **caminho** para o valor apropriado (". vhd" ou ". VHDX").</span><span class="sxs-lookup"><span data-stu-id="f8601-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="f8601-120">A propriedade **Format** deve corresponder à extensão de nome de arquivo no **caminho**.</span><span class="sxs-lookup"><span data-stu-id="f8601-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="f8601-121">A propriedade **LogicalSectorSize** será ignorada.</span><span class="sxs-lookup"><span data-stu-id="f8601-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f8601-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f8601-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8601-123">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f8601-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="f8601-124">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f8601-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8601-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f8601-125">Return value</span></span>

<span data-ttu-id="f8601-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8601-126">Type: **uint32**</span></span>

<span data-ttu-id="f8601-127">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8601-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f8601-128">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f8601-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-129">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f8601-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-130">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f8601-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-131">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f8601-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-132">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f8601-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-133">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f8601-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-134">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f8601-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-135">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f8601-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-136">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f8601-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-137">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f8601-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-138">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f8601-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-139">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f8601-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-140">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f8601-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f8601-141">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="f8601-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f8601-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8601-142">Remarks</span></span>

<span data-ttu-id="f8601-143">Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:</span><span class="sxs-lookup"><span data-stu-id="f8601-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="f8601-144">VHD fixo</span><span class="sxs-lookup"><span data-stu-id="f8601-144">Fixed VHD</span></span>
-   <span data-ttu-id="f8601-145">VHDX fixo</span><span class="sxs-lookup"><span data-stu-id="f8601-145">Fixed VHDX</span></span>
-   <span data-ttu-id="f8601-146">VHD dinâmico</span><span class="sxs-lookup"><span data-stu-id="f8601-146">Dynamic VHD</span></span>
-   <span data-ttu-id="f8601-147">VHDX dinâmico</span><span class="sxs-lookup"><span data-stu-id="f8601-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="f8601-148">VHD diferencial</span><span class="sxs-lookup"><span data-stu-id="f8601-148">Differencing VHD</span></span>
-   <span data-ttu-id="f8601-149">VHDX diferencial</span><span class="sxs-lookup"><span data-stu-id="f8601-149">Differencing VHDX</span></span>

<span data-ttu-id="f8601-150">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="f8601-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f8601-151">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f8601-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f8601-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f8601-152">Examples</span></span>

<span data-ttu-id="f8601-153">O exemplo C# a seguir converte um disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="f8601-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="f8601-154">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f8601-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="f8601-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8601-155">Requirements</span></span>



| <span data-ttu-id="f8601-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8601-156">Requirement</span></span> | <span data-ttu-id="f8601-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f8601-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8601-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8601-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f8601-159">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f8601-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f8601-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8601-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f8601-161">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f8601-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8601-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="f8601-162">Namespace</span></span><br/>                | <span data-ttu-id="f8601-163">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f8601-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f8601-164">MOF</span><span class="sxs-lookup"><span data-stu-id="f8601-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8601-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8601-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8601-166">DLL</span><span class="sxs-lookup"><span data-stu-id="f8601-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8601-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f8601-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f8601-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="f8601-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8601-169">**ConvertVirtualHardDisk (v1)**</span><span class="sxs-lookup"><span data-stu-id="f8601-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="f8601-170">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f8601-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f8601-171">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="f8601-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

