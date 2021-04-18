---
description: O método EnumerateStreams enumera fluxos atualmente com os participantes. Esse método é fornecido para aplicativos C e C++. Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o \_ método Get Streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'Método ITParticipant:: EnumerateStreams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760340"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="ed036-105">Método ITParticipant:: EnumerateStreams</span><span class="sxs-lookup"><span data-stu-id="ed036-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="ed036-106">\[O **EnumerateStreams** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ed036-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ed036-107">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="ed036-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ed036-108">O método **EnumerateStreams** enumera fluxos atualmente com os participantes.</span><span class="sxs-lookup"><span data-stu-id="ed036-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="ed036-109">Esse método é fornecido para aplicativos C e C++.</span><span class="sxs-lookup"><span data-stu-id="ed036-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="ed036-110">Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o método [**Get \_ streams**](itparticipant-get-streams.md) .</span><span class="sxs-lookup"><span data-stu-id="ed036-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed036-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed036-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="ed036-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed036-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed036-113">*ppEnumStream* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ed036-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed036-114">Ponteiro para ponteiro de interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .</span><span class="sxs-lookup"><span data-stu-id="ed036-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed036-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed036-115">Return value</span></span>

<span data-ttu-id="ed036-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ed036-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ed036-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ed036-117">Value</span></span>                                                                                     | <span data-ttu-id="ed036-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ed036-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ed036-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ed036-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ed036-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="ed036-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ed036-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ed036-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ed036-122">O parâmetro *ppEnumStream* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="ed036-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed036-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed036-123">Remarks</span></span>

<span data-ttu-id="ed036-124">A TAPI chama o método **AddRef** na interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) retornada por **ITParticipant:: EnumerateStreams**.</span><span class="sxs-lookup"><span data-stu-id="ed036-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="ed036-125">O aplicativo deve chamar **Release** na interface **IEnumStream** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="ed036-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed036-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed036-126">Requirements</span></span>



| <span data-ttu-id="ed036-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed036-127">Requirement</span></span> | <span data-ttu-id="ed036-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ed036-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed036-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ed036-129">TAPI version</span></span><br/> | <span data-ttu-id="ed036-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ed036-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="ed036-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed036-131">Header</span></span><br/>       | <dl> <span data-ttu-id="ed036-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed036-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed036-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed036-133">Library</span></span><br/>      | <dl> <span data-ttu-id="ed036-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed036-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="ed036-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ed036-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="ed036-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed036-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed036-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed036-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed036-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="ed036-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="ed036-139">**obter \_ fluxos**</span><span class="sxs-lookup"><span data-stu-id="ed036-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="ed036-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="ed036-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




