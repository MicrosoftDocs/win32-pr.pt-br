---
description: Mescla um disco rígido virtual filho em uma cadeia diferencial com um ou mais discos rígidos virtuais pai na cadeia.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Método MergeVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506064"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="79507-103">Método MergeVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="79507-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="79507-104">Mescla um disco rígido virtual filho em uma cadeia diferencial com um ou mais discos rígidos virtuais pai na cadeia.</span><span class="sxs-lookup"><span data-stu-id="79507-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="79507-105">Consulte comentários para restrições de uso para este método.</span><span class="sxs-lookup"><span data-stu-id="79507-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="79507-106">Se o usuário que está executando essa função não tiver permissão para atualizar as máquinas virtuais, essa função falhará.</span><span class="sxs-lookup"><span data-stu-id="79507-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="79507-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79507-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="79507-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79507-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79507-109">*SourcePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79507-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79507-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79507-110">Type: **string**</span></span>

<span data-ttu-id="79507-111">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual a ser mesclado.</span><span class="sxs-lookup"><span data-stu-id="79507-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="79507-112">*DestinationPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79507-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79507-113">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="79507-113">Type: **string**</span></span>

<span data-ttu-id="79507-114">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual pai no qual os dados serão mesclados.</span><span class="sxs-lookup"><span data-stu-id="79507-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="79507-115">Esse pode ser o disco rígido virtual do pai imediato do arquivo de mesclagem ou a imagem do disco pai alguns níveis acima da cadeia diferencial.</span><span class="sxs-lookup"><span data-stu-id="79507-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="79507-116">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="79507-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79507-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="79507-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="79507-118">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="79507-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79507-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79507-119">Return value</span></span>

<span data-ttu-id="79507-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="79507-120">Type: **uint32**</span></span>

<span data-ttu-id="79507-121">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="79507-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="79507-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="79507-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79507-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="79507-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="79507-124">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="79507-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="79507-125">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="79507-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="79507-126">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="79507-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="79507-127">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="79507-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="79507-128">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="79507-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="79507-129">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="79507-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="79507-130">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="79507-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="79507-131">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="79507-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="79507-132">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="79507-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="79507-133">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="79507-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="79507-134">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="79507-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="79507-135">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="79507-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="79507-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="79507-136">Remarks</span></span>

<span data-ttu-id="79507-137">O disco rígido virtual filho deve estar offline.</span><span class="sxs-lookup"><span data-stu-id="79507-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="79507-138">Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:</span><span class="sxs-lookup"><span data-stu-id="79507-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="79507-139">VHD diferencial</span><span class="sxs-lookup"><span data-stu-id="79507-139">Differencing VHD</span></span>
-   <span data-ttu-id="79507-140">VHDX diferencial</span><span class="sxs-lookup"><span data-stu-id="79507-140">Differencing VHDX</span></span>

<span data-ttu-id="79507-141">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="79507-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="79507-142">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="79507-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="79507-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="79507-143">Examples</span></span>

<span data-ttu-id="79507-144">O exemplo C# a seguir expande um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="79507-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="79507-145">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="79507-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="79507-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79507-146">Requirements</span></span>



| <span data-ttu-id="79507-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="79507-147">Requirement</span></span> | <span data-ttu-id="79507-148">Valor</span><span class="sxs-lookup"><span data-stu-id="79507-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79507-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79507-149">Minimum supported client</span></span><br/> | <span data-ttu-id="79507-150">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="79507-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="79507-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79507-151">Minimum supported server</span></span><br/> | <span data-ttu-id="79507-152">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79507-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79507-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="79507-153">Namespace</span></span><br/>                | <span data-ttu-id="79507-154">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="79507-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="79507-155">MOF</span><span class="sxs-lookup"><span data-stu-id="79507-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79507-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="79507-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79507-157">DLL</span><span class="sxs-lookup"><span data-stu-id="79507-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79507-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79507-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79507-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="79507-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="79507-160">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="79507-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="79507-161">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="79507-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

