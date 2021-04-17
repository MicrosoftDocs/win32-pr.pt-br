---
title: Método GetProvisioningProperties da classe Win32_RDMSCollectionProperties
description: Recupera as propriedades de provisionamento da coleção de áreas de trabalho virtuais.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetProvisioningProperties
- Método GetProvisioningProperties Serviços de Área de Trabalho Remota, classe Win32_RDMSCollectionProperties
- Classe Win32_RDMSCollectionProperties Serviços de Área de Trabalho Remota, método GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759945"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="8fbc0-106">Método GetProvisioningProperties da classe Win32 \_ RDMSCollectionProperties</span><span class="sxs-lookup"><span data-stu-id="8fbc0-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="8fbc0-107">Recupera as propriedades de provisionamento da coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbc0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fbc0-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="8fbc0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fbc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbc0-110">*PoolVhdType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-111">Especifica o formato do VHD (disco rígido virtual) do pool de máquinas virtuais na coleção.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="8fbc0-112">Clone</span><span class="sxs-lookup"><span data-stu-id="8fbc0-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-113">Um VHD clonado.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-114">DiffDisk</span><span class="sxs-lookup"><span data-stu-id="8fbc0-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-115">Um VHD diferencial.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8fbc0-116">*MasterVmLocation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-117">Recebe o caminho para a imagem da VM mestre.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-118">*NamePrefix* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-119">Recebe o prefixo de nome a ser anexado ao início dos nomes de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-120">*NameStartIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-121">Índice de início.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-122">*LocalVmLocation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-123">Recebe o caminho local para as máquinas virtuais nos servidores Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="8fbc0-124">Se esse parâmetro for definido como **nulo** ou estiver vazio, o diretório de máquina virtual padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-125">*LocalGoldVmLocation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-126">Recebe o caminho local para a imagem de VHD dourado quando o parâmetro *PoolVhdTpe* é definido como "DiffDisk".</span><span class="sxs-lookup"><span data-stu-id="8fbc0-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="8fbc0-127">Se esse parâmetro for definido como **nulo** ou estiver vazio, o diretório de máquina virtual padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-128">*RunFromSMB* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-129">Recebe um valor que indica se a coleção deve ser executada de um compartilhamento SMB (Server Message Block).</span><span class="sxs-lookup"><span data-stu-id="8fbc0-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="8fbc0-130">**True** para executar as máquinas virtuais de um compartilhamento SBM; , **Falso**.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-131">*SMBLocation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-132">Recebe o caminho para o compartilhamento SMB se o compartilhamento SMB estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-133">*SMBStreaming* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-134">Recebe um valor que indica se o streaming SMB está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="8fbc0-135">**True** se o compartilhamento SMB estiver habilitado; , **Falso**.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-136">*VmDomain* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-137">Recebe o nome de domínio das máquinas virtuais na coleção.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-138">*VmOU* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-139">Recebe a UO (unidade organizacional) Active Directory das máquinas virtuais na coleção.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="8fbc0-140">*ProductKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8fbc0-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbc0-141">Recebe as chaves de produto do sistema operacional para as máquinas virtuais na coleção.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbc0-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fbc0-142">Return value</span></span>

<span data-ttu-id="8fbc0-143">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="8fbc0-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbc0-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fbc0-144">Requirements</span></span>



| <span data-ttu-id="8fbc0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fbc0-145">Requirement</span></span> | <span data-ttu-id="8fbc0-146">Valor</span><span class="sxs-lookup"><span data-stu-id="8fbc0-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbc0-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fbc0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbc0-148">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8fbc0-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8fbc0-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fbc0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbc0-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fbc0-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8fbc0-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="8fbc0-151">Namespace</span></span><br/>                | <span data-ttu-id="8fbc0-152">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="8fbc0-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8fbc0-153">MOF</span><span class="sxs-lookup"><span data-stu-id="8fbc0-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fbc0-154"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fbc0-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fbc0-155">DLL</span><span class="sxs-lookup"><span data-stu-id="8fbc0-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fbc0-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbc0-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8fbc0-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fbc0-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbc0-158">**\_RDMSCollectionProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="8fbc0-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





