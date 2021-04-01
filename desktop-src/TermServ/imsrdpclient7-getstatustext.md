---
title: Método IMsRdpClient7 GetStatusText (OpenService. h)
description: Recupera o texto de status do código de status especificado.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método GetStatusText
- Método GetStatusText Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644810"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="b910d-112">Método IMsRdpClient7:: GetStatusText</span><span class="sxs-lookup"><span data-stu-id="b910d-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="b910d-113">Recupera o texto de status do código de status especificado.</span><span class="sxs-lookup"><span data-stu-id="b910d-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b910d-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b910d-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="b910d-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b910d-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b910d-116">*StatusCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b910d-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b910d-117">Um **uint** que especifica o código de status para o qual recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="b910d-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="b910d-118">*pBstrStatusText* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b910d-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b910d-119">O endereço de um **BSTR** que recebe o texto de status.</span><span class="sxs-lookup"><span data-stu-id="b910d-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b910d-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b910d-120">Return value</span></span>

<span data-ttu-id="b910d-121">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b910d-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b910d-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b910d-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b910d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b910d-123">Requirements</span></span>



| <span data-ttu-id="b910d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b910d-124">Requirement</span></span> | <span data-ttu-id="b910d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b910d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b910d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b910d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b910d-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b910d-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="b910d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b910d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b910d-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b910d-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b910d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b910d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b910d-131"><dt>OpenService. h</dt></span><span class="sxs-lookup"><span data-stu-id="b910d-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="b910d-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b910d-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="b910d-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b910d-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b910d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b910d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b910d-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b910d-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="b910d-136">IID</span><span class="sxs-lookup"><span data-stu-id="b910d-136">IID</span></span><br/>                      | <span data-ttu-id="b910d-137">IID \_ IMsRdpClient7 é definido como b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="b910d-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="b910d-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="b910d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b910d-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="b910d-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="b910d-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="b910d-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="b910d-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b910d-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="b910d-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b910d-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





