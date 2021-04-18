---
description: A mensagem de CALLDEVSPECIFIC da linha TSPI \_ é enviada para a função de retorno de chamada LINEEVENT para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma chamada.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: Mensagem de LINE_CALLDEVSPECIFIC (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48bf8a54a1f326fe7bb27c82349e5575c8bbf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769412"
---
# <a name="line_calldevspecific-message"></a><span data-ttu-id="b1837-103">Mensagem de CALLDEVSPECIFIC de linha \_</span><span class="sxs-lookup"><span data-stu-id="b1837-103">LINE\_CALLDEVSPECIFIC message</span></span>

<span data-ttu-id="b1837-104">A mensagem **de \_ CALLDEVSPECIFIC da linha** TSPI é enviada para a função de retorno de chamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) para notificar a TAPI sobre eventos específicos do dispositivo que ocorrem em uma chamada.</span><span class="sxs-lookup"><span data-stu-id="b1837-104">The TSPI **LINE\_CALLDEVSPECIFIC** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function to notify TAPI about device-specific events occurring on a call.</span></span> <span data-ttu-id="b1837-105">O significado da mensagem e a interpretação dos parâmetros *dwParam1* por meio de *dwParam3* são específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1837-105">The meaning of the message and the interpretation of the *dwParam1* through *dwParam3* parameters is device specific.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b1837-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1837-107">*htLine*</span><span class="sxs-lookup"><span data-stu-id="b1837-107">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="b1837-108">O identificador de objeto TAPI opaco para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="b1837-108">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-109">*htCall*</span><span class="sxs-lookup"><span data-stu-id="b1837-109">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="b1837-110">O identificador de objeto TAPI opaco para o dispositivo de chamada.</span><span class="sxs-lookup"><span data-stu-id="b1837-110">The TAPI opaque object handle to the call device.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-111">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="b1837-111">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b1837-112">A linha de valor \_ CALLDEVSPECIFIC.</span><span class="sxs-lookup"><span data-stu-id="b1837-112">The value LINE\_CALLDEVSPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b1837-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b1837-114">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1837-114">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b1837-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b1837-116">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1837-116">Device specific.</span></span>

</dd> <dt>

<span data-ttu-id="b1837-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b1837-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b1837-118">Específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1837-118">Device specific.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1837-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1837-119">Remarks</span></span>

<span data-ttu-id="b1837-120">A **mensagem \_ CALLDEVSPECIFIC de linha** é usada por um provedor de serviços em conjunto com a função [**\_ lineDevSpecific do TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) .</span><span class="sxs-lookup"><span data-stu-id="b1837-120">The **LINE\_CALLDEVSPECIFIC** message is used by a service provider in conjunction with the [**TSPI\_lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) function.</span></span> <span data-ttu-id="b1837-121">Seu significado é específico ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1837-121">Its meaning is device specific.</span></span>

<span data-ttu-id="b1837-122">A TAPI envia a mensagem de [**linha \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) para os aplicativos em resposta ao recebimento desta mensagem de um provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b1837-122">TAPI sends the [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) message to applications in response to receiving this message from a service provider.</span></span> <span data-ttu-id="b1837-123">Os parâmetros *htLine* e *htCall* são convertidos para o *HCall* apropriado como o parâmetro *hDevice* no nível TAPI.</span><span class="sxs-lookup"><span data-stu-id="b1837-123">The *htLine* and *htCall* parameters are translated to the appropriate *hCall* as the *hDevice* parameter at the TAPI level.</span></span> <span data-ttu-id="b1837-124">Os parâmetros *dwParam1*, *dwParam2* e *dwParam3* são passados por meio de não modificado.</span><span class="sxs-lookup"><span data-stu-id="b1837-124">The *dwParam1*, *dwParam2*, and *dwParam3* parameters are passed through unmodified.</span></span>

<span data-ttu-id="b1837-125">Não há nenhuma mensagem diretamente correspondente no nível de TAPI, embora essa mensagem seja muito semelhante à [**linha \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b1837-125">There is no directly corresponding message at the TAPI level, although this message is very similar to [**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)).</span></span> <span data-ttu-id="b1837-126">No nível de TSPI, as mensagens específicas do dispositivo são divididas entre os eventos de relatório em linhas e endereços, e os eventos de relatório em chamadas.</span><span class="sxs-lookup"><span data-stu-id="b1837-126">At the TSPI level, the device-specific messages are split between those reporting events on lines and addresses, and those reporting events on calls.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1837-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1837-127">Requirements</span></span>



| <span data-ttu-id="b1837-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1837-128">Requirement</span></span> | <span data-ttu-id="b1837-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b1837-129">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b1837-130">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b1837-130">TAPI version</span></span><br/> | <span data-ttu-id="b1837-131">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b1837-131">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b1837-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1837-132">Header</span></span><br/>       | <dl> <span data-ttu-id="b1837-133"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1837-133"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1837-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1837-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1837-135">[**DEVSPECIFIC de linha \_**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1837-135">[**LINE\_DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b1837-136">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="b1837-136">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[<span data-ttu-id="b1837-137">**TSPI \_ lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="b1837-137">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

