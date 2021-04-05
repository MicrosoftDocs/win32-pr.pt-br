---
title: Método GetDisplayName de método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera o nome de exibição para o trabalho. Normalmente, você usa o nome de exibição para identificar o trabalho em uma interface do usuário.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- Método GetDisplayName
- Método GetDisplayName, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, Método GetDisplayName
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918929"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="50b03-107">Método método ibackgroundcopyjob:: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="50b03-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="50b03-108">Recupera o nome de exibição para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="50b03-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="50b03-109">Normalmente, você usa o nome de exibição para identificar o trabalho em uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="50b03-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b03-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50b03-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="50b03-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50b03-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50b03-112">*ppDisplayName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50b03-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50b03-113">Cadeia de caracteres terminada em nulo que contém o nome para exibição que identifica o trabalho.</span><span class="sxs-lookup"><span data-stu-id="50b03-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="50b03-114">Mais de um trabalho pode ter o mesmo nome de exibição.</span><span class="sxs-lookup"><span data-stu-id="50b03-114">More than one job can have the same display name.</span></span> <span data-ttu-id="50b03-115">Chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppDisplayName* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="50b03-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50b03-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50b03-116">Return value</span></span>

<span data-ttu-id="50b03-117">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="50b03-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="50b03-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="50b03-118">Return code</span></span>                                                                                  | <span data-ttu-id="50b03-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="50b03-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="50b03-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="50b03-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="50b03-121">O nome para exibição foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="50b03-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="50b03-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="50b03-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="50b03-123">O parâmetro *ppDisplayName* não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="50b03-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50b03-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b03-124">Requirements</span></span>



| <span data-ttu-id="50b03-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b03-125">Requirement</span></span> | <span data-ttu-id="50b03-126">Valor</span><span class="sxs-lookup"><span data-stu-id="50b03-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b03-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50b03-127">Minimum supported client</span></span><br/> | <span data-ttu-id="50b03-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="50b03-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50b03-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50b03-129">Minimum supported server</span></span><br/> | <span data-ttu-id="50b03-130">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="50b03-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="50b03-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50b03-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="50b03-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="50b03-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="50b03-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="50b03-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50b03-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50b03-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="50b03-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50b03-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="50b03-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50b03-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="50b03-137">DLL</span><span class="sxs-lookup"><span data-stu-id="50b03-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50b03-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50b03-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="50b03-139">IID</span><span class="sxs-lookup"><span data-stu-id="50b03-139">IID</span></span><br/>                      | <span data-ttu-id="50b03-140">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="50b03-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="50b03-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="50b03-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b03-142">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="50b03-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

