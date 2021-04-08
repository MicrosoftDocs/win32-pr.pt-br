---
description: Um método para eliminar esse trabalho e todos os processos subjacentes e remover quaisquer associações de pendente. Esse método é preterido; Use RequestChangeState em vez disso.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Método KillJob da classe CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921543"
---
# <a name="killjob-method-of-the-cim_job-class"></a><span data-ttu-id="50d3c-104">Método KillJob da classe de \_ trabalho CIM</span><span class="sxs-lookup"><span data-stu-id="50d3c-104">KillJob method of the CIM\_Job class</span></span>

<span data-ttu-id="50d3c-105">Um método para eliminar esse trabalho e quaisquer processos subjacentes e remover quaisquer associações ' pendente '.</span><span class="sxs-lookup"><span data-stu-id="50d3c-105">A method to kill this job and any underlying processes, and to remove any 'dangling' associations.</span></span> <span data-ttu-id="50d3c-106">Esse método é preterido; Use **RequestChangeState** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="50d3c-106">This method is deprecated; use **RequestChangeState** instead.</span></span> <span data-ttu-id="50d3c-107">O **KillJob** está sendo preterido porque não há nenhuma distinção entre um desligamento ordenado e uma eliminação imediata.</span><span class="sxs-lookup"><span data-stu-id="50d3c-107">**KillJob** is being deprecated because there is no distinction made between an orderly shutdown and an immediate kill.</span></span> <span data-ttu-id="50d3c-108">[**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fornece as opções ' Terminate ' e ' Kill ' para permitir essa distinção.</span><span class="sxs-lookup"><span data-stu-id="50d3c-108">[**CIM\_ConcreteJob**](cim-concretejob.md).**RequestStateChange**() provides 'Terminate' and 'Kill' options to allow this distinction.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d3c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50d3c-109">Syntax</span></span>


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a><span data-ttu-id="50d3c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50d3c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d3c-111">*DeleteOnKill* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50d3c-111">*DeleteOnKill* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d3c-112">Indica se o trabalho deve ou não ser excluído automaticamente após o encerramento.</span><span class="sxs-lookup"><span data-stu-id="50d3c-112">Indicates whether or not the Job should be automatically deleted upon termination.</span></span> <span data-ttu-id="50d3c-113">Esse parâmetro tem precedência sobre a propriedade **DeleteOnCompletion** .</span><span class="sxs-lookup"><span data-stu-id="50d3c-113">This parameter takes precedence over the **DeleteOnCompletion** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d3c-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50d3c-114">Return value</span></span>

<span data-ttu-id="50d3c-115">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="50d3c-115">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="50d3c-116">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="50d3c-116">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-117">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="50d3c-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-118">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="50d3c-118">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-119">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="50d3c-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-120">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="50d3c-120">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-121">**Acesso negado** (6)</span><span class="sxs-lookup"><span data-stu-id="50d3c-121">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-122">**Não encontrado** (7)</span><span class="sxs-lookup"><span data-stu-id="50d3c-122">**Not Found** (7)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="50d3c-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="50d3c-124">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="50d3c-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="50d3c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50d3c-125">Requirements</span></span>



| <span data-ttu-id="50d3c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="50d3c-126">Requirement</span></span> | <span data-ttu-id="50d3c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="50d3c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d3c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50d3c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50d3c-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="50d3c-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="50d3c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50d3c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50d3c-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="50d3c-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="50d3c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="50d3c-132">Namespace</span></span><br/>                | <span data-ttu-id="50d3c-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="50d3c-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="50d3c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="50d3c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="50d3c-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="50d3c-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="50d3c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="50d3c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d3c-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="50d3c-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="50d3c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="50d3c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d3c-139">**Trabalho do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="50d3c-139">**CIM\_Job**</span></span>](cim-job.md)
</dt> </dl>

 

 




