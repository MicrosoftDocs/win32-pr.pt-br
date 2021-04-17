---
description: O \_ método Get streams cria uma coleção de fluxos associados ao participante atual.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Método ITParticipant:: get_Streams (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766222"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="87329-103">Método ITParticipant:: get \_ streams</span><span class="sxs-lookup"><span data-stu-id="87329-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="87329-104">\[**obter \_ Os fluxos** não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="87329-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="87329-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="87329-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="87329-106">O método **Get \_ streams** cria uma coleção de fluxos associados ao participante atual.</span><span class="sxs-lookup"><span data-stu-id="87329-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="87329-107">Esse método é fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="87329-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="87329-108">Os aplicativos C e C++ devem usar o método [**EnumerateStreams**](itparticipant-enumeratestreams.md) .</span><span class="sxs-lookup"><span data-stu-id="87329-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="87329-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87329-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="87329-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87329-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87329-111">*pVariant* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="87329-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87329-112">Ponteiro para **Variant** que contém um [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de ponteiros de interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="87329-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87329-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87329-113">Return value</span></span>

<span data-ttu-id="87329-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="87329-114">This method can return one of these values.</span></span>



| <span data-ttu-id="87329-115">Valor</span><span class="sxs-lookup"><span data-stu-id="87329-115">Value</span></span>                                                                                         | <span data-ttu-id="87329-116">Significado</span><span class="sxs-lookup"><span data-stu-id="87329-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="87329-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87329-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="87329-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="87329-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="87329-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="87329-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="87329-120">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="87329-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="87329-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="87329-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="87329-122">O parâmetro *pVariant* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="87329-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="87329-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="87329-123">Remarks</span></span>

<span data-ttu-id="87329-124">A TAPI chama o método **AddRef** na interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) retornada por **ITParticipant:: get \_ streams**.</span><span class="sxs-lookup"><span data-stu-id="87329-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="87329-125">O aplicativo deve chamar **Release** na interface **ITStream** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="87329-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="87329-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87329-126">Requirements</span></span>



| <span data-ttu-id="87329-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="87329-127">Requirement</span></span> | <span data-ttu-id="87329-128">Valor</span><span class="sxs-lookup"><span data-stu-id="87329-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87329-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="87329-129">TAPI version</span></span><br/> | <span data-ttu-id="87329-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="87329-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="87329-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87329-131">Header</span></span><br/>       | <dl> <span data-ttu-id="87329-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="87329-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="87329-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87329-133">Library</span></span><br/>      | <dl> <span data-ttu-id="87329-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87329-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="87329-135">DLL</span><span class="sxs-lookup"><span data-stu-id="87329-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="87329-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87329-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87329-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="87329-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87329-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="87329-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="87329-139">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="87329-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="87329-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="87329-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="87329-141">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="87329-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="87329-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="87329-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

