---
description: A \_ mensagem statusfila de linha é enviada quando o status de uma fila AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: Mensagem de LINE_QUEUESTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779902"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="3e036-104">Mensagem de statusfila de linha \_</span><span class="sxs-lookup"><span data-stu-id="3e036-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="3e036-105">A **mensagem \_ Statusfila de linha** é enviada quando o status de uma fila AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta.</span><span class="sxs-lookup"><span data-stu-id="3e036-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="3e036-106">Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="3e036-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="3e036-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e036-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e036-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="3e036-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="3e036-109">O identificador do aplicativo para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="3e036-109">The application's handle to the line device.</span></span> <span data-ttu-id="3e036-110">Isso está relacionado ao manipulador do agente.</span><span class="sxs-lookup"><span data-stu-id="3e036-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="3e036-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="3e036-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="3e036-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="3e036-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="3e036-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="3e036-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="3e036-114">O identificador da fila cujo status foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3e036-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="3e036-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="3e036-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="3e036-116">Especifica o status da fila que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="3e036-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="3e036-117">Pode ser uma ou mais das [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="3e036-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e036-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="3e036-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="3e036-119">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3e036-119">Reserved.</span></span> <span data-ttu-id="3e036-120">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3e036-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e036-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e036-121">Requirements</span></span>



| <span data-ttu-id="3e036-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e036-122">Requirement</span></span> | <span data-ttu-id="3e036-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3e036-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3e036-124">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3e036-124">TAPI version</span></span><br/> | <span data-ttu-id="3e036-125">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="3e036-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="3e036-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e036-126">Header</span></span><br/>       | <dl> <span data-ttu-id="3e036-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e036-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e036-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e036-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e036-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="3e036-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




