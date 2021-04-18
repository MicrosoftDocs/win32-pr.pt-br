---
description: Exclui o ponto de referência especificado.
ms.assetid: cb5245b6-5984-40ec-a37e-e4a0a62e318a
title: Método DestroyReferencePoint da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cf7a21e60369a928cc1d617e24db5f5fc70c522
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105766893"
---
# <a name="destroyreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="aa70d-103">Método DestroyReferencePoint da \_ classe VirtualSystemReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="aa70d-103">DestroyReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="aa70d-104">Exclui o ponto de referência especificado.</span><span class="sxs-lookup"><span data-stu-id="aa70d-104">Deletes the specified reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa70d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa70d-105">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="aa70d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa70d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa70d-107">*AffectedReferencePoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa70d-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa70d-108">Uma referência à instância [**de \_ VirtualSystemReferencePoint Msvm**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência a ser removido.</span><span class="sxs-lookup"><span data-stu-id="aa70d-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="aa70d-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="aa70d-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa70d-110">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="aa70d-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="aa70d-111">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="aa70d-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa70d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa70d-112">Return value</span></span>

<span data-ttu-id="aa70d-113">Em caso de sucesso, retorna um 0 (completo sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="aa70d-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="aa70d-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="aa70d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="aa70d-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="aa70d-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="aa70d-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="aa70d-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="aa70d-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="aa70d-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="aa70d-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="aa70d-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="aa70d-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="aa70d-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="aa70d-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aa70d-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="aa70d-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aa70d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa70d-127">Requirements</span></span>



| <span data-ttu-id="aa70d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa70d-128">Requirement</span></span> | <span data-ttu-id="aa70d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="aa70d-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa70d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa70d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aa70d-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="aa70d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="aa70d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa70d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aa70d-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aa70d-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aa70d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa70d-134">Namespace</span></span><br/>                | <span data-ttu-id="aa70d-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="aa70d-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa70d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="aa70d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa70d-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa70d-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa70d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aa70d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa70d-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa70d-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa70d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa70d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa70d-141">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="aa70d-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




