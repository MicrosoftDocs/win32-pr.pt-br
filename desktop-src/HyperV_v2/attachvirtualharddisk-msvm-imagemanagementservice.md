---
description: Anexa um arquivo de disco rígido virtual no modo de loopback.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Método AttachVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828440"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="d1847-103">Método AttachVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="d1847-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="d1847-104">Anexa um arquivo de disco rígido virtual no modo de loopback.</span><span class="sxs-lookup"><span data-stu-id="d1847-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1847-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1847-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d1847-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1847-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1847-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d1847-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1847-108">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="d1847-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="d1847-109">*AssignDriveLetter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1847-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1847-110">Indica se as letras da unidade são atribuídas aos volumes do disco.</span><span class="sxs-lookup"><span data-stu-id="d1847-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="d1847-111">*Somente leitura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1847-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1847-112">Indica se o disco rígido anexado deve ser somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d1847-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="d1847-113">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="d1847-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1847-114">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d1847-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1847-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1847-115">Return value</span></span>

<span data-ttu-id="d1847-116">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d1847-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d1847-117">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="d1847-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-118">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d1847-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-119">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="d1847-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-120">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d1847-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-121">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="d1847-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-122">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d1847-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-123">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="d1847-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-124">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d1847-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-125">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d1847-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-126">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="d1847-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-127">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d1847-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-128">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="d1847-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-129">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d1847-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d1847-130">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="d1847-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d1847-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1847-131">Remarks</span></span>

<span data-ttu-id="d1847-132">Para desanexar o disco rígido virtual, use o método [**Msvm \_ MountedStorageImage. DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) .</span><span class="sxs-lookup"><span data-stu-id="d1847-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="d1847-133">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="d1847-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d1847-134">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d1847-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d1847-135">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1847-135">Examples</span></span>

<span data-ttu-id="d1847-136">O exemplo de C# a seguir mostra como anexar um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="d1847-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="d1847-137">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d1847-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="d1847-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1847-138">Requirements</span></span>



| <span data-ttu-id="d1847-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1847-139">Requirement</span></span> | <span data-ttu-id="d1847-140">Valor</span><span class="sxs-lookup"><span data-stu-id="d1847-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1847-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1847-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d1847-142">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d1847-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1847-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1847-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d1847-144">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d1847-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1847-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1847-145">Namespace</span></span><br/>                | <span data-ttu-id="d1847-146">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d1847-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d1847-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d1847-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1847-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1847-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1847-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d1847-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1847-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1847-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1847-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1847-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1847-152">**Msvm \_ MountedStorageImage. DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d1847-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="d1847-153">**Montagem (v1)**</span><span class="sxs-lookup"><span data-stu-id="d1847-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="d1847-154">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="d1847-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

