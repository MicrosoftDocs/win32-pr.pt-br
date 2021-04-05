---
title: Método ProvisioningPrepJob da classe Win32_RDMSVirtualDesktopCollection
description: Cria um trabalho de provisionamento de área de trabalho virtual.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningPrepJob
- Método ProvisioningPrepJob Serviços de Área de Trabalho Remota, interface Win32_RDMSVirtualDesktopCollection
- Serviços de Área de Trabalho Remota de interface Win32_RDMSVirtualDesktopCollection, método ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918364"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="df9bf-106">Método ProvisioningPrepJob da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="df9bf-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="df9bf-107">Cria um trabalho de provisionamento de área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="df9bf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df9bf-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="df9bf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df9bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df9bf-110">*CollectionAlias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-111">O alias da coleção que hospeda a área de trabalho virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-112">*VMHostName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-113">O nome do host da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-114">*VMName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-115">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-116">*ExportToLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-117">O caminho completo o local para exportar o trabalho de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="df9bf-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-118">*bSysPrep* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-119">Indica se o trabalho de provisionamento representa uma implantação do Sysprep.</span><span class="sxs-lookup"><span data-stu-id="df9bf-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-120">*MachineName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-121">O nome do computador que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-122">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-123">O nome de usuário do administrador da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-124">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-125">A senha do administrador da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="df9bf-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="df9bf-126">*JobGuid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="df9bf-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df9bf-127">O **GUID** que identifica exclusivamente o trabalho de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="df9bf-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df9bf-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="df9bf-128">Return value</span></span>

<span data-ttu-id="df9bf-129">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="df9bf-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="df9bf-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df9bf-130">Requirements</span></span>



| <span data-ttu-id="df9bf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="df9bf-131">Requirement</span></span> | <span data-ttu-id="df9bf-132">Valor</span><span class="sxs-lookup"><span data-stu-id="df9bf-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="df9bf-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df9bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="df9bf-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="df9bf-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="df9bf-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="df9bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="df9bf-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df9bf-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="df9bf-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="df9bf-137">Namespace</span></span><br/>                | <span data-ttu-id="df9bf-138">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="df9bf-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="df9bf-139">MOF</span><span class="sxs-lookup"><span data-stu-id="df9bf-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df9bf-140"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df9bf-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="df9bf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="df9bf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df9bf-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df9bf-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="df9bf-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="df9bf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df9bf-144">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="df9bf-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





