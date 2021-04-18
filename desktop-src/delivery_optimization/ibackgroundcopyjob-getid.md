---
title: Método método ibackgroundcopyjob GetId (Deliveryoptimization. h)
description: Recupera o identificador usado para identificar o trabalho na fila.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- Método GetId
- Método GetId, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105807180"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="38703-106">Método método ibackgroundcopyjob:: GetId</span><span class="sxs-lookup"><span data-stu-id="38703-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="38703-107">Recupera o identificador usado para identificar o trabalho na fila.</span><span class="sxs-lookup"><span data-stu-id="38703-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="38703-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="38703-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="38703-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38703-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38703-110">*pJobID* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="38703-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38703-111">O GUID que identifica o trabalho dentro da fila do.</span><span class="sxs-lookup"><span data-stu-id="38703-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38703-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38703-112">Return value</span></span>

<span data-ttu-id="38703-113">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="38703-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="38703-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38703-114">Remarks</span></span>

<span data-ttu-id="38703-115">O serviço gera o identificador quando você [cria](ibackgroundcopymanager-createjob.md) o trabalho.</span><span class="sxs-lookup"><span data-stu-id="38703-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="38703-116">Para usar o identificador para recuperar um ponteiro de interface [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md) para o trabalho, chame o método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .</span><span class="sxs-lookup"><span data-stu-id="38703-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="38703-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38703-117">Requirements</span></span>



| <span data-ttu-id="38703-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="38703-118">Requirement</span></span> | <span data-ttu-id="38703-119">Valor</span><span class="sxs-lookup"><span data-stu-id="38703-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38703-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38703-120">Minimum supported client</span></span><br/> | <span data-ttu-id="38703-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="38703-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="38703-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38703-122">Minimum supported server</span></span><br/> | <span data-ttu-id="38703-123">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="38703-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="38703-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38703-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="38703-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="38703-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="38703-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="38703-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38703-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38703-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="38703-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38703-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="38703-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38703-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="38703-130">DLL</span><span class="sxs-lookup"><span data-stu-id="38703-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38703-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38703-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="38703-132">IID</span><span class="sxs-lookup"><span data-stu-id="38703-132">IID</span></span><br/>                      | <span data-ttu-id="38703-133">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="38703-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="38703-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="38703-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38703-135">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="38703-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="38703-136">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="38703-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="38703-137">**IBackgroundCopyManager::GetJob**</span><span class="sxs-lookup"><span data-stu-id="38703-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





