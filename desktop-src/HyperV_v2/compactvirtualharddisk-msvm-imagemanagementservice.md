---
description: Compacta um arquivo de disco rígido virtual.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Método CompactVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770223"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="fc12f-103">Método CompactVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="fc12f-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="fc12f-104">Compacta um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="fc12f-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="fc12f-105">A compactação é o processo de liberação de partes não usadas do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="fc12f-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="fc12f-106">O disco rígido virtual não é montado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fc12f-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="fc12f-107">Consulte comentários para restrições de uso para este método.</span><span class="sxs-lookup"><span data-stu-id="fc12f-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc12f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc12f-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fc12f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc12f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc12f-110">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="fc12f-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12f-111">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fc12f-111">Type: **string**</span></span>

<span data-ttu-id="fc12f-112">Um caminho totalmente qualificado que especifica o local do arquivo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="fc12f-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="fc12f-113">*Modo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc12f-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12f-114">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fc12f-114">Type: **uint16**</span></span>

<span data-ttu-id="fc12f-115">Especifica o modo para a operação de compactação.</span><span class="sxs-lookup"><span data-stu-id="fc12f-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="fc12f-116">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc12f-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="fc12f-117">**Completo** (0)</span><span class="sxs-lookup"><span data-stu-id="fc12f-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="fc12f-118">**Rápido** (1)</span><span class="sxs-lookup"><span data-stu-id="fc12f-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="fc12f-119">**Recortar** (2)</span><span class="sxs-lookup"><span data-stu-id="fc12f-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="fc12f-120">**Preaparado** (3)</span><span class="sxs-lookup"><span data-stu-id="fc12f-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="fc12f-121">**Prezerado** (4)</span><span class="sxs-lookup"><span data-stu-id="fc12f-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="fc12f-122">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="fc12f-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12f-123">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="fc12f-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="fc12f-124">Uma referência ao trabalho (pode ser **NULL** se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="fc12f-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc12f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc12f-125">Return value</span></span>

<span data-ttu-id="fc12f-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fc12f-126">Type: **uint32**</span></span>

<span data-ttu-id="fc12f-127">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc12f-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fc12f-128">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="fc12f-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-129">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="fc12f-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-130">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="fc12f-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-131">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="fc12f-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-132">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="fc12f-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-133">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="fc12f-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-134">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="fc12f-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-135">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="fc12f-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-136">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="fc12f-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-137">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="fc12f-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-138">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="fc12f-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-139">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="fc12f-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-140">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="fc12f-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fc12f-141">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="fc12f-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fc12f-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc12f-142">Remarks</span></span>

<span data-ttu-id="fc12f-143">Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:</span><span class="sxs-lookup"><span data-stu-id="fc12f-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="fc12f-144">VHDX fixo</span><span class="sxs-lookup"><span data-stu-id="fc12f-144">Fixed VHDX</span></span>
-   <span data-ttu-id="fc12f-145">VHD dinâmico</span><span class="sxs-lookup"><span data-stu-id="fc12f-145">Dynamic VHD</span></span>
-   <span data-ttu-id="fc12f-146">VHDX dinâmico</span><span class="sxs-lookup"><span data-stu-id="fc12f-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="fc12f-147">VHD diferencial</span><span class="sxs-lookup"><span data-stu-id="fc12f-147">Differencing VHD</span></span>
-   <span data-ttu-id="fc12f-148">VHDX diferencial</span><span class="sxs-lookup"><span data-stu-id="fc12f-148">Differencing VHDX</span></span>

<span data-ttu-id="fc12f-149">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="fc12f-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="fc12f-150">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="fc12f-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="fc12f-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fc12f-151">Examples</span></span>

<span data-ttu-id="fc12f-152">O exemplo C# a seguir compacta um disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="fc12f-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="fc12f-153">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="fc12f-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="fc12f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc12f-154">Requirements</span></span>



| <span data-ttu-id="fc12f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc12f-155">Requirement</span></span> | <span data-ttu-id="fc12f-156">Valor</span><span class="sxs-lookup"><span data-stu-id="fc12f-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc12f-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc12f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="fc12f-158">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fc12f-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fc12f-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc12f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="fc12f-160">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fc12f-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc12f-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc12f-161">Namespace</span></span><br/>                | <span data-ttu-id="fc12f-162">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fc12f-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fc12f-163">MOF</span><span class="sxs-lookup"><span data-stu-id="fc12f-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc12f-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc12f-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc12f-165">DLL</span><span class="sxs-lookup"><span data-stu-id="fc12f-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc12f-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fc12f-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fc12f-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc12f-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc12f-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fc12f-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fc12f-169">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="fc12f-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

