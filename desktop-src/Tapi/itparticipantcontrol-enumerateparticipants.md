---
description: O método EnumerateParticipants enumera os participantes associados à conferência atual.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Método ITParticipantControl:: EnumerateParticipants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758117"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a><span data-ttu-id="90bab-103">Método ITParticipantControl:: EnumerateParticipants</span><span class="sxs-lookup"><span data-stu-id="90bab-103">ITParticipantControl::EnumerateParticipants method</span></span>

<span data-ttu-id="90bab-104">\[O **EnumerateParticipants** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="90bab-104">\[**EnumerateParticipants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="90bab-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="90bab-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="90bab-106">O método **EnumerateParticipants** enumera os participantes associados à conferência atual.</span><span class="sxs-lookup"><span data-stu-id="90bab-106">The **EnumerateParticipants** method enumerates participants associated with the current conference.</span></span> <span data-ttu-id="90bab-107">Esse método é fornecido para aplicativos C e C++.</span><span class="sxs-lookup"><span data-stu-id="90bab-107">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="90bab-108">Aplicativos cliente de automação, como aqueles escritos em Visual Basic, devem usar o método [**Get \_ participantes**](itparticipantcontrol-get-participants.md) .</span><span class="sxs-lookup"><span data-stu-id="90bab-108">Automation client applications, such as those written in Visual Basic, must use the [**get\_Participants**](itparticipantcontrol-get-participants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="90bab-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90bab-109">Syntax</span></span>


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a><span data-ttu-id="90bab-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90bab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90bab-111">*ppEnumParticipants* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="90bab-111">*ppEnumParticipants* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90bab-112">Ponteiro para a interface [**IEnumParticipant**](ienumparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="90bab-112">Pointer to [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90bab-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90bab-113">Return value</span></span>

<span data-ttu-id="90bab-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="90bab-114">This method can return one of these values.</span></span>



| <span data-ttu-id="90bab-115">Valor</span><span class="sxs-lookup"><span data-stu-id="90bab-115">Value</span></span>                                                                                         | <span data-ttu-id="90bab-116">Significado</span><span class="sxs-lookup"><span data-stu-id="90bab-116">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="90bab-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90bab-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="90bab-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="90bab-118">Method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="90bab-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="90bab-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="90bab-120">O parâmetro *ppEnumParticipants* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="90bab-120">The *ppEnumParticipants* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="90bab-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="90bab-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="90bab-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="90bab-122">Insufficient memory exists to perform the operation.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="90bab-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="90bab-123">Remarks</span></span>

<span data-ttu-id="90bab-124">A TAPI chama o método **AddRef** na interface [**IEnumParticipant**](ienumparticipant.md) retornada por **ITParticipantControl:: EnumerateParticipants**.</span><span class="sxs-lookup"><span data-stu-id="90bab-124">TAPI calls the **AddRef** method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **ITParticipantControl::EnumerateParticipants**.</span></span> <span data-ttu-id="90bab-125">O aplicativo deve chamar **Release** na interface **IEnumParticipant** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="90bab-125">The application must call **Release** on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="90bab-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90bab-126">Requirements</span></span>



| <span data-ttu-id="90bab-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="90bab-127">Requirement</span></span> | <span data-ttu-id="90bab-128">Valor</span><span class="sxs-lookup"><span data-stu-id="90bab-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90bab-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="90bab-129">TAPI version</span></span><br/> | <span data-ttu-id="90bab-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="90bab-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="90bab-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90bab-131">Header</span></span><br/>       | <dl> <span data-ttu-id="90bab-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="90bab-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="90bab-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90bab-133">Library</span></span><br/>      | <dl> <span data-ttu-id="90bab-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90bab-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="90bab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="90bab-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="90bab-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90bab-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="90bab-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="90bab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90bab-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="90bab-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="90bab-139">**obter \_ participantes**</span><span class="sxs-lookup"><span data-stu-id="90bab-139">**get\_Participants**</span></span>](itparticipantcontrol-get-participants.md)
</dt> <dt>

[<span data-ttu-id="90bab-140">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="90bab-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="90bab-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="90bab-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




