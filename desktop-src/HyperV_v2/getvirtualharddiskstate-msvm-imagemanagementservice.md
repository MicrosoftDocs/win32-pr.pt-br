---
description: Recupera informações de estado para um arquivo de disco rígido virtual.
ms.assetid: 398b098b-dc1a-45e0-abcb-37b4b0a32290
title: Método GetVirtualHardDiskState da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e608078b88415eb683a95e3ba41d81b99014961d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759245"
---
# <a name="getvirtualharddiskstate-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="b9578-103">Método GetVirtualHardDiskState da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="b9578-103">GetVirtualHardDiskState method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="b9578-104">Recupera informações de estado para um arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="b9578-104">Retrieves state information for a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9578-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9578-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskState(
  [in]  string              Path,
  [out] string              State,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b9578-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9578-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9578-107">*Caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b9578-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9578-108">O caminho totalmente qualificado do arquivo de imagem de disco.</span><span class="sxs-lookup"><span data-stu-id="b9578-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="b9578-109">*Estado* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b9578-109">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9578-110">Se for bem-sucedido, o receberá uma instância inserida da classe [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md) que contém as informações de estado do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="b9578-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskState**](msvm-virtualharddiskstate.md) class that contains the state information for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="b9578-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="b9578-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9578-112">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9578-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9578-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b9578-113">Return value</span></span>

<span data-ttu-id="b9578-114">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9578-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b9578-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="b9578-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b9578-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="b9578-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b9578-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="b9578-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b9578-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="b9578-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b9578-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b9578-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="b9578-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b9578-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="b9578-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b9578-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b9578-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="b9578-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="b9578-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9578-129">Remarks</span></span>

<span data-ttu-id="b9578-130">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="b9578-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b9578-131">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="b9578-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b9578-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9578-132">Examples</span></span>

<span data-ttu-id="b9578-133">O exemplo de C# a seguir mostra como chamar o método **GetVirtualHardDiskState** .</span><span class="sxs-lookup"><span data-stu-id="b9578-133">The following C# example shows how to call the **GetVirtualHardDiskState** method.</span></span> <span data-ttu-id="b9578-134">Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="b9578-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskState(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskState");

    inParams["Path"] = vhdPath;
    
    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskState", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskState was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskState was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["State"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="b9578-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9578-135">Requirements</span></span>



| <span data-ttu-id="b9578-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9578-136">Requirement</span></span> | <span data-ttu-id="b9578-137">Valor</span><span class="sxs-lookup"><span data-stu-id="b9578-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9578-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9578-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b9578-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b9578-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9578-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9578-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b9578-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b9578-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9578-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9578-142">Namespace</span></span><br/>                | <span data-ttu-id="b9578-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b9578-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9578-144">MOF</span><span class="sxs-lookup"><span data-stu-id="b9578-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9578-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9578-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9578-146">DLL</span><span class="sxs-lookup"><span data-stu-id="b9578-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9578-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9578-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9578-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9578-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9578-149">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="b9578-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

