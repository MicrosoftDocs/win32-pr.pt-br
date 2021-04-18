---
description: A mensagem de CALLDEVSPECIFICFEATURE da linha TSPI \_ é enviada para a função de retorno de chamada LINEEVENT para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma linha ou endereço.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: Mensagem de LINE_CALLDEVSPECIFICFEATURE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761958"
---
# <a name="line_calldevspecificfeature-message"></a><span data-ttu-id="72eb6-103">Mensagem de CALLDEVSPECIFICFEATURE de linha \_</span><span class="sxs-lookup"><span data-stu-id="72eb6-103">LINE\_CALLDEVSPECIFICFEATURE message</span></span>

<span data-ttu-id="72eb6-104">A mensagem **de \_ CALLDEVSPECIFICFEATURE da linha** TSPI é enviada para a função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma linha ou endereço.</span><span class="sxs-lookup"><span data-stu-id="72eb6-104">The TSPI **LINE\_CALLDEVSPECIFICFEATURE** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a line or address.</span></span> <span data-ttu-id="72eb6-105">O significado da mensagem e a interpretação dos parâmetros *dwParam1* por meio de *dwParam3* são específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72eb6-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="72eb6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72eb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72eb6-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="72eb6-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="72eb6-108">O identificador de objeto TAPI opaco para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="72eb6-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="72eb6-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="72eb6-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="72eb6-110">O identificador de objeto TAPI opaco para o dispositivo de chamada.</span><span class="sxs-lookup"><span data-stu-id="72eb6-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="72eb6-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="72eb6-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="72eb6-112">A linha de valor \_ CALLDEVSPECIFICFEATURE.</span><span class="sxs-lookup"><span data-stu-id="72eb6-112">The value LINE\_CALLDEVSPECIFICFEATURE.</span></span>

</dd> <dt>

<span data-ttu-id="72eb6-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="72eb6-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="72eb6-114">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72eb6-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="72eb6-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="72eb6-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="72eb6-116">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72eb6-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="72eb6-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="72eb6-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="72eb6-118">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72eb6-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72eb6-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="72eb6-119">Remarks</span></span>

<span data-ttu-id="72eb6-120">A **mensagem \_ CALLDEVSPECIFICFEATURE de linha** é usada por um provedor de serviços em conjunto com a função [**\_ lineDevSpecificFeature do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) .</span><span class="sxs-lookup"><span data-stu-id="72eb6-120">The **LINE\_CALLDEVSPECIFICFEATURE** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) function.</span></span> <span data-ttu-id="72eb6-121">Seu significado é específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72eb6-121">Its meaning is device specific.</span></span>

<span data-ttu-id="72eb6-122">A TAPI envia a mensagem de [**linha \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) para os aplicativos em resposta ao recebimento desta mensagem de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="72eb6-122">TAPI sends the [**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="72eb6-123">Os parâmetros *htLine* e *htCall* são convertidos para o *HCall* apropriado como o parâmetro *hDevice* no nível TAPI.</span><span class="sxs-lookup"><span data-stu-id="72eb6-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="72eb6-124">Os parâmetros *dwParam1*, *dwParam2* e *dwParam3* são passados por meio de não modificado.</span><span class="sxs-lookup"><span data-stu-id="72eb6-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="72eb6-125">Não há nenhuma mensagem diretamente correspondente no nível de TAPI, embora essa mensagem seja muito semelhante à linha \_ DEVSPECIFICFEATURE.</span><span class="sxs-lookup"><span data-stu-id="72eb6-125">There is no directly corresponding message at the TAPI level, although this message is very similar to LINE\_DEVSPECIFICFEATURE.</span></span> <span data-ttu-id="72eb6-126">No nível de TSPI, as mensagens de recurso específicas do dispositivo são divididas entre os eventos de relatório em linhas e endereços, e os eventos de relatório em chamadas.</span><span class="sxs-lookup"><span data-stu-id="72eb6-126">At the TSPI level, the device-specific feature messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="72eb6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72eb6-127">Requirements</span></span>



| <span data-ttu-id="72eb6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="72eb6-128">Requirement</span></span> | <span data-ttu-id="72eb6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="72eb6-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="72eb6-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="72eb6-130">TAPI version</span></span><br/> | <span data-ttu-id="72eb6-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="72eb6-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="72eb6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72eb6-132">Header</span></span><br/>       | <dl> <span data-ttu-id="72eb6-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="72eb6-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72eb6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="72eb6-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="72eb6-135">[**DEVSPECIFICFEATURE de linha \_**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="72eb6-135">[**LINE\_DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="72eb6-136">**TSPI \_ lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="72eb6-136">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

