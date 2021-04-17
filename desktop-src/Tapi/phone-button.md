---
description: A mensagem do botão de telefone TAPI \_ é enviada para notificar o aplicativo de que o monitoramento de pressionamento de botão está habilitado caso tenha detectado um pressionamento de botão no telefone local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Mensagem de PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757201"
---
# <a name="phone_button-message"></a><span data-ttu-id="d0a57-103">\_Mensagem do botão telefone</span><span class="sxs-lookup"><span data-stu-id="d0a57-103">PHONE\_BUTTON message</span></span>

<span data-ttu-id="d0a57-104">A mensagem **do \_ botão de telefone** TAPI é enviada para notificar o aplicativo de que o monitoramento de pressionamento de botão está habilitado caso tenha detectado um pressionamento de botão no telefone local.</span><span class="sxs-lookup"><span data-stu-id="d0a57-104">The TAPI **PHONE\_BUTTON** message is sent to notify the application that button press monitoring is enabled if it has detected a button press on the local phone.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="d0a57-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d0a57-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a57-106">*hPhone*</span><span class="sxs-lookup"><span data-stu-id="d0a57-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a57-107">Um identificador para o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="d0a57-107">A handle to the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="d0a57-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="d0a57-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a57-109">A instância de retorno de chamada do aplicativo fornecida ao abrir o dispositivo de telefone.</span><span class="sxs-lookup"><span data-stu-id="d0a57-109">The application's callback instance provided when opening the phone device.</span></span>

</dd> <dt>

<span data-ttu-id="d0a57-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d0a57-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a57-111">O identificador de botão/lâmpada do botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="d0a57-111">The button/lamp identifier of the button that was pressed.</span></span> <span data-ttu-id="d0a57-112">Observe que os identificadores de botão de zero a 11 são sempre os botões do teclado, sendo que ' 0 ' é o identificador de botão zero, ' 1 ', sendo o identificador de botão 1 (e assim por diante, por meio do identificador de botão 9) e com ' \* ' sendo o identificador de botão 10 e ' \# ' sendo o identificador de botão 11.</span><span class="sxs-lookup"><span data-stu-id="d0a57-112">Note that button identifiers zero through 11 are always the KEYPAD buttons, with '0' being button identifier zero, '1' being button identifier 1 (and so on through button identifier 9), and with '\*' being button identifier 10, and '\#' being button identifier 11.</span></span> <span data-ttu-id="d0a57-113">Informações adicionais sobre um identificador de botão estão disponíveis com [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) e [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span><span class="sxs-lookup"><span data-stu-id="d0a57-113">Additional information about a button identifier is available with [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) and [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).</span></span>

</dd> <dt>

<span data-ttu-id="d0a57-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d0a57-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a57-115">O modo de botão do botão.</span><span class="sxs-lookup"><span data-stu-id="d0a57-115">The button mode of the button.</span></span> <span data-ttu-id="d0a57-116">Esse parâmetro usa uma das [**\_ constantes PHONEBUTTONMODE**](phonebuttonmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d0a57-116">This parameter uses one of the [**PHONEBUTTONMODE\_ constants**](phonebuttonmode--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0a57-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d0a57-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a57-118">Especifica se este é um evento de botão suspenso ou um evento de botão.</span><span class="sxs-lookup"><span data-stu-id="d0a57-118">Specifies whether this is a button-down event or a button-up event.</span></span> <span data-ttu-id="d0a57-119">Esse parâmetro usa uma das [**\_ constantes PHONEBUTTONSTATE**](phonebuttonstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="d0a57-119">This parameter uses one of the [**PHONEBUTTONSTATE\_ constants**](phonebuttonstate--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a57-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d0a57-120">Return value</span></span>

<span data-ttu-id="d0a57-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d0a57-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a57-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0a57-122">Remarks</span></span>

<span data-ttu-id="d0a57-123">Uma mensagem de **\_ botão de telefone** é enviada sempre que um botão muda de estado.</span><span class="sxs-lookup"><span data-stu-id="d0a57-123">A **PHONE\_BUTTON** message is sent whenever a button changes state.</span></span> <span data-ttu-id="d0a57-124">Um aplicativo tem a garantia de que, para cada evento de botão abaixo, ele é eventualmente enviado um evento de botão correspondente.</span><span class="sxs-lookup"><span data-stu-id="d0a57-124">An application is guaranteed that for each button down event, it is eventually sent a corresponding button up event.</span></span> <span data-ttu-id="d0a57-125">Um provedor de serviços que é incapaz de detectar o botão real é necessário para gerar a mensagem de botão para cima logo após a mensagem do botão para baixo para cada pressionamento de botão.</span><span class="sxs-lookup"><span data-stu-id="d0a57-125">A service provider that is incapable of detecting the actual button up is required to generate the button up message shortly after the button down message for each button press.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a57-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0a57-126">Requirements</span></span>



| <span data-ttu-id="d0a57-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a57-127">Requirement</span></span> | <span data-ttu-id="d0a57-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d0a57-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d0a57-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="d0a57-129">TAPI version</span></span><br/> | <span data-ttu-id="d0a57-130">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="d0a57-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="d0a57-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d0a57-131">Header</span></span><br/>       | <dl> <span data-ttu-id="d0a57-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a57-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a57-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0a57-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a57-134">**phoneGetButtonInfo**</span><span class="sxs-lookup"><span data-stu-id="d0a57-134">**phoneGetButtonInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[<span data-ttu-id="d0a57-135">**phoneGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="d0a57-135">**phoneGetDevCaps**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




