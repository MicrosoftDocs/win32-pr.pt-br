---
title: Método método ibackgroundcopyjob EnumFiles (Deliveryoptimization. h)
description: Recupera um ponteiro de interface IEnumBackgroundCopyFiles que você usa para enumerar os arquivos em um trabalho.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Método EnumFiles
- Método EnumFiles, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085687"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="fa5d3-106">Método método ibackgroundcopyjob:: EnumFiles</span><span class="sxs-lookup"><span data-stu-id="fa5d3-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="fa5d3-107">Recupera um ponteiro de interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que você usa para enumerar os arquivos em um trabalho.</span><span class="sxs-lookup"><span data-stu-id="fa5d3-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5d3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa5d3-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="fa5d3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa5d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa5d3-110">*ppEnumFiles* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa5d3-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa5d3-111">Ponteiro de interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que você usa para enumerar os arquivos no trabalho.</span><span class="sxs-lookup"><span data-stu-id="fa5d3-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="fa5d3-112">Libere *ppEnumFiles* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="fa5d3-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa5d3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa5d3-113">Return value</span></span>

<span data-ttu-id="fa5d3-114">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="fa5d3-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5d3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa5d3-115">Requirements</span></span>



| <span data-ttu-id="fa5d3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa5d3-116">Requirement</span></span> | <span data-ttu-id="fa5d3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="fa5d3-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5d3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa5d3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fa5d3-119">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fa5d3-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa5d3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa5d3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fa5d3-121">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fa5d3-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fa5d3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa5d3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa5d3-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa5d3-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa5d3-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="fa5d3-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa5d3-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa5d3-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa5d3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa5d3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa5d3-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa5d3-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fa5d3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fa5d3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa5d3-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa5d3-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fa5d3-130">IID</span><span class="sxs-lookup"><span data-stu-id="fa5d3-130">IID</span></span><br/>                      | <span data-ttu-id="fa5d3-131">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="fa5d3-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fa5d3-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fa5d3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5d3-133">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="fa5d3-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="fa5d3-134">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="fa5d3-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





