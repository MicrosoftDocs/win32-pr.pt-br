---
title: Método IMsRdpClient8 SendRemoteAction
description: Faz com que uma ação seja executada na sessão remota.
ms.assetid: d6a43662-7e51-404a-a3f9-a8b51cbc69d1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SendRemoteAction
- Método SendRemoteAction Serviços de Área de Trabalho Remota, interface IMsRdpClient8
- Serviços de Área de Trabalho Remota de interface IMsRdpClient8, método SendRemoteAction
- Método SendRemoteAction Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SendRemoteAction
- Método SendRemoteAction Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método SendRemoteAction
topic_type:
- apiref
api_name:
- IMsRdpClient8.SendRemoteAction
- IMsRdpClient9.SendRemoteAction
- IMsRdpClient10.SendRemoteAction
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a28fc9695686402e0a8e98ed17fc1bc6a47939d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456008"
---
# <a name="imsrdpclient8sendremoteaction-method"></a><span data-ttu-id="33b18-110">Método IMsRdpClient8:: SendRemoteAction</span><span class="sxs-lookup"><span data-stu-id="33b18-110">IMsRdpClient8::SendRemoteAction method</span></span>

<span data-ttu-id="33b18-111">Faz com que uma ação seja executada na sessão remota.</span><span class="sxs-lookup"><span data-stu-id="33b18-111">Causes an action to be performed in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="33b18-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33b18-112">Syntax</span></span>


```C++
HRESULT SendRemoteAction(
  [in] RemoteSessionActionType actionType
);
```



## <a name="parameters"></a><span data-ttu-id="33b18-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33b18-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33b18-114">*ação de* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33b18-114">*actionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33b18-115">Um valor da enumeração [**RemoteSessionActionType**](remotesessionactiontype.md) que especifica a ação a ser enviada para a sessão remota.</span><span class="sxs-lookup"><span data-stu-id="33b18-115">A value of the [**RemoteSessionActionType**](remotesessionactiontype.md) enumeration that specifies the action to send to the remote session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33b18-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33b18-116">Return value</span></span>

<span data-ttu-id="33b18-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="33b18-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33b18-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33b18-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b18-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33b18-119">Requirements</span></span>



| <span data-ttu-id="33b18-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="33b18-120">Requirement</span></span> | <span data-ttu-id="33b18-121">Valor</span><span class="sxs-lookup"><span data-stu-id="33b18-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33b18-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33b18-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33b18-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="33b18-123">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="33b18-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33b18-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33b18-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33b18-125">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="33b18-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="33b18-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="33b18-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b18-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="33b18-128">DLL</span><span class="sxs-lookup"><span data-stu-id="33b18-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33b18-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33b18-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="33b18-130">IID</span><span class="sxs-lookup"><span data-stu-id="33b18-130">IID</span></span><br/>                      | <span data-ttu-id="33b18-131">IID \_ IMsRdpClient8 é definido como 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="33b18-131">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="33b18-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="33b18-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33b18-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="33b18-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="33b18-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="33b18-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="33b18-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="33b18-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





