---
title: Método GetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Um método genérico para obter propriedades de trabalho da otimização de entrega (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Método GetProperty
- Método GetProperty, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918538"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="3cedd-106">Método IBackgroundCopyJob5:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="3cedd-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="3cedd-107">Um método genérico para obter propriedades de trabalho da otimização de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="3cedd-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cedd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cedd-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="3cedd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cedd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cedd-110">*PropertyId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3cedd-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cedd-111">A ID da propriedade que está sendo obtida especificada como um [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3cedd-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="3cedd-112">*pPropertyValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3cedd-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3cedd-113">O valor da propriedade retornado como uma União de BITS_JOB_PROPERTY_VALUE.</span><span class="sxs-lookup"><span data-stu-id="3cedd-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cedd-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cedd-114">Return value</span></span>

<span data-ttu-id="3cedd-115">O método retorna os valores de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="3cedd-115">The method returns the following return values.</span></span>



| <span data-ttu-id="3cedd-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3cedd-116">Return code</span></span>                                                                          | <span data-ttu-id="3cedd-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cedd-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="3cedd-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3cedd-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="3cedd-119">Sucesso</span><span class="sxs-lookup"><span data-stu-id="3cedd-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3cedd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cedd-120">Requirements</span></span>



| <span data-ttu-id="3cedd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cedd-121">Requirement</span></span> | <span data-ttu-id="3cedd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3cedd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cedd-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cedd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3cedd-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="3cedd-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3cedd-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cedd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3cedd-126">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="3cedd-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3cedd-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cedd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cedd-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cedd-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cedd-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="3cedd-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3cedd-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3cedd-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3cedd-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3cedd-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="3cedd-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cedd-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3cedd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="3cedd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cedd-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cedd-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3cedd-135">IID</span><span class="sxs-lookup"><span data-stu-id="3cedd-135">IID</span></span><br/>                      | <span data-ttu-id="3cedd-136">IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="3cedd-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="3cedd-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cedd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cedd-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="3cedd-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="3cedd-139">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="3cedd-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





