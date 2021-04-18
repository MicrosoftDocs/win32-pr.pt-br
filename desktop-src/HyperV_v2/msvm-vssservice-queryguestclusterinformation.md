---
description: Consultando informações de cluster do host Hyper-V para o convidado.
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Método QueryGuestClusterInformation da classe Msvm_VssService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501364"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="291d1-103">Método QueryGuestClusterInformation da \_ classe VssService Msvm</span><span class="sxs-lookup"><span data-stu-id="291d1-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="291d1-104">Consultando informações de cluster do host Hyper-V para o convidado.</span><span class="sxs-lookup"><span data-stu-id="291d1-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="291d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="291d1-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="291d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="291d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="291d1-107">*GuestClusterInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="291d1-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="291d1-108">Em caso de sucesso, contém um [**\_ GuestClusterInformation Msvm**](msvm-guestclusterinformation.md) que descreve o cluster de convidado.</span><span class="sxs-lookup"><span data-stu-id="291d1-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="291d1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="291d1-109">Return value</span></span>

<span data-ttu-id="291d1-110">Em caso de sucesso, retorna um 0 (completo sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="291d1-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="291d1-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="291d1-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-112">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="291d1-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-113">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="291d1-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-114">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="291d1-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-115">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="291d1-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-116">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="291d1-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-117">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="291d1-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-118">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="291d1-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-119">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="291d1-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-120">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="291d1-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-121">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="291d1-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-122">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="291d1-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="291d1-123">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="291d1-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="291d1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="291d1-124">Requirements</span></span>



| <span data-ttu-id="291d1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="291d1-125">Requirement</span></span> | <span data-ttu-id="291d1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="291d1-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="291d1-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="291d1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="291d1-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="291d1-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="291d1-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="291d1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="291d1-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="291d1-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="291d1-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="291d1-131">Namespace</span></span><br/>                | <span data-ttu-id="291d1-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="291d1-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="291d1-133">MOF</span><span class="sxs-lookup"><span data-stu-id="291d1-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="291d1-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="291d1-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="291d1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="291d1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="291d1-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="291d1-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="291d1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="291d1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291d1-138">**Msvm \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="291d1-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 




