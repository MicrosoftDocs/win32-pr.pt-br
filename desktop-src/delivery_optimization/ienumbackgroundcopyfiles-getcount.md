---
title: Método GetCount IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera uma contagem do número de arquivos na enumeração.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- Método GetCount
- Método GetCount, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, método GetCount
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644642"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="a52d6-106">Método IEnumBackgroundCopyFiles:: GetCount</span><span class="sxs-lookup"><span data-stu-id="a52d6-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="a52d6-107">Recupera uma contagem do número de arquivos na enumeração.</span><span class="sxs-lookup"><span data-stu-id="a52d6-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a52d6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a52d6-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="a52d6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a52d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a52d6-110">*pCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a52d6-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a52d6-111">Número de arquivos na enumeração.</span><span class="sxs-lookup"><span data-stu-id="a52d6-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a52d6-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a52d6-112">Return value</span></span>

<span data-ttu-id="a52d6-113">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="a52d6-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a52d6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a52d6-114">Requirements</span></span>



| <span data-ttu-id="a52d6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52d6-115">Requirement</span></span> | <span data-ttu-id="a52d6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a52d6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a52d6-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a52d6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a52d6-118">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a52d6-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a52d6-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a52d6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a52d6-120">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a52d6-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a52d6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a52d6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a52d6-122"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a52d6-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a52d6-123">INSERI</span><span class="sxs-lookup"><span data-stu-id="a52d6-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a52d6-124"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a52d6-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a52d6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a52d6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="a52d6-126"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a52d6-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a52d6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a52d6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a52d6-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a52d6-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a52d6-129">IID</span><span class="sxs-lookup"><span data-stu-id="a52d6-129">IID</span></span><br/>                      | <span data-ttu-id="a52d6-130">IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="a52d6-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="a52d6-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a52d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a52d6-132">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="a52d6-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





