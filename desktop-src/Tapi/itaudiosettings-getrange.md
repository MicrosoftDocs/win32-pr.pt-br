---
description: O método GetRange recupera o intervalo de valores válidos para uma determinada propriedade de configurações de áudio.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'Método ITAudioSettings:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788063"
---
# <a name="itaudiosettingsgetrange-method"></a><span data-ttu-id="ca314-103">Método ITAudioSettings:: GetRange</span><span class="sxs-lookup"><span data-stu-id="ca314-103">ITAudioSettings::GetRange method</span></span>

<span data-ttu-id="ca314-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ca314-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ca314-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ca314-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ca314-106">O método **GetRange** recupera o intervalo de valores válidos para uma determinada [**propriedade de configurações de áudio**](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="ca314-106">The **GetRange** method retrieves the range of valid values for a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca314-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca314-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="ca314-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca314-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca314-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca314-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca314-110">Membro da enumeração [**AudioSettingsProperty**](audiosettingsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ca314-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="ca314-111">*plMin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca314-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca314-112">Valor mínimo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca314-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="ca314-113">*plMax* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca314-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca314-114">Valor máximo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca314-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="ca314-115">*plSteppingDelta* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca314-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca314-116">Incremento pelo qual o valor da propriedade pode ser aumentado ou diminuído.</span><span class="sxs-lookup"><span data-stu-id="ca314-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="ca314-117">*plDefault* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca314-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca314-118">Valor padrão para o parâmetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="ca314-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ca314-119">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ca314-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca314-120">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="ca314-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca314-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca314-121">Return value</span></span>

<span data-ttu-id="ca314-122">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ca314-122">This method can return one of these values.</span></span>



| <span data-ttu-id="ca314-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ca314-123">Return code</span></span>                                                                                   | <span data-ttu-id="ca314-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca314-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ca314-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca314-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ca314-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ca314-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ca314-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ca314-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ca314-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ca314-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ca314-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca314-129">Requirements</span></span>



| <span data-ttu-id="ca314-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca314-130">Requirement</span></span> | <span data-ttu-id="ca314-131">Valor</span><span class="sxs-lookup"><span data-stu-id="ca314-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca314-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ca314-132">TAPI version</span></span><br/> | <span data-ttu-id="ca314-133">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="ca314-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="ca314-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca314-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ca314-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca314-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca314-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca314-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ca314-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca314-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="ca314-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ca314-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ca314-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca314-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca314-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca314-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca314-141">**ITAudioSettings**</span><span class="sxs-lookup"><span data-stu-id="ca314-141">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="ca314-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="ca314-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="ca314-143">**AudioSettingsProperty**</span><span class="sxs-lookup"><span data-stu-id="ca314-143">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




