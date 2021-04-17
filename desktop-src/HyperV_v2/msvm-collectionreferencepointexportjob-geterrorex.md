---
description: Recupera informações adicionais sobre um erro.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Método GetErrorEx da classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755105"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="64d38-103">Método GetErrorEx da \_ classe CollectionReferencePointExportJob Msvm</span><span class="sxs-lookup"><span data-stu-id="64d38-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="64d38-104">Recupera informações adicionais sobre um erro.</span><span class="sxs-lookup"><span data-stu-id="64d38-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="64d38-105">Quando o trabalho está em execução ou foi encerrado sem erro, **GetErrorEx** não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="64d38-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="64d38-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, **GetErrorEx** retorna uma ou mais instâncias de **\_ erro Msvm** .</span><span class="sxs-lookup"><span data-stu-id="64d38-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64d38-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="64d38-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64d38-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d38-109">*Erros* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="64d38-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d38-110">Se o status operacional do trabalho não for "OK", esse parâmetro retornará uma matriz de instâncias [**de \_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="64d38-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="64d38-111">Caso contrário, se o trabalho for "OK", esse parâmetro conterá **NULL**.</span><span class="sxs-lookup"><span data-stu-id="64d38-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d38-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64d38-112">Return value</span></span>

<span data-ttu-id="64d38-113">Em caso de sucesso, retorna 0; caso contrário, retorna um dos seguintes valores de erro:</span><span class="sxs-lookup"><span data-stu-id="64d38-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="64d38-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="64d38-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="64d38-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="64d38-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="64d38-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="64d38-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="64d38-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="64d38-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="64d38-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="64d38-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="64d38-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="64d38-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="64d38-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="64d38-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="64d38-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64d38-126">Requirements</span></span>



| <span data-ttu-id="64d38-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d38-127">Requirement</span></span> | <span data-ttu-id="64d38-128">Valor</span><span class="sxs-lookup"><span data-stu-id="64d38-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d38-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64d38-129">Minimum supported client</span></span><br/> | <span data-ttu-id="64d38-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="64d38-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="64d38-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64d38-131">Minimum supported server</span></span><br/> | <span data-ttu-id="64d38-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="64d38-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="64d38-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="64d38-133">Namespace</span></span><br/>                | <span data-ttu-id="64d38-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="64d38-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="64d38-135">MOF</span><span class="sxs-lookup"><span data-stu-id="64d38-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64d38-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64d38-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="64d38-137">DLL</span><span class="sxs-lookup"><span data-stu-id="64d38-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64d38-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="64d38-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="64d38-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="64d38-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d38-140">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="64d38-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




