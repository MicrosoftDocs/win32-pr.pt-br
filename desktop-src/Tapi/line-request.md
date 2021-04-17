---
description: A mensagem de solicitação de linha TAPI \_ é enviada para relatar a chegada de uma nova solicitação de outro aplicativo.
ms.assetid: d4dbba0d-8225-48d7-a66b-b189fdae70a8
title: Mensagem de LINE_REQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23987e370d5ae9c8eeb579780c5659f8075ac865
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782905"
---
# <a name="line_request-message"></a><span data-ttu-id="f65ed-103">Mensagem de solicitação de linha \_</span><span class="sxs-lookup"><span data-stu-id="f65ed-103">LINE\_REQUEST message</span></span>

<span data-ttu-id="f65ed-104">A mensagem **de \_ solicitação de linha** TAPI é enviada para relatar a chegada de uma nova solicitação de outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f65ed-104">The TAPI **LINE\_REQUEST** message is sent to report the arrival of a new request from another application.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="f65ed-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f65ed-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65ed-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="f65ed-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ed-107">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f65ed-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f65ed-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="f65ed-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ed-109">A instância de registro do aplicativo especificado em [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span><span class="sxs-lookup"><span data-stu-id="f65ed-109">The registration instance of the application specified on [**lineRegisterRequestRecipient**](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient).</span></span>

</dd> <dt>

<span data-ttu-id="f65ed-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="f65ed-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ed-111">O modo de solicitação da solicitação recentemente pendente.</span><span class="sxs-lookup"><span data-stu-id="f65ed-111">The request mode of the newly pending request.</span></span> <span data-ttu-id="f65ed-112">Esse parâmetro usa as [**\_ constantes LINEREQUESTMODE**](linerequestmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="f65ed-112">This parameter uses the [**LINEREQUESTMODE\_ constants**](linerequestmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="f65ed-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="f65ed-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ed-114">As condições para esse parâmetro serão, se *dwParam1* for definido como LINEREQUESTMODE \_ drop, *DwParam2* conterá o *HWND* do aplicativo solicitando a remoção.</span><span class="sxs-lookup"><span data-stu-id="f65ed-114">The conditions for this parameter are, if *dwParam1* is set to LINEREQUESTMODE\_DROP, *dwParam2* contains the *hWnd* of the application requesting the drop.</span></span> <span data-ttu-id="f65ed-115">Caso contrário, *dwParam2* não será usado.</span><span class="sxs-lookup"><span data-stu-id="f65ed-115">Otherwise, *dwParam2* is unused.</span></span>

</dd> <dt>

<span data-ttu-id="f65ed-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="f65ed-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ed-117">Se *dwParam1* for definido como LINEREQUESTMODE \_ drop, a palavra de ordem inferior de *dwParam3* conterá *wRequestID* conforme especificado pelo aplicativo que solicitou o descarte.</span><span class="sxs-lookup"><span data-stu-id="f65ed-117">If *dwParam1* is set to LINEREQUESTMODE\_DROP, the low-order word of *dwParam3* contains the *wRequestID* as specified by the application that requested the drop.</span></span> <span data-ttu-id="f65ed-118">Caso contrário, *dwParam3* não será usado.</span><span class="sxs-lookup"><span data-stu-id="f65ed-118">Otherwise, *dwParam3* is unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65ed-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f65ed-119">Return value</span></span>

<span data-ttu-id="f65ed-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f65ed-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f65ed-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f65ed-121">Remarks</span></span>

<span data-ttu-id="f65ed-122">A mensagem de **\_ solicitação de linha** é enviada para o aplicativo de prioridade mais alta que foi registrado para o modo de solicitação correspondente.</span><span class="sxs-lookup"><span data-stu-id="f65ed-122">The **LINE\_REQUEST** message is sent to the highest priority application that has registered for the corresponding request mode.</span></span> <span data-ttu-id="f65ed-123">Essa mensagem indica a chegada de uma solicitação de telefonia assistida do modo de solicitação especificado.</span><span class="sxs-lookup"><span data-stu-id="f65ed-123">This message indicates the arrival of an Assisted Telephony request of the specified request mode.</span></span> <span data-ttu-id="f65ed-124">Se *dwParam1* for LINEREQUESTMODE \_ MAKECALL, o aplicativo poderá invocar [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) usando o modo de solicitação correspondente para receber a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f65ed-124">If *dwParam1* is LINEREQUESTMODE\_MAKECALL, the application can invoke [**lineGetRequest**](/windows/desktop/api/Tapi/nf-tapi-linegetrequest) using the corresponding request mode to receive the request.</span></span> <span data-ttu-id="f65ed-125">Se *dwParam1* for LINEREQUESTMODE \_ drop, a mensagem conterá todos os dados exigidos pelo destinatário da solicitação para executar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f65ed-125">If *dwParam1* is LINEREQUESTMODE\_DROP, the message contains all of the data the request recipient requires to perform the request.</span></span>

## <a name="requirements"></a><span data-ttu-id="f65ed-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f65ed-126">Requirements</span></span>



| <span data-ttu-id="f65ed-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65ed-127">Requirement</span></span> | <span data-ttu-id="f65ed-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f65ed-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f65ed-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="f65ed-129">TAPI version</span></span><br/> | <span data-ttu-id="f65ed-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f65ed-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f65ed-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f65ed-131">Header</span></span><br/>       | <dl> <span data-ttu-id="f65ed-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="f65ed-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f65ed-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f65ed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65ed-134">**lineGetRequest**</span><span class="sxs-lookup"><span data-stu-id="f65ed-134">**lineGetRequest**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetrequest)
</dt> <dt>

[<span data-ttu-id="f65ed-135">**lineRegisterRequestRecipient**</span><span class="sxs-lookup"><span data-stu-id="f65ed-135">**lineRegisterRequestRecipient**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineregisterrequestrecipient)
</dt> <dt>

[<span data-ttu-id="f65ed-136">**tapiRequestMakeCall**</span><span class="sxs-lookup"><span data-stu-id="f65ed-136">**tapiRequestMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-tapirequestmakecall)
</dt> </dl>

 

 




