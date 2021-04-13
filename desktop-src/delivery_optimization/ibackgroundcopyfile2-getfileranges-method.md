---
title: Método IBackgroundCopyFile2 GetFileRanges (Deliveryoptimization. h)
description: Recupera os intervalos que você deseja baixar do arquivo remoto.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Método GetFileRanges
- Método GetFileRanges, interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, método GetFileRanges
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369543"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="cd3a1-106">Método IBackgroundCopyFile2:: GetFileRanges</span><span class="sxs-lookup"><span data-stu-id="cd3a1-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="cd3a1-107">Recupera os intervalos que você deseja baixar do arquivo remoto.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3a1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd3a1-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="cd3a1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd3a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd3a1-110">*RangeCount* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cd3a1-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3a1-111">Número de elementos em *intervalos*.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="cd3a1-112">*Intervalos* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="cd3a1-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3a1-113">Matriz de estruturas de [**BG_FILE_RANGE**](bg-file-range.md) que especificam os intervalos a serem baixados.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="cd3a1-114">Quando terminar, chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para *intervalos* gratuitos.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd3a1-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cd3a1-115">Return value</span></span>

<span data-ttu-id="cd3a1-116">Esse método retorna os seguintes valores de retorno, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="cd3a1-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cd3a1-117">Return code</span></span>                                                                              | <span data-ttu-id="cd3a1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd3a1-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cd3a1-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="cd3a1-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="cd3a1-120">Sucesso</span><span class="sxs-lookup"><span data-stu-id="cd3a1-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="cd3a1-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="cd3a1-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="cd3a1-122">Nenhum intervalo foi especificado ou o trabalho é um trabalho de upload ou de resposta de upload.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="cd3a1-123">*RangeCount* é definido como zero e os *intervalos* são definidos como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cd3a1-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cd3a1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd3a1-124">Requirements</span></span>



| <span data-ttu-id="cd3a1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd3a1-125">Requirement</span></span> | <span data-ttu-id="cd3a1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cd3a1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3a1-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd3a1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3a1-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="cd3a1-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd3a1-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd3a1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3a1-130">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="cd3a1-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cd3a1-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd3a1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd3a1-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd3a1-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd3a1-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="cd3a1-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd3a1-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd3a1-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="cd3a1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd3a1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd3a1-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd3a1-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="cd3a1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cd3a1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd3a1-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd3a1-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="cd3a1-139">IID</span><span class="sxs-lookup"><span data-stu-id="cd3a1-139">IID</span></span><br/>                      | <span data-ttu-id="cd3a1-140">IID_IBackgroundCopyFile2 é definido como 83e81b93-0873-474D-8a8c-f2018b1a939c</span><span class="sxs-lookup"><span data-stu-id="cd3a1-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="cd3a1-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd3a1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3a1-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="cd3a1-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="cd3a1-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="cd3a1-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

