---
description: Copia arquivos do host Hyper-V para a máquina virtual.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Método Msvm_GuestFileService:: CopyFilesToGuest'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783304"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="671e5-103">\_Método Msvm GuestFileService:: CopyFilesToGuest</span><span class="sxs-lookup"><span data-stu-id="671e5-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="671e5-104">Copia arquivos do host Hyper-V para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="671e5-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="671e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="671e5-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="671e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="671e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671e5-107">*CopyFileToGuestSettings* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="671e5-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671e5-108">Uma matriz de instâncias da classe [**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) que representa um trabalho de operação de serviço de arquivo convidado.</span><span class="sxs-lookup"><span data-stu-id="671e5-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="671e5-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="671e5-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="671e5-110">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="671e5-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="671e5-111">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="671e5-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="671e5-112">Esse parâmetro foi adicionado no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="671e5-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="671e5-113">*ParentPools* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="671e5-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="671e5-114">Uma matriz opcional de referências do [**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) que são usadas para monitorar o progresso da operação.</span><span class="sxs-lookup"><span data-stu-id="671e5-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="671e5-115">**CopyFilesToGuest** usará *ParentPools* se não puder ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="671e5-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="671e5-116">Se a operação for executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="671e5-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="671e5-117">Esse parâmetro foi removido no Windows 10.</span><span class="sxs-lookup"><span data-stu-id="671e5-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671e5-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="671e5-118">Return value</span></span>

<span data-ttu-id="671e5-119">Em caso de sucesso, retorna 0; caso contrário, retorna um valor de erro.</span><span class="sxs-lookup"><span data-stu-id="671e5-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="671e5-120">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="671e5-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-121">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="671e5-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-122">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="671e5-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-123">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="671e5-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-124">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="671e5-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-125">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="671e5-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-126">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="671e5-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-127">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="671e5-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-128">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="671e5-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-129">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="671e5-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-130">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="671e5-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-131">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="671e5-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="671e5-132">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="671e5-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="671e5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671e5-133">Requirements</span></span>



| <span data-ttu-id="671e5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="671e5-134">Requirement</span></span> | <span data-ttu-id="671e5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="671e5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671e5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671e5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="671e5-137">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="671e5-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="671e5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671e5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="671e5-139">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="671e5-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="671e5-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="671e5-140">Namespace</span></span><br/>                | <span data-ttu-id="671e5-141">\\\\\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="671e5-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="671e5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="671e5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="671e5-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="671e5-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="671e5-144">DLL</span><span class="sxs-lookup"><span data-stu-id="671e5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="671e5-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="671e5-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="671e5-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="671e5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671e5-147">**Msvm \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="671e5-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 




