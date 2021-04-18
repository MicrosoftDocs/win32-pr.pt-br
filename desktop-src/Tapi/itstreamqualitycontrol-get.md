---
description: O método Get recupera o valor de uma determinada propriedade de qualidade de fluxo.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'Método ITStreamQualityControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760158"
---
# <a name="itstreamqualitycontrolget-method"></a><span data-ttu-id="2ae75-103">Método ITStreamQualityControl:: Get</span><span class="sxs-lookup"><span data-stu-id="2ae75-103">ITStreamQualityControl::Get method</span></span>

<span data-ttu-id="2ae75-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2ae75-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ae75-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="2ae75-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2ae75-106">O método **Get** recupera o valor de uma determinada [**propriedade de qualidade de fluxo**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="2ae75-106">The **Get** method retrieves the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae75-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ae75-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2ae75-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ae75-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae75-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ae75-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae75-110">Membro da enumeração [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae75-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="2ae75-111">*plValue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2ae75-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae75-112">Valor da *Propriedade* de entrada.</span><span class="sxs-lookup"><span data-stu-id="2ae75-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="2ae75-113">*plFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2ae75-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae75-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.</span><span class="sxs-lookup"><span data-stu-id="2ae75-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae75-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ae75-115">Return value</span></span>

<span data-ttu-id="2ae75-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="2ae75-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2ae75-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2ae75-117">Return code</span></span>                                                                                   | <span data-ttu-id="2ae75-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ae75-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2ae75-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ae75-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ae75-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2ae75-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2ae75-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2ae75-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ae75-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2ae75-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2ae75-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ae75-123">Requirements</span></span>



| <span data-ttu-id="2ae75-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ae75-124">Requirement</span></span> | <span data-ttu-id="2ae75-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2ae75-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae75-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="2ae75-126">TAPI version</span></span><br/> | <span data-ttu-id="2ae75-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="2ae75-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="2ae75-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ae75-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2ae75-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae75-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ae75-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ae75-130">Library</span></span><br/>      | <dl> <span data-ttu-id="2ae75-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ae75-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2ae75-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae75-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="2ae75-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ae75-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae75-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ae75-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae75-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="2ae75-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="2ae75-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="2ae75-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="2ae75-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="2ae75-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




