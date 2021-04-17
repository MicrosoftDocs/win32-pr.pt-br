---
description: O método Get recupera o valor de uma determinada propriedade de dispositivo de áudio.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: 'Método ITAudioDeviceControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4311dc18291fcfbbe533dbe17042e6ba19c1122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779906"
---
# <a name="itaudiodevicecontrolget-method"></a><span data-ttu-id="50dd3-103">Método ITAudioDeviceControl:: Get</span><span class="sxs-lookup"><span data-stu-id="50dd3-103">ITAudioDeviceControl::Get method</span></span>

<span data-ttu-id="50dd3-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="50dd3-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="50dd3-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="50dd3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="50dd3-106">O método **Get** recupera o valor de uma determinada [**propriedade de dispositivo de áudio**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="50dd3-106">The **Get** method retrieves the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50dd3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50dd3-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="50dd3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50dd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50dd3-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50dd3-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50dd3-110">Membro da enumeração [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="50dd3-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="50dd3-111">*plValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50dd3-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50dd3-112">Valor da *Propriedade* de entrada.</span><span class="sxs-lookup"><span data-stu-id="50dd3-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="50dd3-113">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50dd3-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50dd3-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="50dd3-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50dd3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50dd3-115">Return value</span></span>

<span data-ttu-id="50dd3-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="50dd3-116">This method can return one of these values.</span></span>



| <span data-ttu-id="50dd3-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="50dd3-117">Return code</span></span>                                                                                   | <span data-ttu-id="50dd3-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="50dd3-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="50dd3-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50dd3-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="50dd3-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="50dd3-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="50dd3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="50dd3-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="50dd3-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="50dd3-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50dd3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50dd3-123">Requirements</span></span>



| <span data-ttu-id="50dd3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="50dd3-124">Requirement</span></span> | <span data-ttu-id="50dd3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="50dd3-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50dd3-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="50dd3-126">TAPI version</span></span><br/> | <span data-ttu-id="50dd3-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="50dd3-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="50dd3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50dd3-128">Header</span></span><br/>       | <dl> <span data-ttu-id="50dd3-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50dd3-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50dd3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50dd3-130">Library</span></span><br/>      | <dl> <span data-ttu-id="50dd3-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50dd3-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="50dd3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="50dd3-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="50dd3-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50dd3-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50dd3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="50dd3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50dd3-135">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="50dd3-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="50dd3-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="50dd3-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="50dd3-137">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="50dd3-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




