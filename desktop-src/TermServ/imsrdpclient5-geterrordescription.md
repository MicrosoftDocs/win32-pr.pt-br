---
title: Método IMsRdpClient5 GetErrorDescription
description: Recupera a descrição do erro para os eventos de desconexão de sessão.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient5
- Serviços de Área de Trabalho Remota de interface IMsRdpClient5, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient6
- Serviços de Área de Trabalho Remota de interface IMsRdpClient6, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient7
- Serviços de Área de Trabalho Remota de interface IMsRdpClient7, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método GetErrorDescription
- Método GetErrorDescription Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369874"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="3f7bf-116">Método IMsRdpClient5:: GetErrorDescription</span><span class="sxs-lookup"><span data-stu-id="3f7bf-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="3f7bf-117">Recupera a descrição do erro para os eventos de desconexão de sessão.</span><span class="sxs-lookup"><span data-stu-id="3f7bf-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f7bf-118">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f7bf-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="3f7bf-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f7bf-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7bf-120">*disconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f7bf-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7bf-121">O motivo da desconexão.</span><span class="sxs-lookup"><span data-stu-id="3f7bf-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="3f7bf-122">*extendedDisconnectReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3f7bf-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7bf-123">Fornece informações detalhadas sobre por que uma desconexão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="3f7bf-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="3f7bf-124">*pBstrErrorMsg* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f7bf-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f7bf-125">Um ponteiro para uma variável **BSTR** que recebe o texto da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="3f7bf-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7bf-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f7bf-126">Return value</span></span>

<span data-ttu-id="3f7bf-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3f7bf-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7bf-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f7bf-128">Requirements</span></span>



| <span data-ttu-id="3f7bf-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f7bf-129">Requirement</span></span> | <span data-ttu-id="3f7bf-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3f7bf-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7bf-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f7bf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7bf-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f7bf-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3f7bf-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f7bf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7bf-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f7bf-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3f7bf-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3f7bf-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f7bf-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7bf-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f7bf-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3f7bf-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f7bf-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f7bf-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f7bf-139">IID</span><span class="sxs-lookup"><span data-stu-id="3f7bf-139">IID</span></span><br/>                      | <span data-ttu-id="3f7bf-140">IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="3f7bf-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3f7bf-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f7bf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f7bf-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3f7bf-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3f7bf-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3f7bf-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3f7bf-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3f7bf-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3f7bf-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3f7bf-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3f7bf-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3f7bf-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3f7bf-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3f7bf-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





