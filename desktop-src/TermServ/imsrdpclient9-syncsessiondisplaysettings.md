---
title: Método IMsRdpClient9 SyncSessionDisplaySettings
description: Sincroniza as configurações de exibição da sessão.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SyncSessionDisplaySettings
- Método SyncSessionDisplaySettings Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SyncSessionDisplaySettings
- Método SyncSessionDisplaySettings Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método SyncSessionDisplaySettings
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918005"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a><span data-ttu-id="7131f-108">Método IMsRdpClient9:: SyncSessionDisplaySettings</span><span class="sxs-lookup"><span data-stu-id="7131f-108">IMsRdpClient9::SyncSessionDisplaySettings method</span></span>

<span data-ttu-id="7131f-109">Sincroniza as configurações de exibição da sessão.</span><span class="sxs-lookup"><span data-stu-id="7131f-109">Synchronizes session display settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="7131f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7131f-110">Syntax</span></span>


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a><span data-ttu-id="7131f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7131f-111">Parameters</span></span>

<span data-ttu-id="7131f-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7131f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7131f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7131f-113">Return value</span></span>

<span data-ttu-id="7131f-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7131f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7131f-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7131f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7131f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7131f-116">Requirements</span></span>



| <span data-ttu-id="7131f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7131f-117">Requirement</span></span> | <span data-ttu-id="7131f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7131f-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7131f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7131f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7131f-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7131f-120">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7131f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7131f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7131f-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7131f-122">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="7131f-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7131f-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7131f-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7131f-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="7131f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7131f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7131f-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7131f-126"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="7131f-127">IID</span><span class="sxs-lookup"><span data-stu-id="7131f-127">IID</span></span><br/>                      | <span data-ttu-id="7131f-128">CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="7131f-128">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="7131f-129">CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="7131f-129">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="7131f-130">IID \_ IMsRdpClient9 é definido como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="7131f-130">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7131f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="7131f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7131f-132">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7131f-132">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7131f-133">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="7131f-133">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





