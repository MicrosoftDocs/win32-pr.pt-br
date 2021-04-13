---
title: Método ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Define a taxa de bits armazenada em cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API de streaming de mídia do método SetCachedBitrateMeasurement
- API de streaming de mídia do método SetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455899"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="04a85-106">Método ActiveBasicDevice:: SetCachedBitrateMeasurement</span><span class="sxs-lookup"><span data-stu-id="04a85-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="04a85-107">Define a taxa de bits armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="04a85-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a85-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04a85-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="04a85-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04a85-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a85-110">*physicalNetworkInterface* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04a85-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a85-111">Especifica a interface de rede física.</span><span class="sxs-lookup"><span data-stu-id="04a85-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="04a85-112">*taxa de bits* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="04a85-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a85-113">O valor para o qual definir a taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="04a85-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a85-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04a85-114">Return value</span></span>

<span data-ttu-id="04a85-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="04a85-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04a85-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04a85-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a85-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04a85-117">Requirements</span></span>



| <span data-ttu-id="04a85-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a85-118">Requirement</span></span> | <span data-ttu-id="04a85-119">Valor</span><span class="sxs-lookup"><span data-stu-id="04a85-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a85-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04a85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04a85-121">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="04a85-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="04a85-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04a85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04a85-123">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="04a85-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="04a85-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04a85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="04a85-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="04a85-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="04a85-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="04a85-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04a85-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04a85-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="04a85-128">DLL</span><span class="sxs-lookup"><span data-stu-id="04a85-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04a85-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04a85-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a85-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="04a85-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="04a85-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="04a85-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

