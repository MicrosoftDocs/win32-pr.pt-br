---
description: Recupera um erro.
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Método GetError da classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011638"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="4e224-103">Método GetError da \_ classe Msvm CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="4e224-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="4e224-104">Recupera um erro.</span><span class="sxs-lookup"><span data-stu-id="4e224-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e224-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e224-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="4e224-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e224-107">*Erro* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="4e224-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e224-108">Em caso de sucesso, contém uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="4e224-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e224-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e224-109">Return value</span></span>

<span data-ttu-id="4e224-110">0 em caso de êxito; caso contrário, um erro.</span><span class="sxs-lookup"><span data-stu-id="4e224-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="4e224-111">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="4e224-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-112">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="4e224-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-113">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="4e224-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-114">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="4e224-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-115">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="4e224-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-116">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="4e224-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-117">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4e224-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-118">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4e224-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-119">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="4e224-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-120">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4e224-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-121">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="4e224-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4e224-122">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4e224-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4e224-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e224-123">Requirements</span></span>



| <span data-ttu-id="4e224-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e224-124">Requirement</span></span> | <span data-ttu-id="4e224-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4e224-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e224-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e224-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4e224-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="4e224-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4e224-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e224-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4e224-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4e224-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4e224-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="4e224-130">Namespace</span></span><br/>                | <span data-ttu-id="4e224-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="4e224-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4e224-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4e224-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e224-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e224-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e224-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4e224-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e224-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4e224-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4e224-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e224-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e224-137">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="4e224-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




