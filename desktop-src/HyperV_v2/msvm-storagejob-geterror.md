---
description: Método GetError da classe Msvm_StorageJob – recupera o erro.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Método GetError da classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 00434ef529b7f26755f52833ff6f37310c7dc210
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109594"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="e5571-103">Método GetError da \_ classe Msvm StorageJob</span><span class="sxs-lookup"><span data-stu-id="e5571-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="e5571-104">Recupera o erro.</span><span class="sxs-lookup"><span data-stu-id="e5571-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5571-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5571-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="e5571-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5571-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5571-107">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="e5571-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5571-108">O erro recuperado.</span><span class="sxs-lookup"><span data-stu-id="e5571-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5571-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e5571-109">Return value</span></span>

<span data-ttu-id="e5571-110">Esse método retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e5571-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e5571-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="e5571-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-112">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="e5571-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-113">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e5571-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-114">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="e5571-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-115">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e5571-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-116">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="e5571-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-117">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e5571-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-118">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e5571-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-119">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="e5571-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-120">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e5571-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-121">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="e5571-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e5571-122">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e5571-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e5571-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5571-123">Requirements</span></span>



| <span data-ttu-id="e5571-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5571-124">Requirement</span></span> | <span data-ttu-id="e5571-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e5571-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5571-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5571-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e5571-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e5571-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e5571-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5571-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e5571-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e5571-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e5571-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5571-130">Namespace</span></span><br/>                | <span data-ttu-id="e5571-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e5571-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e5571-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e5571-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5571-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5571-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5571-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e5571-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5571-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5571-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5571-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e5571-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5571-137">**Msvm \_ StorageJob**</span><span class="sxs-lookup"><span data-stu-id="e5571-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 




