---
title: Método IMsRdpClient9 detachEvent
description: Desanexa um evento.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método detachEvent
- método detachEvent Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método detachEvent
- método detachEvent Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método detachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085193"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="1b7ea-108">IMsRdpClient9: método etachEvent de:d</span><span class="sxs-lookup"><span data-stu-id="1b7ea-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="1b7ea-109">Desanexa um evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ea-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7ea-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b7ea-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="1b7ea-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b7ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7ea-112">*eventoname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b7ea-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ea-113">O nome do evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ea-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="1b7ea-114">*retorno de chamada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b7ea-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7ea-115">O retorno de chamada associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="1b7ea-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7ea-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b7ea-116">Return value</span></span>

<span data-ttu-id="1b7ea-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1b7ea-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b7ea-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b7ea-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7ea-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b7ea-119">Requirements</span></span>



| <span data-ttu-id="1b7ea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b7ea-120">Requirement</span></span> | <span data-ttu-id="1b7ea-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1b7ea-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7ea-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b7ea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1b7ea-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1b7ea-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b7ea-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b7ea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1b7ea-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1b7ea-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="1b7ea-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1b7ea-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1b7ea-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ea-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="1b7ea-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1b7ea-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b7ea-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b7ea-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="1b7ea-130">IID</span><span class="sxs-lookup"><span data-stu-id="1b7ea-130">IID</span></span><br/>                      | <span data-ttu-id="1b7ea-131">CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="1b7ea-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="1b7ea-132">CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="1b7ea-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="1b7ea-133">IID \_ IMsRdpClient9 é definido como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="1b7ea-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b7ea-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b7ea-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7ea-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="1b7ea-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="1b7ea-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1b7ea-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





