---
title: Método SendKeys IMsRdpClientNonScriptable
description: Envia uma série de pressionamentos de teclas para o controle. Os pressionamentos de tecla estão no formato de código de digitalização, que são os dados de teclado das chaves físicas reais.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Método SendKeys Serviços de Área de Trabalho Remota
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, método SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455496"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="cf3ac-115">Método IMsRdpClientNonScriptable:: SendKeys</span><span class="sxs-lookup"><span data-stu-id="cf3ac-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="cf3ac-116">Envia uma série de pressionamentos de teclas para o controle.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="cf3ac-117">Os pressionamentos de tecla estão no formato de código de digitalização, que são os dados de teclado das chaves físicas reais.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf3ac-118">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf3ac-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="cf3ac-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf3ac-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf3ac-120">*numKeys* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cf3ac-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf3ac-121">O número de pressionamentos de teclas a serem enviados.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-121">The number of keystrokes to send.</span></span> <span data-ttu-id="cf3ac-122">O número máximo de chaves que podem ser enviadas em uma operação é 20.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="cf3ac-123">O método retornará **E \_ INVALIDARG** se esse parâmetro for maior que 20.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="cf3ac-124">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="cf3ac-125">*pbArrayKeyUp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cf3ac-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf3ac-126">Uma matriz cujo tamanho é igual a *numKeys*.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="cf3ac-127">Um elemento será **true** se a chave correspondente for up e **false** se a chave correspondente estiver inoperante.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="cf3ac-128">*plKeyData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cf3ac-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf3ac-129">Uma matriz cujo tamanho é igual a *numKeys*.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="cf3ac-130">A matriz contém dados de pressionamento de tecla e corresponde ao valor do parâmetro *lParam* da mensagem [ \_ KEYDOWN do WM](../inputdev/wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="cf3ac-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="cf3ac-131">Os dados especificam a contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="cf3ac-132">Para obter uma descrição dos bits nessa matriz, consulte o [WM \_ KEYDOWN](../inputdev/wm-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="cf3ac-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="cf3ac-133">O elemento correspondente em *pbArrayKeyUp* indica se a chave está para cima ou para baixo.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf3ac-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf3ac-134">Return value</span></span>

<span data-ttu-id="cf3ac-135">Retornar **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf3ac-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf3ac-136">Remarks</span></span>

<span data-ttu-id="cf3ac-137">O método **SendKeys** não mistura pressionamentos de teclas feitos pelo usuário local com pressionamentos de teclas que o método está enviando.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="cf3ac-138">Todos os pressionamentos de teclas passados para o método são enviados para a sessão remota em uma única sequência atômica.</span><span class="sxs-lookup"><span data-stu-id="cf3ac-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="cf3ac-139">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cf3ac-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf3ac-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf3ac-140">Requirements</span></span>



| <span data-ttu-id="cf3ac-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf3ac-141">Requirement</span></span> | <span data-ttu-id="cf3ac-142">Valor</span><span class="sxs-lookup"><span data-stu-id="cf3ac-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3ac-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf3ac-143">Minimum supported client</span></span><br/> | <span data-ttu-id="cf3ac-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf3ac-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="cf3ac-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf3ac-145">Minimum supported server</span></span><br/> | <span data-ttu-id="cf3ac-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf3ac-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="cf3ac-147">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cf3ac-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf3ac-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf3ac-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="cf3ac-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cf3ac-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf3ac-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf3ac-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="cf3ac-151">IID</span><span class="sxs-lookup"><span data-stu-id="cf3ac-151">IID</span></span><br/>                      | <span data-ttu-id="cf3ac-152">IID \_ IMsRdpClientNonScriptable é definido como 2f079c4c-87b2-4AFD-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="cf3ac-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf3ac-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf3ac-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3ac-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="cf3ac-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="cf3ac-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="cf3ac-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="cf3ac-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="cf3ac-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="cf3ac-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="cf3ac-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="cf3ac-158">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="cf3ac-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="cf3ac-159">o WM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="cf3ac-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

