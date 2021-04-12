---
title: 'Método IDeliveryOptimizationFile2:: GetProperty'
description: 'Esse método retorna uma única propriedade do arquivo do. | Método IDeliveryOptimizationFile2:: GetProperty'
keywords:
- Método GetProperty
- Método GetProperty, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, método GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298394"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="d092d-107">Método IDeliveryOptimizationFile2:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="d092d-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="d092d-108">Esse método retorna uma única propriedade do arquivo do.</span><span class="sxs-lookup"><span data-stu-id="d092d-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d092d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d092d-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="d092d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d092d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d092d-111">*propId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d092d-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d092d-112">A ID de propriedade necessária para obter do tipo DOFilePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d092d-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="d092d-113">*propvalue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d092d-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d092d-114">O valor da propriedade armazenado em uma variante.</span><span class="sxs-lookup"><span data-stu-id="d092d-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d092d-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d092d-115">Return value</span></span>

<span data-ttu-id="d092d-116">Esse método retorna os valores de HRESULT a seguir.</span><span class="sxs-lookup"><span data-stu-id="d092d-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="d092d-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d092d-117">Return code</span></span>                  | <span data-ttu-id="d092d-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d092d-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d092d-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="d092d-119">**S_OK**</span></span>                     | <span data-ttu-id="d092d-120">Êxito</span><span class="sxs-lookup"><span data-stu-id="d092d-120">Success</span></span>                                             |
| <span data-ttu-id="d092d-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="d092d-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="d092d-122">ID de propriedade desconhecida.</span><span class="sxs-lookup"><span data-stu-id="d092d-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="d092d-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="d092d-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="d092d-124">A propriedade é somente gravação e não pode ser lida.</span><span class="sxs-lookup"><span data-stu-id="d092d-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="d092d-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="d092d-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="d092d-126">Nenhuma propriedade foi definida por meio do método SetProperty.</span><span class="sxs-lookup"><span data-stu-id="d092d-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="d092d-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="d092d-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="d092d-128">Falha de alocação de memória</span><span class="sxs-lookup"><span data-stu-id="d092d-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="d092d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d092d-129">Requirements</span></span>

| <span data-ttu-id="d092d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d092d-130">Requirement</span></span> | <span data-ttu-id="d092d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d092d-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d092d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d092d-132">Minimum supported client</span></span>  | <span data-ttu-id="d092d-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="d092d-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="d092d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d092d-134">Minimum supported server</span></span>  | <span data-ttu-id="d092d-135">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="d092d-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="d092d-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d092d-136">Header</span></span>                    | <span data-ttu-id="d092d-137">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="d092d-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="d092d-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="d092d-138">IDL</span></span>                       | <span data-ttu-id="d092d-139">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="d092d-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="d092d-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d092d-140">Library</span></span>                   | <span data-ttu-id="d092d-141">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="d092d-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="d092d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d092d-142">DLL</span></span>                       | <span data-ttu-id="d092d-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="d092d-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="d092d-144">IID</span><span class="sxs-lookup"><span data-stu-id="d092d-144">IID</span></span>                       | <span data-ttu-id="d092d-145">IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="d092d-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="d092d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d092d-146">See also</span></span>

[<span data-ttu-id="d092d-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="d092d-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
