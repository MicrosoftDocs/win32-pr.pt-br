---
description: A \_ mensagem de AGENTSPECIFIC de linha TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento. O aplicativo pode invocar lineGetAgentStatus para determinar o status atual do agente.
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: Mensagem de LINE_AGENTSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757209"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="85c94-104">Mensagem de AGENTSPECIFIC de linha \_</span><span class="sxs-lookup"><span data-stu-id="85c94-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="85c94-105">A mensagem **de \_ AGENTSPECIFIC de linha** TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento.</span><span class="sxs-lookup"><span data-stu-id="85c94-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="85c94-106">O aplicativo pode invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar o status atual do agente.</span><span class="sxs-lookup"><span data-stu-id="85c94-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="85c94-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85c94-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85c94-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="85c94-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="85c94-109">O identificador do aplicativo para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="85c94-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="85c94-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="85c94-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="85c94-111">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="85c94-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="85c94-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="85c94-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="85c94-113">O índice na matriz de identificadores de extensão do manipulador na estrutura [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) da extensão do manipulador à qual a mensagem está associada.</span><span class="sxs-lookup"><span data-stu-id="85c94-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="85c94-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="85c94-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="85c94-115">Específico da extensão do manipulador.</span><span class="sxs-lookup"><span data-stu-id="85c94-115">Specific to the handler extension.</span></span> <span data-ttu-id="85c94-116">Em geral, esse valor é usado para fazer com que o aplicativo invoque uma função [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) para buscar mais detalhes sobre a mensagem.</span><span class="sxs-lookup"><span data-stu-id="85c94-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="85c94-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="85c94-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="85c94-118">Específico da extensão do manipulador.</span><span class="sxs-lookup"><span data-stu-id="85c94-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85c94-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85c94-119">Return value</span></span>

<span data-ttu-id="85c94-120">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="85c94-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85c94-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="85c94-121">Remarks</span></span>

<span data-ttu-id="85c94-122">A **mensagem \_ AGENTSPECIFIC de linha** não é enviada para aplicativos que dão suporte a versões mais antigas da TAPI.</span><span class="sxs-lookup"><span data-stu-id="85c94-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c94-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c94-123">Requirements</span></span>



| <span data-ttu-id="85c94-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c94-124">Requirement</span></span> | <span data-ttu-id="85c94-125">Valor</span><span class="sxs-lookup"><span data-stu-id="85c94-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="85c94-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="85c94-126">TAPI version</span></span><br/> | <span data-ttu-id="85c94-127">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="85c94-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="85c94-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85c94-128">Header</span></span><br/>       | <dl> <span data-ttu-id="85c94-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c94-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c94-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="85c94-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c94-131">**LINEAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="85c94-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="85c94-132">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="85c94-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="85c94-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="85c94-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




