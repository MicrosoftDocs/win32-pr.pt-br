---
title: 'Método IDeliveryOptimizationJob2:: SetProperty'
description: Este método não é usado.
keywords:
- Método SetProperty
- Método SetProperty, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, método SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369675"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="f0e35-106">Método IDeliveryOptimizationJob2:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="f0e35-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="f0e35-107">Este método não é usado.</span><span class="sxs-lookup"><span data-stu-id="f0e35-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e35-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0e35-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="f0e35-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0e35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0e35-110">*propId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0e35-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e35-111">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f0e35-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="f0e35-112">*propvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0e35-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0e35-113">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="f0e35-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0e35-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0e35-114">Return value</span></span>

<span data-ttu-id="f0e35-115">Se propId for **DOJobPropertyId_ExtendedErrorInfo**, o valor retornado será **DO_E_READ_ONLY_PROPERTY**, caso contrário, a função retornará **DO_E_UNKNOWN_PROPERTY_ID**.</span><span class="sxs-lookup"><span data-stu-id="f0e35-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0e35-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0e35-116">Requirements</span></span>

| <span data-ttu-id="f0e35-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0e35-117">Requirement</span></span> | <span data-ttu-id="f0e35-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f0e35-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f0e35-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0e35-119">Minimum supported client</span></span>  | <span data-ttu-id="f0e35-120">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="f0e35-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="f0e35-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0e35-121">Minimum supported server</span></span>  | <span data-ttu-id="f0e35-122">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f0e35-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="f0e35-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0e35-123">Header</span></span>                    | <span data-ttu-id="f0e35-124">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="f0e35-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="f0e35-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="f0e35-125">IDL</span></span>                       | <span data-ttu-id="f0e35-126">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="f0e35-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="f0e35-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0e35-127">Library</span></span>                   | <span data-ttu-id="f0e35-128">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="f0e35-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="f0e35-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f0e35-129">DLL</span></span>                       | <span data-ttu-id="f0e35-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="f0e35-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="f0e35-131">IID</span><span class="sxs-lookup"><span data-stu-id="f0e35-131">IID</span></span>                       | <span data-ttu-id="f0e35-132">IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="f0e35-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="f0e35-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0e35-133">See also</span></span>

[<span data-ttu-id="f0e35-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="f0e35-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
