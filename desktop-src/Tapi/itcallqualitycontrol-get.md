---
description: O método Get Obtém o valor de uma determinada propriedade de controle de qualidade de chamada.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'Método ITCallQualityControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea42768c173c0c073abe356e1ae6816a486a03c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779465"
---
# <a name="itcallqualitycontrolget-method"></a><span data-ttu-id="1a344-103">Método ITCallQualityControl:: Get</span><span class="sxs-lookup"><span data-stu-id="1a344-103">ITCallQualityControl::Get method</span></span>

<span data-ttu-id="1a344-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1a344-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1a344-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1a344-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1a344-106">O método **Get** Obtém o valor de uma determinada [propriedade de controle de qualidade de chamada](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1a344-106">The **Get** method gets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a344-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a344-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1a344-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a344-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a344-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a344-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a344-110">Membro da enumeração [**CallQualityProperty**](callqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="1a344-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="1a344-111">*plValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a344-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a344-112">Valor da *Propriedade* de entrada.</span><span class="sxs-lookup"><span data-stu-id="1a344-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="1a344-113">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a344-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a344-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="1a344-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a344-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a344-115">Return value</span></span>

<span data-ttu-id="1a344-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="1a344-116">This method can return one of these values.</span></span>



| <span data-ttu-id="1a344-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1a344-117">Return code</span></span>                                                                                   | <span data-ttu-id="1a344-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a344-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1a344-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a344-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1a344-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1a344-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1a344-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1a344-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1a344-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1a344-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1a344-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a344-123">Requirements</span></span>



| <span data-ttu-id="1a344-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a344-124">Requirement</span></span> | <span data-ttu-id="1a344-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1a344-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1a344-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1a344-126">TAPI version</span></span><br/> | <span data-ttu-id="1a344-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="1a344-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="1a344-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a344-128">Header</span></span><br/>       | <dl> <span data-ttu-id="1a344-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a344-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a344-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a344-130">Library</span></span><br/>      | <dl> <span data-ttu-id="1a344-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a344-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="1a344-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1a344-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="1a344-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a344-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a344-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a344-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a344-135">**ITCallQualityControl**</span><span class="sxs-lookup"><span data-stu-id="1a344-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="1a344-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="1a344-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="1a344-137">**CallQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="1a344-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




