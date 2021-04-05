---
title: Método GetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Obtém uma propriedade genérica de uma transferência de arquivo de otimização de entrega.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Método GetProperty
- Método GetProperty, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085477"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="6e23a-106">Método IBackgroundCopyFile5:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="6e23a-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="6e23a-107">Obtém uma propriedade genérica de uma transferência de arquivo de otimização de entrega.</span><span class="sxs-lookup"><span data-stu-id="6e23a-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e23a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e23a-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="6e23a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e23a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e23a-110">*PropertyId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6e23a-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e23a-111">Especifica a propriedade de arquivo cujo valor deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="6e23a-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="6e23a-112">*PropertyValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6e23a-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e23a-113">O valor da propriedade, retornado como um ponteiro para uma BITS_FILE_PROPERTY_VALUE Union.</span><span class="sxs-lookup"><span data-stu-id="6e23a-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="6e23a-114">Use o campo Union apropriado para o valor de ID de propriedade passado.</span><span class="sxs-lookup"><span data-stu-id="6e23a-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e23a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e23a-115">Return value</span></span>

<span data-ttu-id="6e23a-116">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="6e23a-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="6e23a-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e23a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e23a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e23a-118">Requirements</span></span>



| <span data-ttu-id="6e23a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e23a-119">Requirement</span></span> | <span data-ttu-id="6e23a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="6e23a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e23a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e23a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e23a-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="6e23a-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e23a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e23a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e23a-124">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="6e23a-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6e23a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e23a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e23a-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e23a-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e23a-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="6e23a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e23a-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e23a-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6e23a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e23a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e23a-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e23a-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6e23a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="6e23a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e23a-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e23a-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6e23a-133">IID</span><span class="sxs-lookup"><span data-stu-id="6e23a-133">IID</span></span><br/>                      | <span data-ttu-id="6e23a-134">IID_IBackgroundCopyFile5 é definido como 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="6e23a-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6e23a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e23a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e23a-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="6e23a-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="6e23a-137">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="6e23a-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





