---
title: Método SetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Define uma propriedade genérica de uma transferência de arquivo de otimização de entrega.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- Método SetProperty
- Método SetProperty, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918356"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="16043-106">Método IBackgroundCopyFile5:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="16043-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="16043-107">Define uma propriedade genérica de uma transferência de arquivo de otimização de entrega.</span><span class="sxs-lookup"><span data-stu-id="16043-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="16043-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16043-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="16043-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16043-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16043-110">*PropertyId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="16043-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16043-111">Especifica a propriedade a ser definida.</span><span class="sxs-lookup"><span data-stu-id="16043-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="16043-112">*ProertyValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="16043-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16043-113">Um ponteiro para uma União que especifica o valor a ser definido.</span><span class="sxs-lookup"><span data-stu-id="16043-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="16043-114">O membro de União apropriado para a ID de propriedade é usado.</span><span class="sxs-lookup"><span data-stu-id="16043-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16043-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="16043-115">Return value</span></span>

<span data-ttu-id="16043-116">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="16043-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="16043-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="16043-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16043-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16043-118">Requirements</span></span>



| <span data-ttu-id="16043-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16043-119">Requirement</span></span> | <span data-ttu-id="16043-120">Valor</span><span class="sxs-lookup"><span data-stu-id="16043-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16043-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16043-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16043-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="16043-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="16043-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16043-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16043-124">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="16043-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="16043-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16043-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16043-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="16043-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="16043-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="16043-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="16043-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="16043-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="16043-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="16043-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="16043-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="16043-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="16043-131">DLL</span><span class="sxs-lookup"><span data-stu-id="16043-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16043-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16043-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="16043-133">IID</span><span class="sxs-lookup"><span data-stu-id="16043-133">IID</span></span><br/>                      | <span data-ttu-id="16043-134">IID_IBackgroundCopyFile5 é definido como 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="16043-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="16043-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="16043-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16043-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="16043-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="16043-137">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="16043-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





