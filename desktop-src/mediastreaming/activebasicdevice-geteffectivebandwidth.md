---
title: Método ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Obtém a largura de banda efetiva atual do dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API de streaming de mídia do método GetEffectiveBandwidth
- API de streaming de mídia do método GetEffectiveBandwidth, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009719"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="b718a-106">Método ActiveBasicDevice:: GetEffectiveBandwidth</span><span class="sxs-lookup"><span data-stu-id="b718a-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="b718a-107">Obtém a largura de banda efetiva atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b718a-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="b718a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b718a-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="b718a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b718a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b718a-110">*transmitSpeed* \[ no, retval\]</span><span class="sxs-lookup"><span data-stu-id="b718a-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b718a-111">Especifica se a velocidade de transmissão é recuperada ou se a velocidade de recebimento é recuperada.</span><span class="sxs-lookup"><span data-stu-id="b718a-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="b718a-112">**true** para recuperar a velocidade de transmissão.</span><span class="sxs-lookup"><span data-stu-id="b718a-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="b718a-113">**false** para recuperar a velocidade de recebimento.</span><span class="sxs-lookup"><span data-stu-id="b718a-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="b718a-114">*currentSpeed* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b718a-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b718a-115">Recebe a largura de banda efetiva atual.</span><span class="sxs-lookup"><span data-stu-id="b718a-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b718a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b718a-116">Return value</span></span>

<span data-ttu-id="b718a-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b718a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b718a-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b718a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b718a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b718a-119">Requirements</span></span>



| <span data-ttu-id="b718a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b718a-120">Requirement</span></span> | <span data-ttu-id="b718a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b718a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b718a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b718a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b718a-123">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b718a-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b718a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b718a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b718a-125">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="b718a-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b718a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b718a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b718a-127"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b718a-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="b718a-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="b718a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b718a-129"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b718a-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="b718a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b718a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b718a-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b718a-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b718a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b718a-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="b718a-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b718a-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

