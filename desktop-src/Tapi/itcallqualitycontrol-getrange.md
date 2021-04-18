---
description: O método GetRange Obtém o intervalo de valores válidos para uma determinada propriedade de qualidade de chamada.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'Método ITCallQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767758"
---
# <a name="itcallqualitycontrolgetrange-method"></a><span data-ttu-id="1d2d6-103">Método ITCallQualityControl:: GetRange</span><span class="sxs-lookup"><span data-stu-id="1d2d6-103">ITCallQualityControl::GetRange method</span></span>

<span data-ttu-id="1d2d6-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1d2d6-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1d2d6-106">O método **GetRange** Obtém o intervalo de valores válidos para uma determinada [propriedade de qualidade de chamada](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1d2d6-106">The **GetRange** method gets the range of valid values for a given [call quality property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2d6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d2d6-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1d2d6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d2d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2d6-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2d6-110">Membro da enumeração [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1d2d6-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d6-111">*plMin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2d6-112">Valor mínimo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d6-113">*plMax* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2d6-114">Valor máximo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d6-115">*plSteppingDelta* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2d6-116">Incremento pelo qual o valor da propriedade pode ser aumentado ou diminuído.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d6-117">*plDefault* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2d6-118">Valor padrão para o parâmetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="1d2d6-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d2d6-119">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1d2d6-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2d6-120">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2d6-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d2d6-121">Return value</span></span>

<span data-ttu-id="1d2d6-122">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-122">This method can return one of these values.</span></span>



| <span data-ttu-id="1d2d6-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1d2d6-123">Return code</span></span>                                                                                   | <span data-ttu-id="1d2d6-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d2d6-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1d2d6-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2d6-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1d2d6-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1d2d6-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d2d6-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1d2d6-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1d2d6-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1d2d6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d2d6-129">Requirements</span></span>



| <span data-ttu-id="1d2d6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d2d6-130">Requirement</span></span> | <span data-ttu-id="1d2d6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1d2d6-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2d6-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1d2d6-132">TAPI version</span></span><br/> | <span data-ttu-id="1d2d6-133">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="1d2d6-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="1d2d6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d2d6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1d2d6-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d2d6-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d2d6-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d2d6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1d2d6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d2d6-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="1d2d6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2d6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1d2d6-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2d6-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d2d6-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d2d6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2d6-141">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="1d2d6-141">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="1d2d6-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="1d2d6-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="1d2d6-143">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="1d2d6-143">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




