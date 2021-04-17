---
title: Método IBackgroundCopyCallback JobModification (Deliveryoptimization. h)
description: A otimização de entrega (DO) chama sua implementação do método JobModification quando o trabalho foi modificado.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Método JobModification
- Método JobModification, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, método JobModification
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812092"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="90211-106">Método IBackgroundCopyCallback:: JobModification</span><span class="sxs-lookup"><span data-stu-id="90211-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="90211-107">A otimização de entrega (DO) chama sua implementação do método [**JobModification**](https://www.bing.com/search?q=**JobModification**) quando o trabalho foi modificado.</span><span class="sxs-lookup"><span data-stu-id="90211-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="90211-108">O serviço gera esse evento quando bytes são transferidos, os arquivos foram adicionados ao trabalho, as propriedades foram modificadas ou o estado do trabalho foi alterado.</span><span class="sxs-lookup"><span data-stu-id="90211-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="90211-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90211-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="90211-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90211-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90211-111">*pJob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90211-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90211-112">Contém os métodos para acessar informações de propriedade, progresso e estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="90211-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="90211-113">Não liberar *pJob*; Libera a interface quando o método [**JobModification**](https://www.bing.com/search?q=**JobModification**) retorna.</span><span class="sxs-lookup"><span data-stu-id="90211-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="90211-114">*dwReserved* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90211-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90211-115">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="90211-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90211-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90211-116">Return value</span></span>

<span data-ttu-id="90211-117">Esse método deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="90211-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="90211-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90211-118">Requirements</span></span>



| <span data-ttu-id="90211-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="90211-119">Requirement</span></span> | <span data-ttu-id="90211-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90211-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90211-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90211-121">Minimum supported client</span></span><br/> | <span data-ttu-id="90211-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="90211-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="90211-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90211-123">Minimum supported server</span></span><br/> | <span data-ttu-id="90211-124">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="90211-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="90211-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90211-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="90211-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="90211-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="90211-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="90211-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90211-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90211-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="90211-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90211-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="90211-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90211-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="90211-131">DLL</span><span class="sxs-lookup"><span data-stu-id="90211-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90211-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90211-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="90211-133">IID</span><span class="sxs-lookup"><span data-stu-id="90211-133">IID</span></span><br/>                      | <span data-ttu-id="90211-134">IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="90211-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="90211-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="90211-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90211-136">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="90211-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="90211-137">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="90211-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





