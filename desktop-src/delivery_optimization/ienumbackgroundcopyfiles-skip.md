---
title: Método IEnumBackgroundCopyFiles Skip (Deliveryoptimization. h)
description: Ignora o próximo número especificado de elementos na sequência de enumeração. Se houver menos elementos à esquerda na sequência do que o número solicitado de elementos a serem ignorados, ele ignorará o último elemento na sequência.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Método Skip
- Método Skip, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, método Skip
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009012"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="006e5-107">Método IEnumBackgroundCopyFiles:: Skip</span><span class="sxs-lookup"><span data-stu-id="006e5-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="006e5-108">Ignora o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="006e5-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="006e5-109">Se houver menos elementos à esquerda na sequência do que o número solicitado de elementos a serem ignorados, ele ignorará o último elemento na sequência.</span><span class="sxs-lookup"><span data-stu-id="006e5-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="006e5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="006e5-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="006e5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="006e5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="006e5-112">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="006e5-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="006e5-113">Número de elementos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="006e5-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="006e5-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="006e5-114">Return value</span></span>

<span data-ttu-id="006e5-115">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="006e5-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="006e5-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="006e5-116">Return code</span></span>                                                                              | <span data-ttu-id="006e5-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="006e5-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="006e5-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="006e5-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="006e5-119">O número de elementos solicitados foi ignorado com êxito.</span><span class="sxs-lookup"><span data-stu-id="006e5-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="006e5-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="006e5-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="006e5-121">Ignorado menos que o número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="006e5-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="006e5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="006e5-122">Requirements</span></span>



| <span data-ttu-id="006e5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="006e5-123">Requirement</span></span> | <span data-ttu-id="006e5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="006e5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="006e5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="006e5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="006e5-126">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="006e5-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="006e5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="006e5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="006e5-128">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="006e5-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="006e5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="006e5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="006e5-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="006e5-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="006e5-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="006e5-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="006e5-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="006e5-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="006e5-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="006e5-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="006e5-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="006e5-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="006e5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="006e5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="006e5-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="006e5-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="006e5-137">IID</span><span class="sxs-lookup"><span data-stu-id="006e5-137">IID</span></span><br/>                      | <span data-ttu-id="006e5-138">IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="006e5-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="006e5-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="006e5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006e5-140">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="006e5-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





