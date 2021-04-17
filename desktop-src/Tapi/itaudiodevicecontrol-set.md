---
description: O método set define o valor de uma determinada propriedade de dispositivo de áudio.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'Método ITAudioDeviceControl:: Set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789870"
---
# <a name="itaudiodevicecontrolset-method"></a><span data-ttu-id="7151e-103">Método ITAudioDeviceControl:: Set</span><span class="sxs-lookup"><span data-stu-id="7151e-103">ITAudioDeviceControl::Set method</span></span>

<span data-ttu-id="7151e-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7151e-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7151e-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="7151e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7151e-106">O método **set** define o valor de uma determinada [**propriedade de dispositivo de áudio**](audiodeviceproperty.md).</span><span class="sxs-lookup"><span data-stu-id="7151e-106">The **Set** method sets the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7151e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7151e-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="7151e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7151e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7151e-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7151e-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7151e-110">Membro da enumeração [**AudioDeviceProperty**](audiodeviceproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="7151e-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="7151e-111">*lvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7151e-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7151e-112">Valor desejado para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="7151e-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="7151e-113">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7151e-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7151e-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* deve ser controlado.</span><span class="sxs-lookup"><span data-stu-id="7151e-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7151e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7151e-115">Return value</span></span>

<span data-ttu-id="7151e-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="7151e-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7151e-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7151e-117">Return code</span></span>                                                                                   | <span data-ttu-id="7151e-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="7151e-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7151e-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7151e-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7151e-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7151e-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7151e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7151e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7151e-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="7151e-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7151e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7151e-123">Requirements</span></span>



| <span data-ttu-id="7151e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7151e-124">Requirement</span></span> | <span data-ttu-id="7151e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7151e-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7151e-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="7151e-126">TAPI version</span></span><br/> | <span data-ttu-id="7151e-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7151e-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7151e-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7151e-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7151e-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7151e-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7151e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7151e-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7151e-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7151e-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7151e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7151e-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7151e-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7151e-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7151e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7151e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7151e-135">**ITAudioDeviceControl**</span><span class="sxs-lookup"><span data-stu-id="7151e-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="7151e-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="7151e-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="7151e-137">**AudioDeviceProperty**</span><span class="sxs-lookup"><span data-stu-id="7151e-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




