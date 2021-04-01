---
description: Atualiza o nome do elemento para o \_ objeto CIM CollectionOfMSEs especificado.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Método renomecollection da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836863"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="c3024-103">Método renomecollection da classe Msvm \_ CollectionManagementService</span><span class="sxs-lookup"><span data-stu-id="c3024-103">RenameCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="c3024-104">Atualiza o nome do elemento para o objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="c3024-104">Updates the element name for the specified [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3024-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3024-105">Syntax</span></span>


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c3024-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3024-107">*Coleção* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="c3024-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3024-108">A coleção a ser renomeada.</span><span class="sxs-lookup"><span data-stu-id="c3024-108">The collection to rename.</span></span>

</dd> <dt>

<span data-ttu-id="c3024-109">*NewName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c3024-109">*NewName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3024-110">O novo nome a ser usado.</span><span class="sxs-lookup"><span data-stu-id="c3024-110">The new name to use.</span></span>

</dd> <dt>

<span data-ttu-id="c3024-111">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c3024-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3024-112">Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).</span><span class="sxs-lookup"><span data-stu-id="c3024-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3024-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3024-113">Return value</span></span>

<span data-ttu-id="c3024-114">Retornará 0 se for bem-sucedido ou 4096 se o trabalho for iniciado; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c3024-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c3024-115">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="c3024-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-116">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c3024-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-117">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="c3024-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-118">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c3024-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-119">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="c3024-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-120">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c3024-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-121">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="c3024-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-122">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c3024-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-123">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c3024-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-124">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="c3024-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-125">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c3024-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-126">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="c3024-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-127">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c3024-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c3024-128">**Arquivo não encontrado** (32779)</span><span class="sxs-lookup"><span data-stu-id="c3024-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c3024-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3024-129">Requirements</span></span>



| <span data-ttu-id="c3024-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3024-130">Requirement</span></span> | <span data-ttu-id="c3024-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c3024-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3024-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3024-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c3024-133">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c3024-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="c3024-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3024-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c3024-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c3024-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c3024-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="c3024-136">Namespace</span></span><br/>                | <span data-ttu-id="c3024-137">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="c3024-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c3024-138">MOF</span><span class="sxs-lookup"><span data-stu-id="c3024-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3024-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3024-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3024-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c3024-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3024-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3024-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c3024-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3024-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3024-143">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="c3024-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




