---
description: Recupera um erro devido a um trabalho com falha.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Método GetError da classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759253"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="4b470-103">Método GetError da \_ classe CIM ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="4b470-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="4b470-104">Recupera um erro devido a um trabalho com falha.</span><span class="sxs-lookup"><span data-stu-id="4b470-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="4b470-105">Quando o trabalho está em execução ou foi encerrado sem erros, esse método não retorna nenhuma instância de [**\_ erro CIM**](cim-error.md) .</span><span class="sxs-lookup"><span data-stu-id="4b470-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="4b470-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma instância de **\_ erro CIM** é retornada.</span><span class="sxs-lookup"><span data-stu-id="4b470-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b470-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b470-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="4b470-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b470-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b470-109">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4b470-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b470-110">Retorna uma instância de [**\_ erro CIM**](cim-error.md) se o **OperationalStatus** no trabalho não for "OK"; caso contrário, retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4b470-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b470-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b470-111">Return value</span></span>

<span data-ttu-id="4b470-112">Retorna um 0 em caso de êxito; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4b470-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4b470-113">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="4b470-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-114">**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="4b470-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-115">**Erro não especificado** (2)</span><span class="sxs-lookup"><span data-stu-id="4b470-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-116">**Tempo limite** (3)</span><span class="sxs-lookup"><span data-stu-id="4b470-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-117">**Com falha** (4)</span><span class="sxs-lookup"><span data-stu-id="4b470-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-118">**Parâmetro inválido** (5)</span><span class="sxs-lookup"><span data-stu-id="4b470-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-119">**Acesso negado** (6)</span><span class="sxs-lookup"><span data-stu-id="4b470-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4b470-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4b470-121">**Específico do fornecedor** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4b470-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4b470-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b470-122">Requirements</span></span>



| <span data-ttu-id="4b470-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b470-123">Requirement</span></span> | <span data-ttu-id="4b470-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4b470-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b470-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b470-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4b470-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4b470-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4b470-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b470-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4b470-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4b470-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4b470-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="4b470-129">Namespace</span></span><br/>                | <span data-ttu-id="4b470-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4b470-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b470-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4b470-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b470-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b470-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b470-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4b470-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b470-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b470-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b470-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b470-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b470-136">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="4b470-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




