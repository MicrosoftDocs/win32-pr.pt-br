---
description: O método set define o valor de uma determinada propriedade de qualidade de fluxo.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'Método ITStreamQualityControl:: Set (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757620"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="10784-103">Método ITStreamQualityControl:: Set</span><span class="sxs-lookup"><span data-stu-id="10784-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="10784-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="10784-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="10784-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="10784-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="10784-106">O método **set** define o valor de uma determinada [**propriedade de qualidade de fluxo**](streamqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="10784-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="10784-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10784-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="10784-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10784-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10784-109">*Propriedade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10784-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10784-110">Membro da enumeração [**StreamQualityProperty**](streamqualityproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="10784-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="10784-111">*lvalue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10784-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10784-112">Valor desejado para a *Propriedade* de entrada.</span><span class="sxs-lookup"><span data-stu-id="10784-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="10784-113">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10784-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10784-114">Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* deve ser controlado.</span><span class="sxs-lookup"><span data-stu-id="10784-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10784-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10784-115">Return value</span></span>

<span data-ttu-id="10784-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="10784-116">This method can return one of these values.</span></span>



| <span data-ttu-id="10784-117">Valor</span><span class="sxs-lookup"><span data-stu-id="10784-117">Value</span></span>                                                                                         | <span data-ttu-id="10784-118">Significado</span><span class="sxs-lookup"><span data-stu-id="10784-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="10784-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10784-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="10784-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="10784-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="10784-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="10784-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="10784-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="10784-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="10784-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10784-123">Requirements</span></span>



| <span data-ttu-id="10784-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="10784-124">Requirement</span></span> | <span data-ttu-id="10784-125">Valor</span><span class="sxs-lookup"><span data-stu-id="10784-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10784-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="10784-126">TAPI version</span></span><br/> | <span data-ttu-id="10784-127">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="10784-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="10784-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10784-128">Header</span></span><br/>       | <dl> <span data-ttu-id="10784-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="10784-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="10784-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10784-130">Library</span></span><br/>      | <dl> <span data-ttu-id="10784-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10784-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="10784-132">DLL</span><span class="sxs-lookup"><span data-stu-id="10784-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="10784-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10784-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10784-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="10784-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10784-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="10784-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="10784-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="10784-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="10784-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="10784-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




