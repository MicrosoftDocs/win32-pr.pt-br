---
title: Método AddFile IDeliveryOptimizationJob2
description: O método AddFile adiciona um único arquivo a um trabalho existente DO.
keywords:
- Método AddFile
- Método AddFile, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, método AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085346"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="64172-106">Método IDeliveryOptimizationJob2:: AddFileWithRanges</span><span class="sxs-lookup"><span data-stu-id="64172-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="64172-107">O método AddFile adiciona um único arquivo a um trabalho existente DO.</span><span class="sxs-lookup"><span data-stu-id="64172-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="64172-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64172-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="64172-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64172-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64172-110">*FileID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64172-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64172-111">A cadeia de caracteres de ID de arquivo, que identifica exclusivamente o arquivo a ser baixado.</span><span class="sxs-lookup"><span data-stu-id="64172-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="64172-112">*remoteUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64172-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64172-113">A URL do arquivo que tentará se conectar para baixar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="64172-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="64172-114">*rangeCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64172-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64172-115">O número de itens contidos em *intervalos*.</span><span class="sxs-lookup"><span data-stu-id="64172-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="64172-116">Um valor zero significa que nenhum intervalo é usado para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="64172-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="64172-117">*intervalos* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="64172-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64172-118">A lista de intervalos opcionais.</span><span class="sxs-lookup"><span data-stu-id="64172-118">The optional range list.</span></span> <span data-ttu-id="64172-119">Cada intervalo na lista é uma estrutura de [**BG_FILE_RANGE**](bg-file-range.md) .</span><span class="sxs-lookup"><span data-stu-id="64172-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="64172-120">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64172-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64172-121">O tipo de objeto contido no objeto.</span><span class="sxs-lookup"><span data-stu-id="64172-121">The type of object contained in object.</span></span> <span data-ttu-id="64172-122">Isso deve ser pelo tipo IID_IDeliveryOptimizationFile.</span><span class="sxs-lookup"><span data-stu-id="64172-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="64172-123">*objeto* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="64172-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64172-124">O objeto IDeliveryOptimizationFile, que representa o arquivo de download.</span><span class="sxs-lookup"><span data-stu-id="64172-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64172-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64172-125">Return value</span></span>

<span data-ttu-id="64172-126">Esse método retorna S_OK em caso de êxito ou um dos valores de HRESULT padrão em caso de erro.</span><span class="sxs-lookup"><span data-stu-id="64172-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="64172-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64172-127">Requirements</span></span>

| <span data-ttu-id="64172-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="64172-128">Requirement</span></span> | <span data-ttu-id="64172-129">Valor</span><span class="sxs-lookup"><span data-stu-id="64172-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="64172-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64172-130">Minimum supported client</span></span>  | <span data-ttu-id="64172-131">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="64172-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="64172-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64172-132">Minimum supported server</span></span>  | <span data-ttu-id="64172-133">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="64172-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="64172-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64172-134">Header</span></span>                    | <span data-ttu-id="64172-135">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="64172-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="64172-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="64172-136">IDL</span></span>                       | <span data-ttu-id="64172-137">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="64172-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="64172-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64172-138">Library</span></span>                   | <span data-ttu-id="64172-139">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="64172-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="64172-140">DLL</span><span class="sxs-lookup"><span data-stu-id="64172-140">DLL</span></span>                       | <span data-ttu-id="64172-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="64172-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="64172-142">IID</span><span class="sxs-lookup"><span data-stu-id="64172-142">IID</span></span>                       | <span data-ttu-id="64172-143">IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="64172-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="64172-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="64172-144">See also</span></span>

[<span data-ttu-id="64172-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="64172-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
