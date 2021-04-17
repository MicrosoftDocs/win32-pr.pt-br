---
description: O \_ método Get participantes cria uma coleção de participantes associados à conferência atual.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: 'Método ITParticipantControl:: get_Participants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782911"
---
# <a name="itparticipantcontrolget_participants-method"></a><span data-ttu-id="187d0-103">Método ITParticipantControl:: get \_ participantes</span><span class="sxs-lookup"><span data-stu-id="187d0-103">ITParticipantControl::get\_Participants method</span></span>

<span data-ttu-id="187d0-104">\[**obter \_ Os participantes** não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="187d0-104">\[**get\_Participants** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="187d0-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="187d0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="187d0-106">O método **Get \_ participantes** cria uma coleção de participantes associados à conferência atual.</span><span class="sxs-lookup"><span data-stu-id="187d0-106">The **get\_Participants** method creates a collection of participants associated with the current conference.</span></span> <span data-ttu-id="187d0-107">Esse método é fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="187d0-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="187d0-108">Os aplicativos C e C++ devem usar o método [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) .</span><span class="sxs-lookup"><span data-stu-id="187d0-108">C and C++ applications must use the [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="187d0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="187d0-109">Syntax</span></span>


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="187d0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="187d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="187d0-111">*pVariant* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="187d0-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="187d0-112">Ponteiro para **Variant** que contém um [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de ponteiros de interface [**ITParticipant**](itparticipant.md) .</span><span class="sxs-lookup"><span data-stu-id="187d0-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITParticipant**](itparticipant.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="187d0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="187d0-113">Return value</span></span>

<span data-ttu-id="187d0-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="187d0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="187d0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="187d0-115">Value</span></span>                                                                                         | <span data-ttu-id="187d0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="187d0-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="187d0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="187d0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="187d0-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="187d0-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="187d0-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="187d0-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="187d0-120">O parâmetro *pVariant* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="187d0-120">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |
| <dl> <span data-ttu-id="187d0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="187d0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="187d0-122">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="187d0-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="187d0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="187d0-123">Remarks</span></span>

<span data-ttu-id="187d0-124">A TAPI chama o método **AddRef** na interface [**ITParticipant**](itparticipant.md) retornada por **ITParticipantControl:: get \_ participantes**.</span><span class="sxs-lookup"><span data-stu-id="187d0-124">TAPI calls the **AddRef** method on the [**ITParticipant**](itparticipant.md) interface returned by **ITParticipantControl::get\_Participants**.</span></span> <span data-ttu-id="187d0-125">O aplicativo deve chamar **Release** na interface **ITParticipant** para liberar recursos associados a ela.</span><span class="sxs-lookup"><span data-stu-id="187d0-125">The application must call **Release** on the **ITParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="187d0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="187d0-126">Requirements</span></span>



| <span data-ttu-id="187d0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="187d0-127">Requirement</span></span> | <span data-ttu-id="187d0-128">Valor</span><span class="sxs-lookup"><span data-stu-id="187d0-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="187d0-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="187d0-129">TAPI version</span></span><br/> | <span data-ttu-id="187d0-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="187d0-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="187d0-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="187d0-131">Header</span></span><br/>       | <dl> <span data-ttu-id="187d0-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="187d0-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="187d0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="187d0-133">Library</span></span><br/>      | <dl> <span data-ttu-id="187d0-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="187d0-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="187d0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="187d0-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="187d0-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="187d0-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="187d0-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="187d0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187d0-138">**ITParticipantControl**</span><span class="sxs-lookup"><span data-stu-id="187d0-138">**ITParticipantControl**</span></span>](itparticipantcontrol.md)
</dt> <dt>

[<span data-ttu-id="187d0-139">**EnumerateParticipants**</span><span class="sxs-lookup"><span data-stu-id="187d0-139">**EnumerateParticipants**</span></span>](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[<span data-ttu-id="187d0-140">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="187d0-140">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="187d0-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="187d0-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




