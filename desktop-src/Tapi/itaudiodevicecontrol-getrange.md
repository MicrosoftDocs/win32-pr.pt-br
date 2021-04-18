---
description: O método GetRange recupera o intervalo de valores válidos para uma determinada propriedade de dispositivo de áudio.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'Método ITAudioDeviceControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811929"
---
# <a name="itaudiodevicecontrolgetrange-method"></a><span data-ttu-id="0ac30-103">Método ITAudioDeviceControl:: GetRange</span><span class="sxs-lookup"><span data-stu-id="0ac30-103">ITAudioDeviceControl::GetRange method</span></span>

<span data-ttu-id="0ac30-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0ac30-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0ac30-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0ac30-106">O método **GetRange** recupera o intervalo de valores válidos para uma determinada [**propriedade de dispositivo de áudio**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="0ac30-106">The **GetRange** method retrieves the range of valid values for a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac30-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ac30-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="0ac30-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ac30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ac30-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac30-110">Membro da enumeração [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac30-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="0ac30-111">*plMin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac30-112">Valor mínimo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ac30-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="0ac30-113">*plMax* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac30-114">Valor máximo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="0ac30-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="0ac30-115">*plSteppingDelta* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac30-116">Incremento pelo qual o valor da propriedade pode ser aumentado ou diminuído.</span><span class="sxs-lookup"><span data-stu-id="0ac30-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="0ac30-117">*plDefault* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac30-118">Valor padrão para o parâmetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="0ac30-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ac30-119">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0ac30-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ac30-120">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="0ac30-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ac30-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ac30-121">Return value</span></span>

<span data-ttu-id="0ac30-122">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0ac30-122">This method can return one of these values.</span></span>



| <span data-ttu-id="0ac30-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0ac30-123">Return code</span></span>                                                                                   | <span data-ttu-id="0ac30-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ac30-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0ac30-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac30-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0ac30-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0ac30-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0ac30-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ac30-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0ac30-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0ac30-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0ac30-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ac30-129">Requirements</span></span>



| <span data-ttu-id="0ac30-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ac30-130">Requirement</span></span> | <span data-ttu-id="0ac30-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0ac30-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac30-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="0ac30-132">TAPI version</span></span><br/> | <span data-ttu-id="0ac30-133">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="0ac30-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="0ac30-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ac30-134">Header</span></span><br/>       | <dl> <span data-ttu-id="0ac30-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac30-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ac30-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ac30-136">Library</span></span><br/>      | <dl> <span data-ttu-id="0ac30-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ac30-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="0ac30-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0ac30-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="0ac30-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ac30-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ac30-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ac30-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ac30-141">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="0ac30-141">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="0ac30-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="0ac30-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="0ac30-143">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="0ac30-143">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




