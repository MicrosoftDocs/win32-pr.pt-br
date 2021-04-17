---
description: Exclui o objeto CIM \_ CollectionOfMSEs fornecido.
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Método destroycollection da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782356"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="12821-103">Método destroycollection da classe Msvm \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="12821-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="12821-104">Exclui o objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.</span><span class="sxs-lookup"><span data-stu-id="12821-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="12821-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12821-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="12821-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12821-107">*Coleção* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="12821-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12821-108">A coleção a ser destruída.</span><span class="sxs-lookup"><span data-stu-id="12821-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="12821-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="12821-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12821-110">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="12821-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12821-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12821-111">Return value</span></span>

<span data-ttu-id="12821-112">Retornará 0 se for bem-sucedido ou 4096 se o trabalho for iniciado; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="12821-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="12821-113">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="12821-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12821-114">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="12821-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12821-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="12821-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12821-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="12821-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12821-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="12821-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12821-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="12821-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12821-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="12821-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12821-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="12821-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12821-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="12821-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12821-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="12821-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12821-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="12821-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12821-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="12821-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12821-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="12821-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="12821-126">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="12821-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="12821-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12821-127">Requirements</span></span>



| <span data-ttu-id="12821-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="12821-128">Requirement</span></span> | <span data-ttu-id="12821-129">Valor</span><span class="sxs-lookup"><span data-stu-id="12821-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12821-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12821-130">Minimum supported client</span></span><br/> | <span data-ttu-id="12821-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="12821-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="12821-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12821-132">Minimum supported server</span></span><br/> | <span data-ttu-id="12821-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="12821-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="12821-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="12821-134">Namespace</span></span><br/>                | <span data-ttu-id="12821-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="12821-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="12821-136">MOF</span><span class="sxs-lookup"><span data-stu-id="12821-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12821-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12821-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12821-138">DLL</span><span class="sxs-lookup"><span data-stu-id="12821-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12821-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12821-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12821-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="12821-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12821-141">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="12821-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




