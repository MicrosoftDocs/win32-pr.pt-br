---
description: A \_ mensagem de AGENTSTATUS de linha TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento. O aplicativo pode invocar lineGetAgentStatus para determinar o status atual do agente.
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: Mensagem de LINE_AGENTSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789454"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="207a8-104">Mensagem de AGENTSTATUS de linha \_</span><span class="sxs-lookup"><span data-stu-id="207a8-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="207a8-105">A mensagem **de \_ AGENTSTATUS de linha** TAPI é enviada quando o status de um agente AD é alterado em uma linha que o aplicativo abriu no momento.</span><span class="sxs-lookup"><span data-stu-id="207a8-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="207a8-106">O aplicativo pode invocar [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) para determinar o status atual do agente.</span><span class="sxs-lookup"><span data-stu-id="207a8-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="207a8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="207a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207a8-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="207a8-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="207a8-109">O identificador do aplicativo para o dispositivo de linha no qual o status do agente foi alterado.</span><span class="sxs-lookup"><span data-stu-id="207a8-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="207a8-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="207a8-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="207a8-111">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="207a8-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="207a8-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="207a8-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="207a8-113">Identificador do endereço na linha na qual o status do agente foi alterado.</span><span class="sxs-lookup"><span data-stu-id="207a8-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="207a8-114">Um identificador de endereço é permanentemente associado a um endereço; o identificador permanece constante nas atualizações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="207a8-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="207a8-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="207a8-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="207a8-116">Especifica o status do agente que foi alterado; pode ser uma combinação de [**\_ constantes LINEAGENTSTATUS**](lineagentstatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="207a8-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="207a8-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="207a8-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="207a8-118">Se *dwParam2* incluir o \_ bit de estado LINEAGENTSTATUS, *dwParam3* indicará o novo valor do membro **dwState** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span><span class="sxs-lookup"><span data-stu-id="207a8-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="207a8-119">Caso contrário, esse parâmetro será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="207a8-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="207a8-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="207a8-120">Return value</span></span>

<span data-ttu-id="207a8-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="207a8-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="207a8-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="207a8-122">Remarks</span></span>

<span data-ttu-id="207a8-123">A **mensagem \_ AGENTSTATUS de linha** não é enviada para aplicativos que dão suporte a versões mais antigas da TAPI.</span><span class="sxs-lookup"><span data-stu-id="207a8-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="207a8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="207a8-124">Requirements</span></span>



| <span data-ttu-id="207a8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="207a8-125">Requirement</span></span> | <span data-ttu-id="207a8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="207a8-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="207a8-127">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="207a8-127">TAPI version</span></span><br/> | <span data-ttu-id="207a8-128">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="207a8-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="207a8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="207a8-129">Header</span></span><br/>       | <dl> <span data-ttu-id="207a8-130"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="207a8-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="207a8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="207a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="207a8-132">**LINEAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="207a8-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="207a8-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="207a8-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




