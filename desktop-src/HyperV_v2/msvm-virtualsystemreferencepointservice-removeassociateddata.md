---
description: Remove o log de dados associado ao ponto de referência.
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Método RemoveAssociatedData da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0d67502d349f0b0dac7cbf9a1998dcd6db0fb4a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105753470"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="753f6-103">Método RemoveAssociatedData da \_ classe VirtualSystemReferencePointService Msvm</span><span class="sxs-lookup"><span data-stu-id="753f6-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="753f6-104">Remove o log de dados associado ao ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="753f6-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="753f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="753f6-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="753f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="753f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="753f6-107">*AffectedReferencePoint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="753f6-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="753f6-108">Uma referência à instância [**de \_ VirtualSystemReferencePoint Msvm**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência a ser removido.</span><span class="sxs-lookup"><span data-stu-id="753f6-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="753f6-109">*Trabalho* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="753f6-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="753f6-110">Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="753f6-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="753f6-111">Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.</span><span class="sxs-lookup"><span data-stu-id="753f6-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="753f6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="753f6-112">Return value</span></span>

<span data-ttu-id="753f6-113">Em caso de sucesso, retorna um 0 (completo sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="753f6-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="753f6-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="753f6-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-115">**Parâmetros de método marcados-trabalho iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="753f6-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-116">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="753f6-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-117">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="753f6-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-118">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="753f6-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-119">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="753f6-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-120">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="753f6-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-121">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="753f6-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-122">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="753f6-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-123">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="753f6-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-124">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="753f6-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-125">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="753f6-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="753f6-126">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="753f6-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="753f6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="753f6-127">Requirements</span></span>



| <span data-ttu-id="753f6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="753f6-128">Requirement</span></span> | <span data-ttu-id="753f6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="753f6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="753f6-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="753f6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="753f6-131">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="753f6-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="753f6-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="753f6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="753f6-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="753f6-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="753f6-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="753f6-134">Namespace</span></span><br/>                | <span data-ttu-id="753f6-135">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="753f6-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="753f6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="753f6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="753f6-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="753f6-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="753f6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="753f6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="753f6-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="753f6-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="753f6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="753f6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="753f6-141">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="753f6-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




