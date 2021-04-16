---
description: Determina se um arquivo de disco rígido virtual é válido.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Método ValidateVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750834"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0b29a-103">Método ValidateVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="0b29a-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0b29a-104">Determina se um arquivo de disco rígido virtual é válido.</span><span class="sxs-lookup"><span data-stu-id="0b29a-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b29a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b29a-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0b29a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b29a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b29a-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0b29a-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b29a-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0b29a-108">Type: **string**</span></span>

<span data-ttu-id="0b29a-109">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="0b29a-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="0b29a-110">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="0b29a-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b29a-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0b29a-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="0b29a-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b29a-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b29a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0b29a-113">Return value</span></span>

<span data-ttu-id="0b29a-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0b29a-114">Type: **uint32**</span></span>

<span data-ttu-id="0b29a-115">Esse método pode retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b29a-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0b29a-116">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="0b29a-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-117">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0b29a-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-118">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="0b29a-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-119">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0b29a-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-120">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="0b29a-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-121">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0b29a-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-122">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="0b29a-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-123">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0b29a-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-124">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0b29a-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-125">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="0b29a-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-126">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0b29a-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-127">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="0b29a-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-128">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0b29a-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-129">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="0b29a-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0b29a-130">**Ciclo de cadeia diferencial VHD detectado** (32787)</span><span class="sxs-lookup"><span data-stu-id="0b29a-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0b29a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b29a-131">Remarks</span></span>

<span data-ttu-id="0b29a-132">Se o disco rígido virtual for um disco diferencial, toda a cadeia de discos virtuais será aberta.</span><span class="sxs-lookup"><span data-stu-id="0b29a-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="0b29a-133">Se o link for quebrado na cadeia de discos, um objeto de trabalho será retornado com o erro apropriado inicializado e as propriedades Child e Parent serão inicializadas para o local onde o link está quebrado.</span><span class="sxs-lookup"><span data-stu-id="0b29a-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="0b29a-134">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="0b29a-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0b29a-135">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0b29a-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0b29a-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b29a-136">Examples</span></span>

<span data-ttu-id="0b29a-137">O exemplo C# a seguir valida uma imagem de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="0b29a-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="0b29a-138">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0b29a-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="0b29a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b29a-139">Requirements</span></span>



| <span data-ttu-id="0b29a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b29a-140">Requirement</span></span> | <span data-ttu-id="0b29a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="0b29a-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b29a-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b29a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0b29a-143">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0b29a-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b29a-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b29a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0b29a-145">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0b29a-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b29a-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="0b29a-146">Namespace</span></span><br/>                | <span data-ttu-id="0b29a-147">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0b29a-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b29a-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0b29a-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b29a-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b29a-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b29a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0b29a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b29a-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b29a-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b29a-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b29a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b29a-153">**ValidateVirtualHardDisk (v1)**</span><span class="sxs-lookup"><span data-stu-id="0b29a-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="0b29a-154">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0b29a-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0b29a-155">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="0b29a-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

