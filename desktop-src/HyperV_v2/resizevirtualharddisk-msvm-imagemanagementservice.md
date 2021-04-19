---
description: Redimensiona um disco rígido virtual existente.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Método ResizeVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768744"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="f559a-103">Método ResizeVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="f559a-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="f559a-104">Redimensiona um disco rígido virtual existente.</span><span class="sxs-lookup"><span data-stu-id="f559a-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="f559a-105">O disco rígido virtual deve estar offline.</span><span class="sxs-lookup"><span data-stu-id="f559a-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="f559a-106">Consulte comentários para restrições de uso para este método.</span><span class="sxs-lookup"><span data-stu-id="f559a-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f559a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f559a-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f559a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f559a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f559a-109">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="f559a-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f559a-110">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f559a-110">Type: **string**</span></span>

<span data-ttu-id="f559a-111">O caminho totalmente qualificado do arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="f559a-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="f559a-112">*MaxInternalSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f559a-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f559a-113">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f559a-113">Type: **uint64**</span></span>

<span data-ttu-id="f559a-114">O tamanho máximo do disco rígido virtual como visível pela máquina virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f559a-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="f559a-115">*MaxInternalSize* valor mínimo é *disks* + 512-(*diskize* mod 512).</span><span class="sxs-lookup"><span data-stu-id="f559a-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="f559a-116">*Disks* é o tamanho do arquivo de disco rígido virtual, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f559a-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="f559a-117">O erro InvalidParameter (32773) será retornado se o valor de *MaxInternalSize* especificado for menor que o valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="f559a-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="f559a-118">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="f559a-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f559a-119">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f559a-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="f559a-120">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f559a-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f559a-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f559a-121">Return value</span></span>

<span data-ttu-id="f559a-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f559a-122">Type: **uint32**</span></span>

<span data-ttu-id="f559a-123">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f559a-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f559a-124">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="f559a-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-125">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f559a-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-126">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="f559a-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-127">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f559a-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-128">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="f559a-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-129">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f559a-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-130">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="f559a-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-131">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f559a-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-132">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f559a-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-133">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="f559a-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-134">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f559a-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-135">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="f559a-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-136">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f559a-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f559a-137">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="f559a-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f559a-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="f559a-138">Remarks</span></span>

<span data-ttu-id="f559a-139">Somente os seguintes tipos de discos rígidos virtuais podem ser usados com esse método quando o tamanho do disco rígido virtual está sendo aumentado:</span><span class="sxs-lookup"><span data-stu-id="f559a-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="f559a-140">VHD fixo</span><span class="sxs-lookup"><span data-stu-id="f559a-140">Fixed VHD</span></span>
-   <span data-ttu-id="f559a-141">VHDX fixo</span><span class="sxs-lookup"><span data-stu-id="f559a-141">Fixed VHDX</span></span>
-   <span data-ttu-id="f559a-142">VHD dinâmico</span><span class="sxs-lookup"><span data-stu-id="f559a-142">Dynamic VHD</span></span>
-   <span data-ttu-id="f559a-143">VHDX dinâmico</span><span class="sxs-lookup"><span data-stu-id="f559a-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="f559a-144">VHDX diferencial</span><span class="sxs-lookup"><span data-stu-id="f559a-144">Differencing VHDX</span></span>

<span data-ttu-id="f559a-145">Somente os seguintes tipos de discos rígidos virtuais podem ser usados com esse método quando o tamanho do disco rígido virtual está sendo reduzido:</span><span class="sxs-lookup"><span data-stu-id="f559a-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="f559a-146">VHDX fixo</span><span class="sxs-lookup"><span data-stu-id="f559a-146">Fixed VHDX</span></span>
-   <span data-ttu-id="f559a-147">VHDX dinâmico</span><span class="sxs-lookup"><span data-stu-id="f559a-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="f559a-148">VHDX diferencial</span><span class="sxs-lookup"><span data-stu-id="f559a-148">Differencing VHDX</span></span>

<span data-ttu-id="f559a-149">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="f559a-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f559a-150">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f559a-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="f559a-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f559a-151">Examples</span></span>

<span data-ttu-id="f559a-152">O exemplo C# a seguir expande um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="f559a-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="f559a-153">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="f559a-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="f559a-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f559a-154">Requirements</span></span>



| <span data-ttu-id="f559a-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="f559a-155">Requirement</span></span> | <span data-ttu-id="f559a-156">Valor</span><span class="sxs-lookup"><span data-stu-id="f559a-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f559a-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f559a-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f559a-158">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f559a-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f559a-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f559a-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f559a-160">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f559a-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f559a-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="f559a-161">Namespace</span></span><br/>                | <span data-ttu-id="f559a-162">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f559a-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f559a-163">MOF</span><span class="sxs-lookup"><span data-stu-id="f559a-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f559a-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f559a-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f559a-165">DLL</span><span class="sxs-lookup"><span data-stu-id="f559a-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f559a-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f559a-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f559a-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="f559a-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="f559a-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f559a-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f559a-169">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="f559a-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

