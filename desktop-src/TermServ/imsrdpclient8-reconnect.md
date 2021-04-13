---
title: Método de reconexão do IMsRdpClient8
description: Reconecta-se à sessão remota com a nova largura e altura da área de trabalho.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método de reconexão
- Método reconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método reconnect
- Método reconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método reconnect
- Método reconnect Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método reconnect
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499848"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="e9857-110">Método IMsRdpClient8:: Reconnect</span><span class="sxs-lookup"><span data-stu-id="e9857-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="e9857-111">Reconecta-se à sessão remota com a nova largura e altura da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="e9857-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="e9857-112">O controle já deve estar conectado a uma sessão remota para que esse método tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="e9857-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9857-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9857-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="e9857-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9857-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9857-115">*ulWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9857-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9857-116">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="e9857-116">Type: **ULONG**</span></span>

<span data-ttu-id="e9857-117">A nova largura da área de trabalho, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e9857-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="e9857-118">Consulte a propriedade [**DesktopWidth**](imstscax-desktopwidth.md) para restrições de valor.</span><span class="sxs-lookup"><span data-stu-id="e9857-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="e9857-119">*ulHeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9857-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9857-120">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="e9857-120">Type: **ULONG**</span></span>

<span data-ttu-id="e9857-121">A nova altura da área de trabalho, em pixels.</span><span class="sxs-lookup"><span data-stu-id="e9857-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="e9857-122">Consulte a propriedade [**DesktopHeight**](imstscax-desktopheight.md) para restrições de valor.</span><span class="sxs-lookup"><span data-stu-id="e9857-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="e9857-123">*pReconnectStatus* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e9857-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e9857-124">Tipo: \**[**ControlReconnectStatus**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="e9857-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="e9857-125">Um ponteiro para uma variável [_ *ControlReconnectStatus* \*](controlreconnectstatus.md) que recebe o status da operação de reconexão.</span><span class="sxs-lookup"><span data-stu-id="e9857-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9857-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9857-126">Return value</span></span>

<span data-ttu-id="e9857-127">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e9857-127">Type: **HRESULT**</span></span>

<span data-ttu-id="e9857-128">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e9857-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9857-129">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e9857-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9857-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9857-130">Requirements</span></span>



| <span data-ttu-id="e9857-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9857-131">Requirement</span></span> | <span data-ttu-id="e9857-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e9857-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9857-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9857-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e9857-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9857-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="e9857-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9857-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e9857-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e9857-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="e9857-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e9857-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="e9857-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9857-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9857-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e9857-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9857-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9857-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9857-141">IID</span><span class="sxs-lookup"><span data-stu-id="e9857-141">IID</span></span><br/>                      | <span data-ttu-id="e9857-142">IID \_ IMsRdpClient8 é definido como 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="e9857-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e9857-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9857-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9857-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e9857-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e9857-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e9857-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e9857-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e9857-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="e9857-147">**ControlReconnectStatus**</span><span class="sxs-lookup"><span data-stu-id="e9857-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





