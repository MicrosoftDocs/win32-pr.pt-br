---
description: O método GetRange Obtém o intervalo de valores válidos para uma determinada propriedade de qualidade de fluxo.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'Método ITStreamQualityControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792621"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="09e17-103">Método ITStreamQualityControl:: GetRange</span><span class="sxs-lookup"><span data-stu-id="09e17-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="09e17-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="09e17-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="09e17-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="09e17-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="09e17-106">O método **GetRange** Obtém o intervalo de valores válidos para uma determinada [**propriedade de qualidade de fluxo**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="09e17-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="09e17-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09e17-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="09e17-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09e17-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e17-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09e17-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e17-110">Membro da enumeração [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="09e17-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="09e17-111">*plMin* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09e17-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e17-112">Valor mínimo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="09e17-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="09e17-113">*plMax* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09e17-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e17-114">Valor máximo válido para a propriedade de entrada.</span><span class="sxs-lookup"><span data-stu-id="09e17-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="09e17-115">*plSteppingDelta* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09e17-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e17-116">Incremento pelo qual o valor da propriedade pode ser aumentado ou diminuído.</span><span class="sxs-lookup"><span data-stu-id="09e17-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="09e17-117">*plDefault* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09e17-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e17-118">Valor padrão para o parâmetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="09e17-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="09e17-119">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09e17-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e17-120">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="09e17-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e17-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09e17-121">Return value</span></span>

<span data-ttu-id="09e17-122">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="09e17-122">This method can return one of these values.</span></span>



| <span data-ttu-id="09e17-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="09e17-123">Return code</span></span>                                                                                   | <span data-ttu-id="09e17-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="09e17-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="09e17-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09e17-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="09e17-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="09e17-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="09e17-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="09e17-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="09e17-128">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="09e17-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="09e17-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09e17-129">Requirements</span></span>



| <span data-ttu-id="09e17-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="09e17-130">Requirement</span></span> | <span data-ttu-id="09e17-131">Valor</span><span class="sxs-lookup"><span data-stu-id="09e17-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="09e17-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="09e17-132">TAPI version</span></span><br/> | <span data-ttu-id="09e17-133">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="09e17-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="09e17-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09e17-134">Header</span></span><br/>       | <dl> <span data-ttu-id="09e17-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e17-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="09e17-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09e17-136">Library</span></span><br/>      | <dl> <span data-ttu-id="09e17-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09e17-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="09e17-138">DLL</span><span class="sxs-lookup"><span data-stu-id="09e17-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="09e17-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09e17-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e17-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="09e17-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e17-141">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="09e17-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="09e17-142">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="09e17-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="09e17-143">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="09e17-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




