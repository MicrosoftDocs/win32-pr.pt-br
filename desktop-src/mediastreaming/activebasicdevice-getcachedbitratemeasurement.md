---
title: Método ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Obtém a taxa de bits armazenada em cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API de streaming de mídia do método GetCachedBitrateMeasurement
- API de streaming de mídia do método GetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499682"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="c980a-106">Método ActiveBasicDevice:: GetCachedBitrateMeasurement</span><span class="sxs-lookup"><span data-stu-id="c980a-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="c980a-107">Obtém a taxa de bits armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="c980a-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="c980a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c980a-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="c980a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c980a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c980a-110">*physicalNetworkInterface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c980a-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c980a-111">Especifica a interface de rede física.</span><span class="sxs-lookup"><span data-stu-id="c980a-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="c980a-112">*taxa de bits* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c980a-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c980a-113">Recebe o valor de taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="c980a-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c980a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c980a-114">Return value</span></span>

<span data-ttu-id="c980a-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c980a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c980a-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c980a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c980a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c980a-117">Requirements</span></span>



| <span data-ttu-id="c980a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c980a-118">Requirement</span></span> | <span data-ttu-id="c980a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c980a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c980a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c980a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c980a-121">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c980a-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c980a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c980a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c980a-123">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="c980a-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c980a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c980a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c980a-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c980a-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="c980a-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="c980a-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c980a-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c980a-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="c980a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c980a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c980a-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c980a-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c980a-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c980a-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="c980a-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c980a-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

