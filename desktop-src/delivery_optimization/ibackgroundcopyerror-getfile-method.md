---
title: Método GetFile IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Método GetFile
- Método GetFile, interface IBackgroundCopyError
- Interface IBackgroundCopyError, método GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105795466"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="9f06f-106">Método IBackgroundCopyError:: GetFile</span><span class="sxs-lookup"><span data-stu-id="9f06f-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="9f06f-107">Recupera um ponteiro de interface para o objeto de arquivo associado ao erro.</span><span class="sxs-lookup"><span data-stu-id="9f06f-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f06f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f06f-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="9f06f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f06f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f06f-110">*ppFile* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9f06f-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f06f-111">Um ponteiro de interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) cujos métodos você usa para determinar os nomes de arquivo local e remoto associados ao erro.</span><span class="sxs-lookup"><span data-stu-id="9f06f-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="9f06f-112">O parâmetro *ppFile* será definido como **NULL** se o erro não estiver associado ao arquivo local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="9f06f-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="9f06f-113">Quando terminar, libere *ppFile*.</span><span class="sxs-lookup"><span data-stu-id="9f06f-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f06f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f06f-114">Return value</span></span>

<span data-ttu-id="9f06f-115">Esse método retorna os valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="9f06f-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="9f06f-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9f06f-116">Return code</span></span>                                                                                                | <span data-ttu-id="9f06f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f06f-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f06f-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9f06f-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="9f06f-119">Um ponteiro de interface foi recuperado com êxito para o objeto de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f06f-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="9f06f-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="9f06f-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="9f06f-121">O erro não está associado a um arquivo local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="9f06f-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="9f06f-122">O parâmetro *ppFile* está definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9f06f-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9f06f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f06f-123">Requirements</span></span>



| <span data-ttu-id="9f06f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f06f-124">Requirement</span></span> | <span data-ttu-id="9f06f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9f06f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f06f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f06f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9f06f-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="9f06f-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9f06f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f06f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9f06f-129">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="9f06f-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9f06f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f06f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f06f-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f06f-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f06f-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="9f06f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f06f-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f06f-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f06f-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f06f-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f06f-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f06f-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9f06f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9f06f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f06f-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f06f-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9f06f-138">IID</span><span class="sxs-lookup"><span data-stu-id="9f06f-138">IID</span></span><br/>                      | <span data-ttu-id="9f06f-139">IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="9f06f-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="9f06f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f06f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f06f-141">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="9f06f-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="9f06f-142">**IBackgroundCopyError:: GetError**</span><span class="sxs-lookup"><span data-stu-id="9f06f-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





