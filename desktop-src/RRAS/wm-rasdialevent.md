---
title: Mensagem de WM_RASDIALEVENT (RAS. h)
description: O sistema operacional envia uma \_ mensagem do WM RASDIALEVENT para um procedimento de janela quando uma alteração de evento de estado ocorre durante um processo de conexão RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- RAS de mensagens WM_RASDIALEVENT
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782291"
---
# <a name="wm_rasdialevent-message"></a><span data-ttu-id="14566-104">Mensagem do WM \_ RASDIALEVENT</span><span class="sxs-lookup"><span data-stu-id="14566-104">WM\_RASDIALEVENT message</span></span>

<span data-ttu-id="14566-105">O sistema operacional envia uma mensagem do **WM \_ RASDIALEVENT** para um procedimento de janela quando uma alteração de evento de estado ocorre durante um processo de conexão RAS.</span><span class="sxs-lookup"><span data-stu-id="14566-105">The operating system sends a **WM\_RASDIALEVENT** message to a window procedure when a change of state event occurs during a RAS connection process.</span></span> <span data-ttu-id="14566-106">Isso acontece quando uma janela é especificada para manipular notificações de tais eventos usando o parâmetro de *notificador* de [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span><span class="sxs-lookup"><span data-stu-id="14566-106">This happens when a window has been specified to handle notifications of such events by using the *notifier* parameter of [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).</span></span>

<span data-ttu-id="14566-107">Os dois parâmetros de mensagem são equivalentes aos parâmetros dos mesmos nomes que são usados com as funções de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="14566-107">The two message parameters are equivalent to the parameters of the same names that are used with [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span>


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a><span data-ttu-id="14566-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14566-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14566-109">*rasconnstate*</span><span class="sxs-lookup"><span data-stu-id="14566-109">*rasconnstate*</span></span> 
</dt> <dd>

<span data-ttu-id="14566-110">Valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="14566-110">Value of *wParam*.</span></span> <span data-ttu-id="14566-111">Equivalente ao parâmetro *RASCONNSTATE* das funções de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="14566-111">Equivalent to the *rasconnstate* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="14566-112">Especifica um valor de enumerador [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) que indica o estado que o processo de conexão de acesso remoto de RasDial está prestes a entrar.</span><span class="sxs-lookup"><span data-stu-id="14566-112">Specifies a [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) enumerator value that indicates the state the RasDial remote access connection process is about to enter.</span></span>

</dd> <dt>

<span data-ttu-id="14566-113">*dwError*</span><span class="sxs-lookup"><span data-stu-id="14566-113">*dwError*</span></span> 
</dt> <dd>

<span data-ttu-id="14566-114">Valor de *lParam*.</span><span class="sxs-lookup"><span data-stu-id="14566-114">Value of *lParam*.</span></span> <span data-ttu-id="14566-115">Equivalente ao parâmetro *dwError* das funções de retorno de chamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .</span><span class="sxs-lookup"><span data-stu-id="14566-115">Equivalent to the *dwError* parameter of the [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) and [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) callback functions.</span></span> <span data-ttu-id="14566-116">Um valor diferente de zero indica o erro que ocorreu ou zero se nenhum erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="14566-116">A nonzero value indicates the error that has occurred, or zero if no error has occurred.</span></span>

<span data-ttu-id="14566-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) envia essa mensagem com *dwError* definido como zero na entrada para cada Estado de conexão.</span><span class="sxs-lookup"><span data-stu-id="14566-117">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) sends this message with *dwError* set to zero upon entry to each connection state.</span></span> <span data-ttu-id="14566-118">Se ocorrer um erro dentro de um estado, a mensagem será enviada novamente para o estado, desta vez com um valor *dwError* diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="14566-118">If an error occurs within a state, the message is sent again for the state, this time with a nonzero *dwError* value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14566-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14566-119">Return value</span></span>

<span data-ttu-id="14566-120">Se um aplicativo processar essa mensagem, ele deverá retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="14566-120">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14566-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14566-121">Requirements</span></span>



| <span data-ttu-id="14566-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14566-122">Requirement</span></span> | <span data-ttu-id="14566-123">Valor</span><span class="sxs-lookup"><span data-stu-id="14566-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="14566-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14566-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14566-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14566-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="14566-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14566-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14566-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="14566-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="14566-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="14566-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="14566-129"><dt>RAS. h</dt></span><span class="sxs-lookup"><span data-stu-id="14566-129"><dt>Ras.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14566-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="14566-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14566-131">Visão geral do serviço de acesso remoto (RAS)</span><span class="sxs-lookup"><span data-stu-id="14566-131">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="14566-132">Mensagens do serviço de acesso remoto</span><span class="sxs-lookup"><span data-stu-id="14566-132">Remote Access Service Messages</span></span>](remote-access-service-messages.md)
</dt> <dt>

[<span data-ttu-id="14566-133">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="14566-133">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[<span data-ttu-id="14566-134">**RasDialFunc**</span><span class="sxs-lookup"><span data-stu-id="14566-134">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[<span data-ttu-id="14566-135">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="14566-135">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

<span data-ttu-id="14566-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14566-136">[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))</span></span>
</dt> </dl>

 

