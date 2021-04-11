---
title: Método GetProgress do IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera informações sobre o progresso da transferência de arquivo.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Método GetProgress
- Método GetProgress, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, método GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455032"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="8bf89-106">Método IBackgroundCopyFile:: GetProgress</span><span class="sxs-lookup"><span data-stu-id="8bf89-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="8bf89-107">Recupera informações sobre o progresso da transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8bf89-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf89-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bf89-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="8bf89-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bf89-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf89-110">*pProgress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8bf89-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bf89-111">Estrutura cujos membros indicam o progresso da transferência de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8bf89-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="8bf89-112">Para obter detalhes sobre o tipo de informações de progresso disponíveis, consulte a estrutura de [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf89-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf89-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8bf89-113">Return value</span></span>

<span data-ttu-id="8bf89-114">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="8bf89-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf89-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf89-115">Requirements</span></span>



| <span data-ttu-id="8bf89-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf89-116">Requirement</span></span> | <span data-ttu-id="8bf89-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8bf89-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf89-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf89-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf89-119">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="8bf89-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8bf89-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf89-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf89-121">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="8bf89-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8bf89-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8bf89-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf89-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf89-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bf89-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="8bf89-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bf89-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bf89-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8bf89-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8bf89-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8bf89-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8bf89-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8bf89-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf89-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf89-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bf89-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8bf89-130">IID</span><span class="sxs-lookup"><span data-stu-id="8bf89-130">IID</span></span><br/>                      | <span data-ttu-id="8bf89-131">IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="8bf89-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="8bf89-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bf89-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf89-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="8bf89-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="8bf89-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="8bf89-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="8bf89-135">**Método ibackgroundcopyjob:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="8bf89-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





