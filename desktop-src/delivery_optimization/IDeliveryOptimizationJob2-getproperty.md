---
title: 'Método IDeliveryOptimizationJob2:: GetProperty'
description: Retorna uma única propriedade do trabalho do.
keywords:
- Método GetProperty
- Método GetProperty, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454885"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a><span data-ttu-id="83776-106">Método IDeliveryOptimizationJob2:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="83776-106">IDeliveryOptimizationJob2::GetProperty method</span></span>

<span data-ttu-id="83776-107">Esse método retorna uma única propriedade do trabalho do.</span><span class="sxs-lookup"><span data-stu-id="83776-107">This method returns a single property of the DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="83776-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83776-108">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="83776-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83776-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83776-110">*propId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83776-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83776-111">A ID de propriedade necessária a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="83776-111">The required property ID to get.</span></span> <span data-ttu-id="83776-112">Há suporte apenas para **DOJobPropertyId_ExtendedErrorInfo** do tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="83776-112">Only **DOJobPropertyId_ExtendedErrorInfo** of type VT_BSTR is supported.</span></span>

</dd> <dt>

<span data-ttu-id="83776-113">*propvalue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="83776-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83776-114">O valor da propriedade resultante, armazenado em um tipo VARIANT.</span><span class="sxs-lookup"><span data-stu-id="83776-114">The resultant property value, stored in a VARIANT type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83776-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83776-115">Return value</span></span>

<span data-ttu-id="83776-116">Esse método retorna os valores de HRESULT a seguir.</span><span class="sxs-lookup"><span data-stu-id="83776-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="83776-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="83776-117">Return code</span></span>                  | <span data-ttu-id="83776-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="83776-118">Description</span></span>          |
|------------------------------|----------------------|
| <span data-ttu-id="83776-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="83776-119">**S_OK**</span></span>                     | <span data-ttu-id="83776-120">Sucesso</span><span class="sxs-lookup"><span data-stu-id="83776-120">Success</span></span>              |
| <span data-ttu-id="83776-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="83776-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="83776-122">ID de propriedade desconhecida.</span><span class="sxs-lookup"><span data-stu-id="83776-122">Unknown property ID.</span></span> |

## <a name="requirements"></a><span data-ttu-id="83776-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83776-123">Requirements</span></span>

| <span data-ttu-id="83776-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="83776-124">Requirement</span></span> | <span data-ttu-id="83776-125">Valor</span><span class="sxs-lookup"><span data-stu-id="83776-125">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="83776-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83776-126">Minimum supported client</span></span>  | <span data-ttu-id="83776-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="83776-127">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="83776-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83776-128">Minimum supported server</span></span>  | <span data-ttu-id="83776-129">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="83776-129">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="83776-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83776-130">Header</span></span>                    | <span data-ttu-id="83776-131">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="83776-131">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="83776-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="83776-132">IDL</span></span>                       | <span data-ttu-id="83776-133">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="83776-133">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="83776-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83776-134">Library</span></span>                   | <span data-ttu-id="83776-135">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="83776-135">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="83776-136">DLL</span><span class="sxs-lookup"><span data-stu-id="83776-136">DLL</span></span>                       | <span data-ttu-id="83776-137">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="83776-137">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="83776-138">IID</span><span class="sxs-lookup"><span data-stu-id="83776-138">IID</span></span>                       | <span data-ttu-id="83776-139">IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="83776-139">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="83776-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="83776-140">See also</span></span>

[<span data-ttu-id="83776-141">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="83776-141">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
