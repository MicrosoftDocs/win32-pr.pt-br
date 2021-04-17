---
title: 'Método IDeliveryOptimizationFile2:: SetProperty'
description: 'Esse método retorna uma única propriedade do arquivo do. | Método IDeliveryOptimizationFile2:: SetProperty'
keywords:
- Método SetProperty
- Método SetProperty, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105811969"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="46cce-107">Método IDeliveryOptimizationFile2:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="46cce-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="46cce-108">Esse método retorna uma única propriedade do arquivo do.</span><span class="sxs-lookup"><span data-stu-id="46cce-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cce-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46cce-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="46cce-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46cce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cce-111">*propId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cce-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cce-112">A ID de propriedade necessária para definir o tipo DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="46cce-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="46cce-113">*propvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46cce-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46cce-114">O valor da propriedade a ser definido, do tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="46cce-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cce-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46cce-115">Return value</span></span>

<span data-ttu-id="46cce-116">Esse método retorna os valores de HRESULT a seguir.</span><span class="sxs-lookup"><span data-stu-id="46cce-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="46cce-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="46cce-117">Return code</span></span>                  | <span data-ttu-id="46cce-118">Description</span><span class="sxs-lookup"><span data-stu-id="46cce-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="46cce-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="46cce-119">**S_OK**</span></span>                     | <span data-ttu-id="46cce-120">Sucesso</span><span class="sxs-lookup"><span data-stu-id="46cce-120">Success</span></span>                                                            |
| <span data-ttu-id="46cce-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="46cce-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="46cce-122">ID de propriedade desconhecida</span><span class="sxs-lookup"><span data-stu-id="46cce-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="46cce-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="46cce-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="46cce-124">O trabalho não está atualmente em um estado que permita uma configuração de propriedade</span><span class="sxs-lookup"><span data-stu-id="46cce-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="46cce-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46cce-125">Requirements</span></span>

| <span data-ttu-id="46cce-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="46cce-126">Requirement</span></span> | <span data-ttu-id="46cce-127">Valor</span><span class="sxs-lookup"><span data-stu-id="46cce-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="46cce-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46cce-128">Minimum supported client</span></span>  | <span data-ttu-id="46cce-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="46cce-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="46cce-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46cce-130">Minimum supported server</span></span>  | <span data-ttu-id="46cce-131">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="46cce-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="46cce-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46cce-132">Header</span></span>                    | <span data-ttu-id="46cce-133">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="46cce-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="46cce-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="46cce-134">IDL</span></span>                       | <span data-ttu-id="46cce-135">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="46cce-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="46cce-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46cce-136">Library</span></span>                   | <span data-ttu-id="46cce-137">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="46cce-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="46cce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="46cce-138">DLL</span></span>                       | <span data-ttu-id="46cce-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="46cce-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="46cce-140">IID</span><span class="sxs-lookup"><span data-stu-id="46cce-140">IID</span></span>                       | <span data-ttu-id="46cce-141">IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="46cce-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="46cce-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="46cce-142">See also</span></span>

[<span data-ttu-id="46cce-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="46cce-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
