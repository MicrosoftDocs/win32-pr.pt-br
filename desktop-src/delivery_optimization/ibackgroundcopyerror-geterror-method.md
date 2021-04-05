---
title: Método GetError IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera o código de erro e identifica o contexto no qual o erro ocorreu.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Método GetError
- Método GetError, interface IBackgroundCopyError
- Interface IBackgroundCopyError, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918358"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="e7279-106">Método IBackgroundCopyError:: GetError</span><span class="sxs-lookup"><span data-stu-id="e7279-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="e7279-107">Recupera o código de erro e identifica o contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e7279-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7279-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7279-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="e7279-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7279-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7279-110">*pContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7279-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7279-111">Contexto no qual o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e7279-111">Context in which the error occurred.</span></span> <span data-ttu-id="e7279-112">Para obter uma lista de valores de contexto, consulte a enumeração [**BG_ERROR_CONTEXT**](bg-error-context.md) .</span><span class="sxs-lookup"><span data-stu-id="e7279-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e7279-113">*pErrorCode* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7279-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7279-114">Código de erro do erro que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="e7279-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7279-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7279-115">Return value</span></span>

<span data-ttu-id="e7279-116">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com HRESULT em erro.</span><span class="sxs-lookup"><span data-stu-id="e7279-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7279-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7279-117">Requirements</span></span>



| <span data-ttu-id="e7279-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7279-118">Requirement</span></span> | <span data-ttu-id="e7279-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e7279-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7279-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7279-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e7279-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e7279-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e7279-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7279-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e7279-123">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="e7279-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e7279-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7279-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7279-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7279-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7279-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="e7279-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7279-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7279-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e7279-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7279-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7279-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7279-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e7279-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e7279-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7279-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7279-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e7279-132">IID</span><span class="sxs-lookup"><span data-stu-id="e7279-132">IID</span></span><br/>                      | <span data-ttu-id="e7279-133">IID_IBackgroundCopyError é definido como 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="e7279-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e7279-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7279-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7279-135">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="e7279-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="e7279-136">**IBackgroundCopyError:: GetFile**</span><span class="sxs-lookup"><span data-stu-id="e7279-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





