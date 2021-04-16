---
description: Recupera informações adicionais sobre um erro.
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Método GetErrorEx da classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c6c392adb2b638c2d638b758696252adcb54d7e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105750463"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="8a2da-103">Método GetErrorEx da \_ classe VirtualSystemReferencePointExportJob Msvm</span><span class="sxs-lookup"><span data-stu-id="8a2da-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="8a2da-104">Recupera informações adicionais sobre um erro.</span><span class="sxs-lookup"><span data-stu-id="8a2da-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="8a2da-105">Quando o trabalho está em execução ou termina sem erro, **GetErrorEx** não retorna nenhuma instância de **GetErrorEx** .</span><span class="sxs-lookup"><span data-stu-id="8a2da-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="8a2da-106">No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, **GetErrorEx** retorna uma ou mais instâncias de [**\_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="8a2da-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a2da-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="8a2da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a2da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2da-109">*Erros* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="8a2da-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2da-110">Se o status operacional do trabalho não for "OK", esse parâmetro retornará uma matriz de instâncias [**de \_ erro Msvm**](msvm-error.md) .</span><span class="sxs-lookup"><span data-stu-id="8a2da-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="8a2da-111">Caso contrário, se o trabalho for "OK", esse parâmetro conterá **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8a2da-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2da-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a2da-112">Return value</span></span>

<span data-ttu-id="8a2da-113">Em caso de sucesso, retorna 0; caso contrário, retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="8a2da-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8a2da-114">**Concluído sem erro** (0)</span><span class="sxs-lookup"><span data-stu-id="8a2da-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-115">**Falha** (32768)</span><span class="sxs-lookup"><span data-stu-id="8a2da-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-116">**Acesso negado** (32769)</span><span class="sxs-lookup"><span data-stu-id="8a2da-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-117">**Sem suporte** (32770)</span><span class="sxs-lookup"><span data-stu-id="8a2da-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-118">O **status é desconhecido** (32771)</span><span class="sxs-lookup"><span data-stu-id="8a2da-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-119">**Tempo limite** (32772)</span><span class="sxs-lookup"><span data-stu-id="8a2da-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-120">**Parâmetro inválido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8a2da-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-121">O **sistema está em uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8a2da-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-122">**Estado inválido para esta operação** (32775)</span><span class="sxs-lookup"><span data-stu-id="8a2da-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-123">**Tipo de dados incorreto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8a2da-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-124">O **sistema não está disponível** (32777)</span><span class="sxs-lookup"><span data-stu-id="8a2da-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8a2da-125">**Memória insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8a2da-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a2da-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a2da-126">Requirements</span></span>



| <span data-ttu-id="8a2da-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a2da-127">Requirement</span></span> | <span data-ttu-id="8a2da-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8a2da-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2da-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a2da-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2da-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="8a2da-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8a2da-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a2da-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2da-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8a2da-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="8a2da-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a2da-133">Namespace</span></span><br/>                | <span data-ttu-id="8a2da-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="8a2da-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8a2da-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8a2da-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a2da-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a2da-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a2da-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8a2da-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a2da-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a2da-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a2da-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a2da-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2da-140">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="8a2da-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




