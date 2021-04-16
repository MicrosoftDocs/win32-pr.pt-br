---
title: Método IMsRdpClient9 attachEvent
description: Anexa um evento.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método attachEvent
- método attachEvent Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método attachEvent
- método attachEvent Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método attachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454655"
---
# <a name="imsrdpclient9attachevent-method"></a><span data-ttu-id="1aa5b-108">Método IMsRdpClient9:: attachEvent</span><span class="sxs-lookup"><span data-stu-id="1aa5b-108">IMsRdpClient9::attachEvent method</span></span>

<span data-ttu-id="1aa5b-109">Anexa um evento.</span><span class="sxs-lookup"><span data-stu-id="1aa5b-109">Attaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa5b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1aa5b-110">Syntax</span></span>


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="1aa5b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1aa5b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa5b-112">*eventoname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1aa5b-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa5b-113">O evento a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="1aa5b-113">The event to attach.</span></span>

</dd> <dt>

<span data-ttu-id="1aa5b-114">*retorno de chamada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1aa5b-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa5b-115">O retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="1aa5b-115">The callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa5b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1aa5b-116">Return value</span></span>

<span data-ttu-id="1aa5b-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1aa5b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1aa5b-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1aa5b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa5b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aa5b-119">Requirements</span></span>



| <span data-ttu-id="1aa5b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa5b-120">Requirement</span></span> | <span data-ttu-id="1aa5b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1aa5b-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa5b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa5b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1aa5b-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1aa5b-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1aa5b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1aa5b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1aa5b-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1aa5b-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="1aa5b-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1aa5b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1aa5b-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa5b-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="1aa5b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1aa5b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1aa5b-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aa5b-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="1aa5b-130">IID</span><span class="sxs-lookup"><span data-stu-id="1aa5b-130">IID</span></span><br/>                      | <span data-ttu-id="1aa5b-131">CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="1aa5b-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="1aa5b-132">CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="1aa5b-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="1aa5b-133">IID \_ IMsRdpClient9 é definido como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="1aa5b-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1aa5b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1aa5b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa5b-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="1aa5b-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="1aa5b-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1aa5b-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





