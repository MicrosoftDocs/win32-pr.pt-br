---
title: Método SetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Um método genérico para definir propriedades de trabalho de otimização de entrega (DO).
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- Método SetProperty
- Método SetProperty, interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644989"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="e6f35-106">Método IBackgroundCopyJob5:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="e6f35-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="e6f35-107">Um método genérico para definir propriedades de trabalho de otimização de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="e6f35-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f35-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6f35-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="e6f35-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6f35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6f35-110">*PropertyId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6f35-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f35-111">A ID da propriedade que está sendo definida como um [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="e6f35-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="e6f35-112">*PropertyValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e6f35-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f35-113">O valor da propriedade que está sendo definida.</span><span class="sxs-lookup"><span data-stu-id="e6f35-113">The value of the property that is being set.</span></span> <span data-ttu-id="e6f35-114">Para manter um valor cujo tipo é apropriado para a propriedade, esse valor é especificado por meio da União de [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) que é composta por todos os tipos de propriedade conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e6f35-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6f35-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6f35-115">Return value</span></span>

<span data-ttu-id="e6f35-116">O método retorna os valores de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6f35-116">The method returns the following return values.</span></span>



| <span data-ttu-id="e6f35-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e6f35-117">Return code</span></span>                                                                          | <span data-ttu-id="e6f35-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6f35-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="e6f35-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="e6f35-120">Êxito</span><span class="sxs-lookup"><span data-stu-id="e6f35-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e6f35-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6f35-121">Requirements</span></span>



| <span data-ttu-id="e6f35-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6f35-122">Requirement</span></span> | <span data-ttu-id="e6f35-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e6f35-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f35-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6f35-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f35-125">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e6f35-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e6f35-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6f35-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f35-127">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e6f35-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e6f35-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6f35-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6f35-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6f35-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="e6f35-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6f35-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e6f35-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6f35-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6f35-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e6f35-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e6f35-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6f35-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6f35-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e6f35-136">IID</span><span class="sxs-lookup"><span data-stu-id="e6f35-136">IID</span></span><br/>                      | <span data-ttu-id="e6f35-137">IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="e6f35-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="e6f35-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6f35-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f35-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="e6f35-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="e6f35-140">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="e6f35-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





