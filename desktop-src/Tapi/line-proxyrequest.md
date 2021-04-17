---
description: A mensagem de PROXYREQUEST de linha TAPI \_ entrega uma solicitação para um manipulador de função proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Mensagem de LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761957"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="71b11-103">Mensagem de PROXYREQUEST de linha \_</span><span class="sxs-lookup"><span data-stu-id="71b11-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="71b11-104">A mensagem **de \_ PROXYREQUEST de linha** TAPI entrega uma solicitação para um manipulador de função proxy registrado.</span><span class="sxs-lookup"><span data-stu-id="71b11-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="71b11-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71b11-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b11-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="71b11-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="71b11-107">O identificador do aplicativo para o dispositivo de linha no qual o status do agente foi alterado.</span><span class="sxs-lookup"><span data-stu-id="71b11-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="71b11-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="71b11-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="71b11-109">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="71b11-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="71b11-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="71b11-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="71b11-111">Ponteiro para uma estrutura [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) que contém a solicitação a ser processada pelo aplicativo de manipulador de proxy.</span><span class="sxs-lookup"><span data-stu-id="71b11-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="71b11-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="71b11-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="71b11-113">Reservado.</span><span class="sxs-lookup"><span data-stu-id="71b11-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="71b11-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="71b11-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="71b11-115">Reservado.</span><span class="sxs-lookup"><span data-stu-id="71b11-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b11-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71b11-116">Return value</span></span>

<span data-ttu-id="71b11-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="71b11-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71b11-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="71b11-118">Remarks</span></span>

<span data-ttu-id="71b11-119">A mensagem de **linha \_ PROXYREQUEST** é enviada somente para o primeiro aplicativo registrado para lidar com solicitações de proxy do tipo que está sendo entregue.</span><span class="sxs-lookup"><span data-stu-id="71b11-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="71b11-120">O aplicativo deve processar a solicitação contida no buffer de proxy e chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para retornar dados ou fornecer resultados.</span><span class="sxs-lookup"><span data-stu-id="71b11-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="71b11-121">O processamento da solicitação deve ser feito dentro do contexto da função de retorno de chamada TAPI do aplicativo somente se puder ser executado imediatamente, sem aguardar a resposta de qualquer outra entidade.</span><span class="sxs-lookup"><span data-stu-id="71b11-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="71b11-122">Se o aplicativo precisar se comunicar com outras entidades (por exemplo, um provedor de serviços para lidar com AD baseados em PBX ou qualquer outro serviço do sistema que possa resultar em bloqueio), a solicitação deverá ser enfileirada no aplicativo e a função de retorno de chamada será encerrada para evitar atrasar o recebimento de mensagens TAPI adicionais pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71b11-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="71b11-123">No momento em que a **linha \_ PROXYREQUEST** é entregue ao manipulador de proxy, a TAPI já retornou um resultado de função *dwRequestID* positivo para o aplicativo original e desbloqueou o thread de chamada para continuar a execução.</span><span class="sxs-lookup"><span data-stu-id="71b11-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="71b11-124">O aplicativo está aguardando uma mensagem de [**\_ resposta de linha**](line-reply.md) , que é gerada automaticamente quando o aplicativo do manipulador de proxy chama [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="71b11-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="71b11-125">O aplicativo não deve liberar a memória apontada por *lpProxyRequest*.</span><span class="sxs-lookup"><span data-stu-id="71b11-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="71b11-126">A TAPI libera a memória durante a execução de [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="71b11-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="71b11-127">O aplicativo pode chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exatamente uma vez para cada **linha \_ PROXYREQUEST** Message.</span><span class="sxs-lookup"><span data-stu-id="71b11-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="71b11-128">Se o aplicativo receber uma mensagem de [**\_ fechamento de linha**](line-close.md) enquanto tem solicitações de proxy pendentes, ele deverá chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitação pendente, passando um valor *dwResult* apropriado (como LINEERR \_ OPERATIONFAILED).</span><span class="sxs-lookup"><span data-stu-id="71b11-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="71b11-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71b11-129">Requirements</span></span>



| <span data-ttu-id="71b11-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b11-130">Requirement</span></span> | <span data-ttu-id="71b11-131">Valor</span><span class="sxs-lookup"><span data-stu-id="71b11-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="71b11-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="71b11-132">TAPI version</span></span><br/> | <span data-ttu-id="71b11-133">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="71b11-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="71b11-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71b11-134">Header</span></span><br/>       | <dl> <span data-ttu-id="71b11-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b11-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b11-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="71b11-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b11-137">**fechamento de linha \_**</span><span class="sxs-lookup"><span data-stu-id="71b11-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="71b11-138">**resposta de linha \_**</span><span class="sxs-lookup"><span data-stu-id="71b11-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="71b11-139">**LINEPROXYREQUEST**</span><span class="sxs-lookup"><span data-stu-id="71b11-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="71b11-140">**lineProxyResponse**</span><span class="sxs-lookup"><span data-stu-id="71b11-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




