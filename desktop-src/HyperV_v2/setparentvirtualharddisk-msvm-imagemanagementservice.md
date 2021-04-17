---
description: Atualiza o pai para os arquivos de disco rígido virtual de folha e filho especificados.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Método SetParentVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782802"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="82e6d-103">Método SetParentVirtualHardDisk da \_ classe imagens Msvm</span><span class="sxs-lookup"><span data-stu-id="82e6d-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="82e6d-104">Atualiza o pai para os arquivos de disco rígido virtual de folha e filho especificados.</span><span class="sxs-lookup"><span data-stu-id="82e6d-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="82e6d-105">Consulte comentários para restrições de uso para este método.</span><span class="sxs-lookup"><span data-stu-id="82e6d-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e6d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82e6d-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="82e6d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82e6d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e6d-108">*ChildPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82e6d-109">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual filho.</span><span class="sxs-lookup"><span data-stu-id="82e6d-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="82e6d-110">*ParentPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82e6d-111">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual pai.</span><span class="sxs-lookup"><span data-stu-id="82e6d-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="82e6d-112">*LeafPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82e6d-113">Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual de folha.</span><span class="sxs-lookup"><span data-stu-id="82e6d-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="82e6d-114">O parâmetro poderá ser **nulo** se o disco rígido virtual estiver offline, mas deverá ser especificado se o disco rígido virtual estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="82e6d-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="82e6d-115">*IgnoreIDMismatch* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82e6d-116">Indica se o pai deve ser forçado a definir quando os identificadores de disco virtual não correspondem.</span><span class="sxs-lookup"><span data-stu-id="82e6d-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="82e6d-117">Esse parâmetro deve ser usado com cautela porque se o novo disco rígido virtual pai não for idêntico ao pai original, poderá ocorrer corrupção de dados.</span><span class="sxs-lookup"><span data-stu-id="82e6d-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="82e6d-118">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82e6d-119">Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="82e6d-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e6d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82e6d-120">Return value</span></span>

<span data-ttu-id="82e6d-121">Esse método retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="82e6d-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="82e6d-122">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="82e6d-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-123">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="82e6d-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-124">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="82e6d-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-125">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="82e6d-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-126">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="82e6d-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-127">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="82e6d-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-128">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="82e6d-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-129">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="82e6d-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-130">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="82e6d-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-131">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="82e6d-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-132">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="82e6d-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-133">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="82e6d-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-134">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="82e6d-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="82e6d-135">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="82e6d-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="82e6d-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="82e6d-136">Remarks</span></span>

<span data-ttu-id="82e6d-137">Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:</span><span class="sxs-lookup"><span data-stu-id="82e6d-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="82e6d-138">VHD diferencial</span><span class="sxs-lookup"><span data-stu-id="82e6d-138">Differencing VHD</span></span>
-   <span data-ttu-id="82e6d-139">VHDX diferencial</span><span class="sxs-lookup"><span data-stu-id="82e6d-139">Differencing VHDX</span></span>

<span data-ttu-id="82e6d-140">O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="82e6d-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="82e6d-141">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="82e6d-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="82e6d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82e6d-142">Requirements</span></span>



| <span data-ttu-id="82e6d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="82e6d-143">Requirement</span></span> | <span data-ttu-id="82e6d-144">Valor</span><span class="sxs-lookup"><span data-stu-id="82e6d-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e6d-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82e6d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="82e6d-146">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="82e6d-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82e6d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="82e6d-148">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="82e6d-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="82e6d-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="82e6d-149">Namespace</span></span><br/>                | <span data-ttu-id="82e6d-150">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="82e6d-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="82e6d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="82e6d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82e6d-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82e6d-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82e6d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="82e6d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82e6d-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82e6d-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82e6d-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="82e6d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e6d-156">**Msvm \_ imagens**</span><span class="sxs-lookup"><span data-stu-id="82e6d-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

