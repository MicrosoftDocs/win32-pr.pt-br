---
title: Método IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: O método ProcessRegistrationResponse processa uma resposta de registro enviada pelo transmissor em resposta a um desafio de registro.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Formato de mídia do Windows do método ProcessRegistrationResponse
- Método ProcessRegistrationResponse Windows Media Format, interface IWMDRMNetReceiver
- Formato de mídia do Windows de interface IWMDRMNetReceiver, método ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786945"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="9bddb-106">IWMDRMNetReceiver: método rocessRegistrationResponse de:P</span><span class="sxs-lookup"><span data-stu-id="9bddb-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="9bddb-107">O método **ProcessRegistrationResponse** processa uma resposta de registro enviada pelo transmissor em resposta a um desafio de registro.</span><span class="sxs-lookup"><span data-stu-id="9bddb-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bddb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bddb-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="9bddb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bddb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bddb-110">*pbRegistrationResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9bddb-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bddb-111">Resposta de registro recebida do transmissor.</span><span class="sxs-lookup"><span data-stu-id="9bddb-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="9bddb-112">*cbRegistrationResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9bddb-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bddb-113">Tamanho da resposta de registro em bytes.</span><span class="sxs-lookup"><span data-stu-id="9bddb-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9bddb-114">*ppunkCancellationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9bddb-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bddb-115">Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9bddb-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="9bddb-116">Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="9bddb-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bddb-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bddb-117">Return value</span></span>

<span data-ttu-id="9bddb-118">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9bddb-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9bddb-119">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9bddb-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9bddb-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9bddb-120">Return code</span></span>                                                                          | <span data-ttu-id="9bddb-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bddb-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9bddb-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9bddb-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9bddb-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="9bddb-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9bddb-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bddb-124">Remarks</span></span>

<span data-ttu-id="9bddb-125">Esse método é executado de forma assíncrona; Quando o processamento é concluído, o evento MEProximityCompleted é enviado para a interface **IMFMediaEventGenerator** .</span><span class="sxs-lookup"><span data-stu-id="9bddb-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bddb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bddb-126">Requirements</span></span>



| <span data-ttu-id="9bddb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bddb-127">Requirement</span></span> | <span data-ttu-id="9bddb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9bddb-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bddb-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bddb-129">Header</span></span><br/> | <dl> <span data-ttu-id="9bddb-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bddb-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bddb-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bddb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bddb-132">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="9bddb-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="9bddb-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="9bddb-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





