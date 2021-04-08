---
title: Método IMsRdpDeviceCollection2 RedirectNow
description: Força os dispositivos que foram selecionados ou desmarcados da coleção a serem redirecionados ou removidos.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RedirectNow
- Método RedirectNow Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection2, método RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918002"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="e4927-106">Método IMsRdpDeviceCollection2:: RedirectNow</span><span class="sxs-lookup"><span data-stu-id="e4927-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="e4927-107">Força os dispositivos que foram selecionados ou desmarcados da coleção a serem redirecionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="e4927-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4927-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4927-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="e4927-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4927-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4927-110">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="e4927-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4927-111">Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="e4927-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="e4927-112">Um valor da enumeração [**RedirectDeviceType**](redirectdevicetype.md) que especifica o tipo de dispositivo a ser redirecionado.</span><span class="sxs-lookup"><span data-stu-id="e4927-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4927-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4927-113">Return value</span></span>

<span data-ttu-id="e4927-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e4927-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e4927-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e4927-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4927-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4927-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4927-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4927-117">Requirements</span></span>



| <span data-ttu-id="e4927-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4927-118">Requirement</span></span> | <span data-ttu-id="e4927-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e4927-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4927-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4927-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e4927-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e4927-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="e4927-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4927-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e4927-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4927-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="e4927-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e4927-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4927-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4927-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e4927-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e4927-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4927-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4927-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4927-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4927-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4927-129">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="e4927-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="e4927-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="e4927-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





