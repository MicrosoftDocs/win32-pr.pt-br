---
title: Método IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: A otimização de entrega (DO) chama sua implementação do método JobTransferred quando todos os arquivos no trabalho foram transferidos com êxito.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Método JobTransferred
- Método JobTransferred, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, método JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085480"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="892d7-106">Método IBackgroundCopyCallback:: JobTransferred</span><span class="sxs-lookup"><span data-stu-id="892d7-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="892d7-107">A otimização de entrega (DO) chama sua implementação do método **JobTransferred** quando todos os arquivos no trabalho foram transferidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="892d7-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="892d7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="892d7-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="892d7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="892d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892d7-110">*pJob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="892d7-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892d7-111">Contém informações relacionadas ao trabalho, como a hora em que o trabalho foi concluído, o número de bytes transferidos e o número de arquivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="892d7-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="892d7-112">Não liberar *pJob*; Libera a interface quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="892d7-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892d7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="892d7-113">Return value</span></span>

<span data-ttu-id="892d7-114">Esse método deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="892d7-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="892d7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="892d7-115">Remarks</span></span>

<span data-ttu-id="892d7-116">Normalmente, sua implementação deve chamar o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que o transferiu com êxito os arquivos.</span><span class="sxs-lookup"><span data-stu-id="892d7-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="892d7-117">Baixar arquivos e o arquivo de resposta não estarão disponíveis no cliente até que você chame o método **Complete** .</span><span class="sxs-lookup"><span data-stu-id="892d7-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="892d7-118">Se você não chamar o método [**Complete**](ibackgroundcopyjob-complete.md) ou o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) , o cancelará o trabalho após 30 dias e excluirá os arquivos incompletos.</span><span class="sxs-lookup"><span data-stu-id="892d7-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="892d7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="892d7-119">Requirements</span></span>



| <span data-ttu-id="892d7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="892d7-120">Requirement</span></span> | <span data-ttu-id="892d7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="892d7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892d7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="892d7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="892d7-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="892d7-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="892d7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="892d7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="892d7-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="892d7-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="892d7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="892d7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="892d7-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="892d7-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="892d7-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="892d7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="892d7-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="892d7-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="892d7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="892d7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="892d7-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="892d7-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="892d7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="892d7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="892d7-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="892d7-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="892d7-134">IID</span><span class="sxs-lookup"><span data-stu-id="892d7-134">IID</span></span><br/>                      | <span data-ttu-id="892d7-135">IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="892d7-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="892d7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="892d7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892d7-137">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="892d7-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="892d7-138">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="892d7-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="892d7-139">**Método ibackgroundcopyjob:: concluir**</span><span class="sxs-lookup"><span data-stu-id="892d7-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="892d7-140">**Método ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="892d7-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





