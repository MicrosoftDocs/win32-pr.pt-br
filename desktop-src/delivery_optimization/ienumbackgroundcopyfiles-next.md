---
title: Método Next IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera um número especificado de itens na sequência de enumeração. Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Próximo método
- Método Next, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, próximo método
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918926"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="8d155-107">Método IEnumBackgroundCopyFiles:: Next</span><span class="sxs-lookup"><span data-stu-id="8d155-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="8d155-108">Recupera um número especificado de itens na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="8d155-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="8d155-109">Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.</span><span class="sxs-lookup"><span data-stu-id="8d155-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d155-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d155-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="8d155-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d155-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d155-112">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d155-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d155-113">Número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="8d155-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="8d155-114">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d155-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d155-115">Matriz de objetos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="8d155-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="8d155-116">Você deve liberar cada objeto em *rgelt* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="8d155-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="8d155-117">*pceltFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8d155-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d155-118">Número de elementos retornados em *rgelt*.</span><span class="sxs-lookup"><span data-stu-id="8d155-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="8d155-119">Você pode definir *pceltFetched* como **NULL** se *celt* for um.</span><span class="sxs-lookup"><span data-stu-id="8d155-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="8d155-120">Caso contrário, inicialize o valor de *pceltFetched* como 0 antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="8d155-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d155-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d155-121">Return value</span></span>

<span data-ttu-id="8d155-122">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="8d155-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="8d155-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8d155-123">Return code</span></span>                                                                              | <span data-ttu-id="8d155-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d155-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d155-125"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8d155-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="8d155-126">O número de elementos solicitados foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8d155-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="8d155-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="8d155-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="8d155-128">Retornou menos que o número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="8d155-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="8d155-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d155-129">Requirements</span></span>



| <span data-ttu-id="8d155-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d155-130">Requirement</span></span> | <span data-ttu-id="8d155-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8d155-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d155-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d155-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8d155-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="8d155-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8d155-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d155-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8d155-135">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="8d155-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8d155-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d155-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d155-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d155-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d155-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="8d155-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d155-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d155-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8d155-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d155-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d155-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d155-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8d155-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8d155-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d155-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d155-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8d155-144">IID</span><span class="sxs-lookup"><span data-stu-id="8d155-144">IID</span></span><br/>                      | <span data-ttu-id="8d155-145">IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="8d155-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8d155-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d155-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d155-147">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="8d155-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





